---
title: W10 – Data–Model Integration and Uncertainty
slug: week10-data-model-integration-uncertainty
abstract:
---

# The Role of Data in Quantitative Geomorphology


To sum up what we have learned so far:
  - Tectonics provides forcing.
  - Rivers respond (chi, ksn).
  - SPIM explains mechanisms.
  - LEMs simulate evolution.

In this week we put these parts together and ask how models and data should be combined, and how far the results can be trusted.

# Embracing Uncertainty
In quantitative geomorphology, we use **models** to explore how landscapes might respond to tectonic forcing, climate, and surface processes. We use **data** to constrain what is physically plausible.  

Neither models nor data alone can fully explain landscape evolution:

- **Models without data** are unconstrained and speculative.
- **Data without models** are difficult to interpret mechanistically.

> **Key idea:** Models help us *ask better questions*, not provide final answers.

Scientific models are tools, not answers.

> [!WARNING]
> Classic motto: Garbage in, garbage out. Models are only as good as the data and assumptions that go into them. Understanding and quantifying uncertainty is crucial for responsible interpretation.


## Calibration vs. Constraint

Data can be used in a model in two ways:

- **Calibration**: tuning the model parameters until the model output matches the data as closely as possible. The result is one "best" set of parameters.
- **Constraint**: using the data to limit the parameter values to a plausible range. The result is a set of acceptable parameter combinations.

In this course, we focus on **constraint**, not calibration. A calibrated model gives a false impression of precision: it hides the fact that other parameter sets might fit the data almost equally well.

> Matching the data does **not** prove the model is correct.

---

## Types of Data Used to Constrain Models
What is a constraint? A model works in a parameter space, i.e., the space of all possible combinations of its parameter values. When we do not know the exact values of the parameters, we can use data to limit their plausible ranges. This is called constraining the model.

The models we used in this course have several parameters:
  - uplift rate ($U$),
  - erodibility ($K$),
  - concavity ($m/n$),
  - diffusion coefficient ($D$).

Each of them can vary within some range, and different types of data constrain different parameters. The types of data also differ in the timescale over which they average. This is essential when they are compared with each other and with a model:

| Data | Averaging timescale | What it constrains |
|---|---|---|
| Topography (DEM) | 10⁴–10⁷ yr (response time of the landscape) | $m/n$, the ratio $U/K$, steady vs. transient state |
| Sediment yield, gauging | 10⁰–10² yr | modern erosion rate |
| Cosmogenic nuclides (¹⁰Be) | 10³–10⁵ yr | basin-averaged erosion rate |
| Thermochronology | 10⁶–10⁷ yr | long-term exhumation rate |
| Geodesy (GNSS, levelling, InSAR) | 10⁰–10¹ yr | present-day surface motion |
| Dated markers (terraces, shorelines) | 10³–10⁶ yr | rock uplift or incision rate |

## What data are used to constrain models?

### Topographic Data (Primary Constraint)
Topography is the primary constraint, because it is the output that landscape evolution models predict. The metrics derived from a DEM include:
  - river profiles,
  - chi plots,
  - slope distributions,
  - hypsometry.

Topography constrains the relative pattern of uplift, the spatial variability of the landscape and whether it is in a steady or a transient state. Its strengths are that it is spatially continuous and widely available. Its limitations are that it integrates long time periods, so we see the sum of everything that happened during the response time of the landscape, and that its interpretation is non-unique. As we saw in W6, steady-state topography constrains only the ratios $m/n$ and $U/K$.

### Erosion Rate Data
#### Cosmogenic nuclides (e.g. ¹⁰Be)
We can use the concentrations of cosmogenic nuclides such as ¹⁰Be in river sediments to estimate basin-averaged erosion rates (Granger et al., 1996; von Blanckenburg, 2005). The nuclides are produced by cosmic rays in the uppermost metres of rock and soil. The slower the surface erodes, the longer the mineral grains stay in this zone and the higher the concentration they accumulate. River sand is a natural mixture of grains from the whole basin, so one sample gives the mean erosion rate of the basin.

The rate is averaged over the time needed to erode about 60 cm of rock. At an erosion rate of 0.1 mm/yr it is about 6,000 years, and at 1 mm/yr only about 600 years. Typical averaging times are 10³–10⁵ years. These measurements provide a direct constraint on how quickly landscapes are lowering, which can be compared to model predictions.

