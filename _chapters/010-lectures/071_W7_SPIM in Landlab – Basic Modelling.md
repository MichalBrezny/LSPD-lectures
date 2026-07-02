---
title: W7 – SPIM in Landlab – Basic Modelling
slug: week7-spim-landlab-basic-modelling
abstract: A hands-on walkthrough of building, running, and interpreting a Stream Power Incision Model in Landlab.
---

# Landlab and Basic SPIM Modelling

In the previous lecture we introduced Landscape Evolution Models conceptually. Here we build one. This session translates the **Stream Power Incision Model (SPIM)** from equation to running code, drives it with uplift until it reaches steady state, and then perturbs it to watch a transient response propagate through the landscape.

## Learning objectives
By the end of this session you should be able to:
- assemble a minimal SPIM in Landlab from its core components,
- set boundary conditions and a stable time step,
- run a model to steady state and recognise when it has arrived,
- change a single parameter and predict, then verify, the response,
- visualise and interpret model output (topography, slope–area, χ).

## Recap: the equation we are implementing
The SPIM describes the rate of river incision into bedrock as a power-law function of drainage area (a proxy for discharge) and channel slope:

$$
E = K \, A^{m} \, S^{n}
$$

where $E$ is the incision rate, $A$ is the upstream drainage area, $S$ is the local channel slope, $K$ is the erodibility coefficient (lithology, climate, sediment effects lumped together), and $m$ and $n$ are exponents. Combined with rock uplift $U$, the change in elevation $z$ at each point in time is:

$$
\frac{\partial z}{\partial t} = U - K \, A^{m} \, S^{n}
$$

> [!NOTE]
> A landscape is at **steady state** when uplift and erosion balance everywhere, so $\partial z / \partial t = 0$. At steady state the SPIM predicts a fixed channel steepness for a given uplift rate — the link we exploit in the χ and $k_{sn}$ lectures.

## Anatomy of a Landlab SPIM
Every model we build is the same five ingredients assembled in the same order:

1. **A grid** — the raster that stores elevation and every derived field.
2. **An elevation field** — the initial condition (usually a flat surface plus tiny random noise to break symmetry).
3. **Boundary conditions** — which edges are open (base level, water/sediment leaves) and which are closed (walls).
4. **Process components** — a `FlowAccumulator` (routes flow, computes $A$) and an eroder (`FastscapeEroder`, which solves the SPIM).
5. **A time loop** — apply uplift, route flow, erode, advance time; repeat.

## Step-by-step build

### 1. Grid and initial condition
```python
import numpy as np
from landlab import RasterModelGrid
from landlab.components import FlowAccumulator, FastscapeEroder

# 100 x 100 cells, 100 m spacing  -> a 10 x 10 km domain
mg = RasterModelGrid((100, 100), xy_spacing=100.0)

# Flat surface + small random noise so flow routing has something to work with
np.random.seed(42)  # reproducibility
z = mg.add_zeros("topographic__elevation", at="node")
z += np.random.rand(mg.number_of_nodes)  # ~0-1 m of noise
```

### 2. Boundary conditions
Decide where material can leave the model. Here we open all four edges (fixed base level around the perimeter); everything inside is free to evolve.
```python
mg.set_closed_boundaries_at_grid_edges(False, False, False, False)  # all edges open
```
> [!TIP]
> A common variant is to **close three edges and open one** (a single outlet), which forces all drainage toward one side — useful for mimicking a range front.

### 3. Add the process components
```python
fa = FlowAccumulator(mg, flow_director="D8")          # computes drainage area A
sp = FastscapeEroder(mg, K_sp=1e-5, m_sp=0.5, n_sp=1.0)  # solves E = K A^m S^n
```

### 4. Choose parameters and time step
```python
U  = 0.001     # uplift rate (m/yr)
dt = 1000.0    # time step (yr)
n_steps = 500  # -> 500,000 yr of model time
```
> [!WARNING]
> With the explicit `StreamPowerEroder`, the time step is limited by the **CFL condition** (roughly $\Delta t < \Delta x / v$, where $v$ is knickpoint celerity) or the model becomes unstable. `FastscapeEroder` uses an implicit solver and tolerates much larger $\Delta t$ — that is why we use it here.

### 5. The time loop
```python
for i in range(n_steps):
    z[mg.core_nodes] += U * dt      # uplift the interior only
    fa.run_one_step()               # route flow, update drainage area
    sp.run_one_step(dt)             # erode according to the SPIM
```

## Reaching steady state (spin-up)
The model starts far from equilibrium (a noisy near-flat plane) and must **spin up** before its topography is physically meaningful. Track a diagnostic each step and stop when it stops changing:
```python
mean_z = z[mg.core_nodes].mean()   # or max relief, or total erosion flux
```
Plotting `mean_z` against time gives a curve that rises and then flattens — the flattening marks the approach to steady state.

## Visualising the output
```python
from landlab import imshow_grid

imshow_grid(mg, "topographic__elevation", cmap="terrain",
            colorbar_label="Elevation (m)")
```
Three views worth generating every time:
- **Topography map** — overall relief and drainage organisation.
- **Slope–area plot** ($\log S$ vs $\log A$) — the slope of the fluvial part of this plot is $-m/n$ (the concavity); a good check that the model behaves as the SPIM predicts.
- **χ-plot** — connects this lecture back to W5; collinear tributaries indicate steady state.

## Numerical experiment: a transient response
This is the payoff. Take a steady-state landscape and **double the uplift rate**, then keep running:
```python
U = 0.002   # doubled
# ... continue the same time loop ...
```
Watch what happens: a **knickpoint** appears at the outlet and sweeps upstream, separating the newly steepened lower channel (adjusted to the higher uplift) from the still-relict upper channel. Over time the whole network re-steepens to a new, higher steady-state $k_{sn}$.

> [!NOTE]
> This single experiment demonstrates the course's central theme: **topography is a filtered, time-lagged record of tectonic forcing.** The knickpoint *is* the tectonic signal migrating through the landscape.

## Parameter exploration
Vary one thing at a time and predict before you run:

| Parameter | Change | Expected effect |
|-----------|--------|-----------------|
| $K$ (erodibility) | decrease | steeper channels, higher relief at steady state |
| $U$ (uplift) | increase | steeper channels, higher relief, faster erosion |
| $m/n$ (concavity) | change ratio | more/less concave long profiles |
| grid resolution | finer | sharper drainage, but longer run time |

## Common pitfalls
- Uplifting **all** nodes instead of only `core_nodes` (the boundaries should stay fixed as base level).
- Forgetting to re-run `FlowAccumulator` each step — drainage area then never updates.
- Reading topography **before spin-up** and mistaking transient noise for signal.
- An unstable explicit time step producing checkerboard artefacts or `NaN`s.

## Exercise / deliverable
1. Build the steady-state model above and record its mean elevation and relief.
2. Change **one** parameter (your choice of $K$ or $U$). Write down your prediction *first*.
3. Run to a new steady state and compare topography, slope–area, and χ before and after.
4. Submit: two annotated figures + a short paragraph on whether the outcome matched your prediction and why.

---

## Key references and further reading
- Barnhart, K. R., et al. (2020). Landlab v2.0: a software package for Earth surface dynamics. *Earth Surface Dynamics*.
- Tucker, G. E., & Hancock, G. R. (2010). Modelling landscape evolution. *Earth Surface Processes and Landforms*.
- Whipple, K. X., & Tucker, G. E. (1999). Dynamics of the stream-power river incision model. *Journal of Geophysical Research*.

{% include youtube.html id="jrpabwebOGY" title="Landlab – running a model" %}
