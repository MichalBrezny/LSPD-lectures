---
title: Week 6 – SPIM in Landlab – Basic Modelling
slug: Week6
abstract:
---
<!--
### Lecture 1: Introduction to LEMs
**Structure**
- **Introduction (5 min)**
  - Why use numerical models? Bridging theory and reality.
- **Core Concepts (25 min)**
  - Types of models:
    - Conceptual (block diagrams).
    - Physical (flume experiments).
    - Numerical (Landlab, CHILD).
  - Model grids: raster vs. hexagonal vs. irregular meshes.
  - Numerical stability:
    - CFL condition (Δt < Δx / v).
  - Advantages: exploring transient processes.
  - Limitations: simplifications, parameter uncertainty.
- **Examples (10 min)**
  - Diffusion equation demonstration on simple hillslope.
- **Wrap-up (5–10 min)**
  - Quick quiz: Match model type to research question.

### Lecture 2: Implementing SPIM in Landlab
**Structure**
- **Introduction (5 min)**
  - From equations to simulation.
- **Core Concepts (25 min)**
  - Flow routing algorithms (D8, D∞, Fastscape).
  - Stream Power component: setup, parameters.
  - Boundary conditions: fixed vs. open.
  - Spin-up period to achieve equilibrium.
  - Visualization: elevation grids, slope maps, χ-plots.
- **Examples (10 min)**
  - Demo: small synthetic basin with uplift rate applied.
- **Wrap-up (5–10 min)**
  - Discussion: what outputs should we focus on in LEM experiments?

### Lab 6: Basic SPIM Modelling in Landlab
**Objectives**
- Learn Landlab basics and run SPIM simulations.

**Steps**
1. **Set up Python notebook** with Landlab.
2. **Initialize grid** (raster) and assign uplift rate.
3. **Add FlowAccumulator** and **StreamPowerEroder**.
4. **Run simulation** for 10^4–10^6 years.
5. **Visualize outputs**: topography maps, χ plots.
6. **Experiment with parameter changes** (K, m, n).
7. **Checkpoint (graded 10%)**
   - Submit 2–3 page project proposal:
     - Dataset to be used.
     - Research question.
     - Planned methods and expected challenges.
-->