#### Sediment yield
The sediment load measured at gauging stations or the volume of sediment trapped in reservoirs and lakes gives the modern erosion rate of the basin. The records cover years to decades, so they are strongly affected by land use and dams, and they may miss rare large events.

#### Thermochronology
Thermochronometers such as apatite fission tracks or (U-Th)/He record the time when a rock cooled below a certain temperature on its way to the surface. With an estimate of the geothermal gradient, the cooling age gives the exhumation rate averaged over millions of years (Reiners and Brandon, 2006).

#### Comparing rates
All these methods constrain the magnitude of incision or denudation, but each of them represents a specific timescale, and they are not directly comparable. A difference between short-term and long-term rates is a common observation. For example, in the mountains of Idaho the erosion rates over thousands to millions of years are many times higher than the sediment yields measured over decades, probably because sediment is delivered mostly by rare, large events (Kirchner et al., 2001). Such a difference is a result in itself and not an error.

### Uplift and Boundary Condition Data
- **Geodetic data** (GNSS, levelling, InSAR) give the present-day rates of surface motion. They cover years to decades and may record only a part of the earthquake cycle, so they need not represent long-term rates.
- **Geological proxies** give long-term rates: river and marine terraces and other dated markers (W4), and thermochronology.

In models these data have a different role than topography and erosion rates: they define the forcing and not the outcome. We prescribe them as boundary conditions and compare the outcome with the other data.

## How Data Are Used in Models (Conceptually)

### Forward vs. Inverse Thinking
- **Forward modeling** goes from cause to effect: we assume the forcing and predict the landscape. We prescribe $U$, $K$ and $m/n$ and simulate the topography. The Landlab exercises in W7 were forward models.
- **Inverse reasoning** goes from effect to cause: we observe the landscape and infer the forcing. Given the topography, we estimate $U$, $K$ and $m/n$. The interpretation of $k_{sn}$ maps in terms of uplift is an example.

A forward model always has one solution. An inverse problem usually has many.

> [!WARNING]
> Inversion is inherently non-unique. Multiple parameter sets can yield similar landscapes.

In practice, inversion is done by running a forward model many times with different parameters and keeping the runs that agree with the data (see the next part on Monte Carlo simulations).

### Non-Uniqueness and Equifinality

Various parameter combinations can produce similar model outputs. This is known as **equifinality**. It is similar to several roads leading to the same destination, although the journeys differ significantly. Evolutionary biologists know the same thing as convergent evolution: different paths leading to similar forms (e.g., wings in bats and birds).

We have already met a clear example. The steady-state steepness of a river depends on the ratio $U/K$. A river in weak rocks with fast uplift and a river in resistant rocks with slow uplift can have identical profiles. No analysis of topography can distinguish them, however precise it is.

Equifinality is unavoidable, because we never know everything about the system:
  - the past climate is unknown,
  - lithology varies in space,
  - the boundary and initial conditions are incomplete.

The consequence is:
  > *Matching topography does not prove correctness.*

Equifinality can be reduced, although not removed, by adding independent types of data. An erosion rate from cosmogenic nuclides separates $U$ from $K$ in steady state. A dated knickpoint or terrace constrains the response time. Each new type of data excludes a part of the parameter space.

---

## Wrap-up 

Key messages:
  - Data guide models, they do not validate them absolutely.
  - Agreement ≠ truth.
  - Different data average over different timescales, and they must be compared with care.
  - Focus on patterns, not exact fits.

# References
Granger, D.E., Kirchner, J.W., Finkel, R., 1996. Spatially averaged long-term erosion rates measured from in situ-produced cosmogenic nuclides in alluvial sediment. The Journal of Geology 104, 249–257. https://doi.org/10.1086/629823

Kirchner, J.W., Finkel, R.C., Riebe, C.S., Granger, D.E., Clayton, J.L., King, J.G., Megahan, W.F., 2001. Mountain erosion over 10 yr, 10 k.y., and 10 m.y. time scales. Geology 29, 591–594. https://doi.org/10.1130/0091-7613(2001)029<0591:MEOYKY>2.0.CO;2

Reiners, P.W., Brandon, M.T., 2006. Using thermochronology to understand orogenic erosion. Annual Review of Earth and Planetary Sciences 34, 419–466. https://doi.org/10.1146/annurev.earth.34.031405.125202

von Blanckenburg, F., 2005. The control mechanisms of erosion and weathering at basin scale from cosmogenic nuclides in river sediment. Earth and Planetary Science Letters 237, 462–479. https://doi.org/10.1016/j.epsl.2005.06.030
