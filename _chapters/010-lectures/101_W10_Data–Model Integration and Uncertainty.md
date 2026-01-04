---
title: W10 – Data–Model Integration and Uncertainty
slug: week10-data-model-integration-uncertainty
abstract:
---
## Week 10 – Data–Model Integration and Uncertainty
### Lecture 1: Calibration Data
**Structure**
- **Introduction (5 min)**
  - Models are only as good as their calibration.
- **Core Concepts (25 min)**
  - Erosion rate measurements:
    - Cosmogenic nuclides (10Be, 26Al).
    - Sediment yield gauging.
  - Uplift rate estimates:
    - GPS geodesy.
    - Thermochronology.
  - Glacial proxies:
    - Lake sediment cores.
    - Trimline mapping.
  - DEM benchmarks for morphology.
- **Examples (10 min)**
  - Andes: cosmogenic rates vs. modeled incision.
- **Wrap-up (5 min)**
  - Q: Which dataset is most robust at different timescales?

### Lecture 2: Uncertainty and Equifinality
**Structure**
- **Introduction (5 min)**
  - Why uncertainty matters in scientific interpretation.
- **Core Concepts (25 min)**
  - Sensitivity analysis: one-at-a-time vs. Monte Carlo.
  - Equifinality: multiple parameter sets produce same output.
  - Uncertainty propagation through LEMs.
  - Reporting uncertainty in publications.
- **Examples (10 min)**
  - Landlab SPIM runs with varied K.
- **Wrap-up (5 min)**
  - Brainstorm: list 3 main sources of uncertainty in geomorphic models.

### Lab 9: Calibration and Sensitivity Testing
**Objectives**
- Integrate empirical data into models.
- Practice sensitivity analysis.

**Steps**
1. **Assign erosion rates** (field data provided).
2. **Run Landlab SPIM** with fixed vs. variable K.
3. **Perform sensitivity runs** (vary m, n, U).
4. **Visualize uncertainty** with ensemble outputs.
5. **Exercise**
   - Short written reflection: limits of calibration.