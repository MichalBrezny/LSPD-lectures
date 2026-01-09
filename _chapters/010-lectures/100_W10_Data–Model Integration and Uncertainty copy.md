---
title: W10 – Data–Model Integration and Uncertainty
slug: week10-data-model-integration-uncertainty
abstract:
---
<!-- 
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

-->

### 1. Introduction: The Role of Data in Quantitative Geomorphology

- Recap of course narrative:
  - Tectonics provides forcing.
  - Rivers respond (chi, ksn).
  - SPIM explains mechanisms.
  - LEMs simulate evolution.
- Key realization:
  > *Models without data are unconstrained; data without models are hard to interpret.*
- Purpose of data–model integration at MSc level:
  - not prediction,
  - not optimization,
  - but **plausibility testing**.

---

### 2. Types of Data Used to Constrain Models

#### 2.1 Topographic Data (Primary Constraint)
- DEM-derived metrics:
  - river profiles,
  - chi plots,
  - slope distributions,
  - hypsometry.
- What topography constrains:
  - relative uplift patterns,
  - transient vs. steady-state behavior,
  - spatial variability.
- Strengths:
  - spatially continuous,
  - widely available.
- Limitations:
  - integrates long time periods,
  - non-unique interpretations.

---

### Erosion Rate Data
#### Cosmogenic nuclides (e.g. ¹⁰Be):
We can use concentrations of cosmogenic nuclides like ¹⁰Be in river sediments to estimate basin-averaged erosion rates over timescales of 10³–10⁵ years. These measurements provide direct constraints on how quickly landscapes are lowering, which can be compared to model predictions.



- Sediment yield measurements:
  - modern erosion proxies.
- What they constrain:
  - magnitude of incision/denudation.
- Key limitation:
  - represent specific timescales,
  - not directly comparable to short-term processes.

---

#### Uplift and Boundary Condition Data
- Geodetic uplift (GPS):
  - short-term rates.
- Geological proxies:
  - terraces,
  - marine markers,
  - thermochronology.
- Role in models:
  - define forcing, not outcome.

---

###  How Data Are Used in Models (Conceptually)

#### Calibration vs. Constraint
- **Calibration**:
  - adjusting parameters to fit data.
- **Constraint** (preferred at MSc level):
  - limiting plausible parameter ranges.

In this course, we focus on **constraint**, not calibration.
> Matching the data does **not** prove the model is correct.

---

#### Forward vs. Inverse Thinking
- Forward modeling:
  - assume forcing → predict landscape.
- Inverse reasoning:
  - observe landscape → infer forcing.
- Important warning:
  - inversion is inherently non-unique.

---

### Non-Uniqueness and Equifinality

Various parameter combinations can produce similar model outputs. This is known as **equifinality**. That is similar to multiple roads leading to the same destination, but the journey taken may differ significantly. Or as evolutionary biologists say, "convergent evolution"—different paths leading to similar forms (e.g., wings in bats and birds).

- Definition of equifinality:
  - multiple parameter sets → similar topography.
- Why equifinality is unavoidable:
  - unknown past climate,
  - spatially variable lithology,
  - incomplete boundary conditions.
- Consequence:
  > *Matching topography does not prove correctness.*

---

### Wrap-up 

- Key messages:
  - Data guide models, not validate them absolutely.
  - Agreement ≠ truth.
- Prepare students for:
  - sensitivity analysis,
  - uncertainty discussion.


