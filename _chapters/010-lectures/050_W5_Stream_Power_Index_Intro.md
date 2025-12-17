---
title: W5 – Stream Power Incision Model – Theory and Implementation
slug: week5-stream-power-incision-model
abstract:
---

### Lecture 1: Fundamentals of SPIM
**Structure**
- **Introduction (5 min)**
  - Fluvial incision as dominant erosional process in most landscapes.
- **Core Concepts (25 min)**
  - Governing equation: E = K A^m S^n.
    - K: erodibility (climate, lithology).
    - m, n: scaling exponents.
  - Detachment-limited vs. transport-limited frameworks.
  - Thresholds: critical shear stress τc.
  - Limitations of SPIM: assumption of steady discharge scaling.
- **Examples (10 min)**
  - Arid basin: episodic incision.
  - Humid basin: continuous transport.
- **Wrap-up (5–10 min)**
  - Q: What happens if m/n ratio is wrong?

### Lecture 2: Applying SPIM
**Structure**
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

---

# Fluvial incision

Fluvial incision is a dominant erosion process in many landscapes. The Stream Power Incision Model (SPIM) provides a framework to quantify how rivers erode their beds based on drainage area and channel slope. In this lecture, we will explore the theoretical underpinnings of SPIM, its assumptions, and how to implement it using real-world data.

## Fundamentals of SPIM

Stream power incision model (SPIM) is based on the idea that the rate of river incision (E) is proportional to the stream power per unit bed area, which can be expressed as:
$$E = KA^mS^n$$

Where:
- E = incision rate (m/yr)
- K = erodibility coefficient (depends on climate, lithology)
- A = drainage area (m²)
- S = channel slope (dimensionless)
- m, n = empirical exponents that describe how incision scales with area and slope

This is the simplest but still widely used model for fluvial incision. Parameter $K$ incorporates factors like climate and lithology that affect how easily a river can erode its bed. The exponents $m$ and $n$ are typically determined empirically, often through regression analysis of slope-area data from river networks. These parameters, though thought to be constants, can vary in space and time depending on environmental conditions. Different erodibility values can be during glacial vs. interglacial periods or in different lithologies.


