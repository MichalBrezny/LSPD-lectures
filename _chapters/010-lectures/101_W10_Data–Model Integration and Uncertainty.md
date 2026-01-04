---
title: W10 – Data–Model Integration and Uncertainty 2
slug: week10-data-model-integration-uncertainty2
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

# Embracing Uncertainty
In quantitative geomorphology, we use **models** to explore how landscapes might respond to tectonic forcing, climate, and surface processes. We use **data** to constrain what is physically plausible.  

Neither models nor data alone can fully explain landscape evolution:

- **Models without data** are unconstrained and speculative.
- **Data without models** are difficult to interpret mechanistically.

> **Key idea:** Models help us *ask better questions*, not provide final answers.

Scientific models are tools, not answers.

>[!Warning]
>Classic motto: Garbage in, garbage out. Models are only as good as the data and assumptions that go into them. >Understanding and quantifying uncertainty is crucial for responsible interpretation.

---

## Calibration vs. Constraint

- **Calibration**: tuning model parameters to match data exactly  
- **Constraint**: limiting parameter values to a plausible range  

In this course, we focus on **constraint**, not calibration.

> Matching the data does **not** prove the model is correct.

---

In this course, models are primarily constrained by:

- **Topographic data**
  - River profiles, chi plots, slope patterns, hypsometry
  - Provide spatially continuous information
- **Erosion-rate estimates**
  - Cosmogenic nuclides or sediment yields
  - Constrain the *magnitude* of incision
- **Boundary-condition data**
  - Uplift rates, base-level history, fault locations
  - Define *forcing*, not model outcomes

Each data type represents **different timescales** and contains uncertainty. These uncertainties propagate through models and affect interpretations.

---

## Sensitivity Analysis

### What Is Sensitivity?
- Response of model output to parameter changes.
- Key SPIM/LEM parameters:
  - uplift rate (U),
  - erodibility (K),
  - concavity (m/n),
  - diffusion coefficient (D).

Understanding sensitivity helps identify which parameters most influence model behavior and where to focus data collection efforts. For example if subtle changes in $K$ lead to large changes in incision rates, then accurate estimation of $K$ is critical.

## How to Perform Sensitivity Analysis?

### One-At-a-Time Sensitivity
- Change one parameter while others fixed.
- Observe:
  - incision depth,
  - profile shape,
  - transient response time.
- Emphasis:
  - patterns, not exact values.

### Monte Carlo Simulations
- Randomly sample parameter space.
- Generate ensemble of model runs.
- Analyze distribution of outputs.
- Benefits:
  - captures interactions between parameters,
  - quantifies uncertainty ranges.
  - Identifies equifinality (multiple parameter sets yield similar results).
  - Helps assess robustness of interpretations.
  - Visualize uncertainty with confidence intervals or probability density functions.
  

---

## Sources of Uncertainty

### Data Uncertainty
DEM errors:
- resolution,
- vegetation bias.

For details see previous lectures on DEM processing.

Measurement uncertainty:
  - cosmogenic inheritance,
  - sediment yield variability.

---

### Model Structural Uncertainty
- Simplified physics:
  - SPIM assumptions,
  - absence of sediment cover.
- Scale mismatch:
  - model grid vs. real landscape.

---

### Conceptual Uncertainty
- Incorrect process dominance.
- Over-interpreting metrics.
- Assuming steady state where none exists.

---

### 4. Interpreting Model–Data Agreement 

- Good agreement may indicate:
  - plausible forcing,
  - reasonable parameter choices.
- Poor agreement may indicate:
  - missing processes,
  - wrong boundary conditions,
  - transient landscape.
- Important message:
  > *Disagreement is informative, not failure.*

---

### 5. Best Practices for MSc-Level Interpretation

- Always ask:
  - What assumptions matter most?
  - Which parameters dominate outcomes?
  - Are alternative explanations possible?
- Prefer:
  - qualitative patterns,
  - spatial coherence,
  - consistency across metrics.

---

### 6. Wrap-up & Transition to Applications (10 min)

- Key takeaways:
  - Models explore hypotheses, not reality.
  - Data limit but do not determine solutions.
- Transition:
  > *Next, we explore how these tools are applied in real-world and research contexts.*

---