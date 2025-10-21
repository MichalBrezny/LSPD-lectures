---
title: Week 5 – Stream Power Incision Model – Theory and Implementation
slug: Week5
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