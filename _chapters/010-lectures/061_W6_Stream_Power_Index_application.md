---
title: W6 – Stream Power Incision Model – Applications
slug: week6-application-stream-power-incision-model
abstract:
---

<!--- **Structure**
- **Introduction (5 min)**
  - From equations to real-world catchments.
- **Core Concepts (25 min)**
  - Deriving m/n from slope–area regressions.
  - SPIM in steady vs. transient settings.
  - Model calibration: fitting K using known incision rates.
  - Testing sensitivity of erosion rates to parameter changes.
- **Examples (10 min)**
  - Grand Canyon incision history.
- **Wrap-up (5–10 min)**
  - Short exercise: students calculate predicted incision for a sample catchment.

### Lab 5: Stream Power Calculations
**Objectives**
- Apply SPIM to real DEM-derived catchments.

**Steps**
1. **Extract slope–area data** from selected basins.
2. **Fit regression** to determine concavity (θ) and steepness.
3. **Estimate m and n values** from theory vs. data.
4. **Calculate erosion rates** for given K, m, n.
5. **Exercise**
   - Compare two basins (active vs. passive margin).
   - Discuss sensitivity to DEM resolution.
--->

# Applications of stream power incision model

The Stream Power Incision Model (SPIM) is widely used to understand and predict river incision rates in various geological settings. In this lecture, we will focus on how to apply SPIM to real-world catchments, derive model parameters from topographic data, and calibrate the model using known incision rates.

## Introduction: From Explanation to Experiment
$\chi$ analysis showed us *what* the landscape is doing, and SPIM explains *why*. The next step is to use the model actively:

> *Use SPIM to test hypotheses about tectonic forcing.*

A hypothesis such as "the uplift rate doubled two million years ago" has consequences that SPIM allows us to calculate: how steep the rivers should be, where the knickpoints should be today, and how much relief should have been created. These predictions can be compared with the real landscape.

## Applying SPIM: estimating the parameters
To apply SPIM to real-world catchments, we need the model parameters $K$, $m$ and $n$. Topography alone does not provide all of them, and it is important to understand what can be obtained from which data.

### Step 1: concavity ($m/n$) from topography
The first step is to analyze the slope–area relationship obtained from a digital elevation model (DEM) of the catchment:

$$S = k_s A^{-\theta}$$

where $k_s$ is the channel steepness index and $\theta$ is the concavity index. By plotting slope ($S$) against drainage area ($A$) on a log-log scale, we can fit a linear regression to determine $\theta$ (the negative slope of the line) and $k_s$ (the intercept). Alternatively, and with less noise, $\theta$ can be found as the value that makes the $\chi$ plot most linear (W5).

For a river in steady state, $\theta$ equals the ratio $m/n$. The topography of a steady-state river gives only this ratio and not the individual values of $m$ and $n$.

### Step 2: steepness ($k_{sn}$) from topography
With a fixed reference concavity we calculate the normalized steepness index $k_{sn}$, either from slope and area or as the slope of the $\chi$ plot. In steady state

$$ k_{sn} = \left( \frac{E}{K} \right)^{1/n} $$

where the erosion rate $E$ equals the uplift rate $U$. Steepness gives us the ratio $E/K$, and again not the individual values.

### Step 3: $n$ and $K$ from independent rates
To separate the parameters we need erosion or incision rates measured independently, for example from cosmogenic nuclides in river sediment, from dated river terraces or from thermochronology.

If we have several basins with similar rocks and climate but different erosion rates, we can plot $k_{sn}$ against $E$. According to the equation above, the data should follow a power law with the exponent $1/n$, and its coefficient gives $K$. Global compilations of such data suggest that $n$ is often larger than 1 (Harel et al., 2016).

If we have only one rate, we have to assume $n$ (most often $n = 1$, and $m$ then equals $\theta_{ref}$) and calculate the erodibility as

$$ K = \frac{E}{k_{sn}^{\,n}} $$

This is the calibration of the model: $K$ is adjusted so that the model reproduces the observed incision rate.

> [!NOTE]
> **Worked example.** A basin has a mean $k_{sn} = 100\ \mathrm{m^{0.9}}$ (calculated with $\theta_{ref} = 0.45$) and a cosmogenic erosion rate of 0.1 mm/yr, i.e., $10^{-4}$ m/yr. Assuming steady state and $n = 1$:
> $$ K = \frac{10^{-4}}{100} = 10^{-6}\ \mathrm{m^{0.1}\,yr^{-1}} $$

> [!IMPORTANT]
> A calibrated $K$ is valid only for the lithology and climate of the area where it was obtained, and only together with the values of $m$ and $n$ that were used in the calibration. It cannot be transferred to a model with different exponents.

### Step 4: sensitivity
Finally, it is important to test the sensitivity of the results to the parameters $K$, $m$ and $n$. This helps to understand how the uncertainties in these parameters affect the predicted incision rates. We will return to it in W10.

---

## Steady-State Solutions

### Balance Between Uplift and Incision
At steady state, $U = K A^m S^n$ holds everywhere along the channel. The slope of every reach is determined by its drainage area and by the ratio $U/K$:

$$ S = \left( \frac{U}{K} \right)^{1/n} A^{-m/n} $$

Spatially uniform uplift therefore produces a systematic pattern of slopes, decreasing downstream as drainage area grows. Rivers encode uplift in their geometry.

### Forward prediction
SPIM allows forward prediction: if the forcing changes, how must the river respond?

