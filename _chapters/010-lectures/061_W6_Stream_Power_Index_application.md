---
title: W6 – Stream Power Incision Model – Applications
slug: week6-application-stream-power-incision-model
abstract:
---

### Lecture 2: Applying SPIM
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

The Stream Power Incision Model (SPIM) is widely used to understand and predict river incision rates in various geological settings. In this lecture, we will focus on how to apply SPIM to real-world catchments, derive model parameters from field data, and calibrate the model using known incision rates.


## Applying SPIM
To apply SPIM to real-world catchments, we need to derive the model parameters (K, m, n) from empirical data. The first step is to analyze slope–area relationships from digital elevation models (DEMs) of the catchment.

The slope–area relationship can be expressed as:
$$S = k_s A^{-\theta}$$
where \(k_s\) is the channel steepness index and \(\theta\) is the concavity index. By plotting slope (S) against drainage area (A) on a log-log scale, we can fit a linear regression to determine \(\theta\) (the negative slope of the line) and \(k_s\) (the intercept).

Once we have estimates for \(\theta\) and \(k_s\), we can relate them to the SPIM parameters \(m\) and \(n\). The ratio \(m/n\) is equal to \(\theta\), and we can choose typical values for \(m\) and \(n\) based on literature or field studies (e.g., \(m = 0.5\), \(n = 1\)).

Model calibration involves adjusting the erodibility coefficient \(K\) to match observed incision rates. This can be done by comparing modeled erosion rates from SPIM with measured incision rates from field data, such as river terrace elevations or cosmogenic nuclide dating.

Finally, it is important to test the sensitivity of the model to changes in parameters \(K\), \(m\), and \(n\). This helps to understand how uncertainties in these parameters can affect predicted incision rates. 






## Lecture 2: Using SPIM to Interpret and Predict Landscape Evolution

### 1. Introduction: From Explanation to Experiment (5 min)
- Chi showed us *what* the landscape is doing.
- SPIM explains *why*.
- Next step:
  > *Use SPIM to test hypotheses about tectonic forcing.*

---

### 2. Steady-State Solutions (20 min)

#### 2.1 Balance Between Uplift and Incision
- At steady state:
  - U = K A^m S^n everywhere along channel.
- Implications:
  - spatially uniform uplift produces systematic slope patterns.
  - rivers encode uplift in their geometry.

#### 2.2 Spatial Variations
- Changes in:
  - uplift rate,
  - erodibility,
  - base level
  produce predictable profile changes.
- SPIM allows forward prediction:
  - if U doubles, how must S respond?

---

### 3. Transient Scenarios (25 min)

#### 3.1 Uplift Rate Change
- Sudden increase in uplift:
  - produces steep reach near outlet,
  - knickpoint migrates upstream.
- Rate of migration depends on:
  - K,
  - drainage area,
  - channel slope.

#### 3.2 Base-Level Fall
- River responds similarly to uplift pulse.
- Explains:
  - postglacial incision,
  - river response to sea-level change.

---

### 4. Interpreting SPIM Outputs (20 min)

#### 4.1 What SPIM Can Tell Us
- Relative uplift patterns.
- Incision histories (qualitative).
- Expected profile shapes.

#### 4.2 What SPIM Cannot Tell Us
- Absolute uplift rates without calibration.
- Exact timing of events.
- Effects of complex sediment dynamics.

---

### 5. Linking SPIM to LEMs (15 min)

- SPIM is:
  - 1D along channels.
- Landscape evolution models:
  - extend SPIM across 2D surfaces,
  - couple with hillslopes and tectonics.
- Conceptual shift:
  > *From interpreting rivers to simulating landscapes.*

---

### 6. Wrap-up & Transition (10 min)

- Key takeaways:
  - SPIM explains chi patterns mechanistically.
  - Parameters have physical meaning tied to tectonics.
- Explicit transition:
  > *Next, we implement SPIM numerically to explore landscape evolution through time.*

---