> [!NOTE]
> **Worked example.** With $K = 10^{-6}\ \mathrm{m^{0.1}\,yr^{-1}}$, $m = 0.45$, $n = 1$ and an uplift rate $U = 0.1$ mm/yr, the steepness is $U/K = 100\ \mathrm{m^{0.9}}$. A reach with a drainage area of 10 km² ($10^7$ m²) has a steady-state slope of
> $$ S = 100 \times (10^7)^{-0.45} \approx 0.07 $$
> If the uplift rate doubles, the steady-state slope of this reach doubles to about 0.14. With $n = 2$ and the same initial steepness, the slope would increase only by a factor of $\sqrt{2}$, to about 0.10.

### Fluvial relief
The same equation predicts the fluvial relief, i.e., the elevation difference between the outlet and the channel head. From the $\chi$ form of the steady-state profile (with $A_0 = 1\ \mathrm{m^2}$):

$$ R = k_{sn}\, \chi_{max} = \left( \frac{U}{K} \right)^{1/n} \chi_{max} $$

where $\chi_{max}$ is the value of $\chi$ at the channel head. The relief increases with the uplift rate, with rock resistance and with the size of the basin.

### Spatial Variations
Spatial changes in uplift rate or erodibility produce predictable changes in the steady-state profile:
- Where a river enters a zone of faster uplift, it becomes steeper, and $k_{sn}$ increases in proportion to $U^{1/n}$.
- Where a river crosses more resistant rocks (lower $K$), it becomes steeper as well.
- The boundaries appear as slope-break knickpoints that stay in place.

In all these cases the river is in steady state, although its profile is not smooth. This is the reason why a knickpoint alone is not evidence of a transient state.

---

##  Transient Scenarios 

### Uplift Rate Change
A sudden increase in the uplift rate produces a steep reach near the outlet. Its upstream end is a knickpoint, which migrates upstream. Downstream of the knickpoint the river is already adjusted to the new uplift rate (higher $k_{sn}$), and upstream of it the river still has the steepness that corresponds to the old uplift rate.

The rate of migration (celerity) of the knickpoint is

$$ C = K A^m S^{n-1} $$

It depends on the erodibility $K$ and on the drainage area. For $n = 1$ it does not depend on the slope. For $n > 1$ steeper knickpoints migrate faster.

The response time of the river is the time the knickpoint needs to reach the channel head. For $n = 1$ there is a simple and useful rule: the response time equals the steady-state fluvial relief divided by the uplift rate,

$$ \tau = \frac{\chi_{max}}{K} = \frac{R}{U} $$

where $R$ and $U$ are the relief and the uplift rate of the new steady state. For example, a river with 1000 m of fluvial relief adjusted to an uplift rate of 0.5 mm/yr has a response time of about 2 million years. Response times of the order of 10⁵–10⁷ years are typical for mountain rivers (Whipple and Tucker, 1999; Whipple, 2001). The whole landscape needs more time, because hillslopes respond only after the channels.

The ratio of the steepness below and above the knickpoint records the magnitude of the change:

$$ \frac{k_{sn,\,new}}{k_{sn,\,old}} = \left( \frac{U_{new}}{U_{old}} \right)^{1/n} $$

### Base-Level Fall
A river responds to a sudden fall in base level in a similar way to a pulse of uplift. A step is created at the outlet and migrates upstream with the same celerity. After it has passed, the river returns to its original steepness, because the uplift rate has not changed. The knickpoint is therefore a vertical step and not a slope break (W5).

This mechanism explains, for example:
- postglacial incision of rivers into valley fills and glacially overdeepened valleys,
- the response of rivers to sea-level changes,
- incision following river capture or the drainage of a lake.

---

## Interpreting SPIM Outputs

### What SPIM Can Tell Us
- Relative patterns of uplift: where steepness is higher under similar rocks and climate, uplift is probably faster.
- The magnitude of a change in uplift rate, from the steepness below and above a knickpoint.
- Incision histories, at least qualitatively: the order of events and whether a landscape is in steady or transient state.
- Expected profile shapes for a given scenario, which can be compared with observed profiles.

### What SPIM Cannot Tell Us
- Absolute uplift rates without calibration. Topography gives only $U/K$.
- The exact timing of events. The response time depends on $K$ and $n$, which are poorly known.
- The effects of complex sediment dynamics, changes in channel width or changes in climate through time.

---

## Linking SPIM to LEMs 

In this week we applied SPIM in one dimension, along individual channels with a given drainage area. Landscape evolution models (LEMs):
- extend SPIM across a two-dimensional surface, where the drainage area is not given but evolves together with the topography,
- couple river incision with hillslope processes and tectonics.

It is a conceptual shift:
> *From interpreting rivers to simulating landscapes.*

---

## Wrap-up & Transition

Key takeaways:
- SPIM explains the patterns in $\chi$ space mechanistically.
- Topography constrains $m/n$ and $U/K$. Independent rates are needed to obtain $n$ and $K$.
- The parameters have a physical meaning tied to tectonics, lithology and climate.
- Transient signals travel upstream with a predictable celerity, so the positions of knickpoints carry information on timing.

> *Next, we implement SPIM numerically to explore landscape evolution through time.*

# References
Harel, M.-A., Mudd, S.M., Attal, M., 2016. Global analysis of the stream power law parameters based on worldwide ¹⁰Be denudation rates. Geomorphology 268, 184–196. https://doi.org/10.1016/j.geomorph.2016.05.035

Whipple, K.X., 2001. Fluvial landscape response time: how plausible is steady-state denudation? American Journal of Science 301, 313–325. https://doi.org/10.2475/ajs.301.4-5.313

Whipple, K.X., Tucker, G.E., 1999. Dynamics of the stream-power river incision model: Implications for height limits of mountain ranges, landscape response timescales, and research needs. Journal of Geophysical Research: Solid Earth 104, 17661–17674. https://doi.org/10.1029/1999JB900120
