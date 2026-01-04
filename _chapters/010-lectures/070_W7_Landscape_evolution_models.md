---
title: W7 – Landscape Evolution Models – Introduction
slug: week7-landscape-evolution-models-introduction
abstract:
---

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

----

# Introduction to Landscape Evolution Models (LEMs)

## What is a Landscape Evolution Model?

Landscape Evolution Models (LEMs) are numerical tools that simulate the long-term evolution of topography under the influence of tectonic, climatic, and surface processes. They allow us to explore how landscapes respond to various forcings over geological timescales by implementing mathematical representations of physical processes such as erosion, sediment transport, and uplift.

## Why Use LEMs?
LEMs serve as a bridge between theoretical concepts and real-world observations. They help us to:
- Test hypotheses about landscape dynamics.
- Understand the interplay between different geomorphic processes.
- Predict future landscape changes under varying conditions.
- Explore transient responses to tectonic or climatic perturbations.
- Visualize complex interactions in a controlled environment.
- Identify key parameters that influence landscape evolution.
- Generate synthetic datasets for comparison with field data.
- Facilitate learning and teaching of geomorphic principles.
- And more!
However, it is important to recognize the limitations of LEMs, including simplifications of complex processes, uncertainties in parameter values, and computational constraints.

## Types of Models
LEMs can be broadly categorized into three types:
1. **Conceptual Models**: Simplified representations using block diagrams or flowcharts to illustrate processes and interactions.
2. **Physical Models**: Laboratory experiments (e.g., flume studies) that replicate landscape processes at a smaller scale.
3. **Numerical Models**: Computer simulations that implement mathematical equations to represent landscape processes over time. Examples include Landlab, CHILD, and others.

## Numerical landscape evolution models - an overview

There are several numerical landscape evolution models (LEMs) available, each with its own strengths and applications. Some popular LEMs include:
- **Landlab**: An open-source Python library that provides a flexible framework for building and running LEMs. It includes components for various geomorphic processes and supports grid-based landscape representations.
- **CHILD (Channel-Hillslope Integrated Landscape Development)**: A widely used LEM that simulates fluvial and hillslope processes, allowing for the study of landscape evolution under different tectonic and climatic conditions.
- **SIBERIA**: A LEM that focuses on simulating sediment transport and landscape evolution in response to tectonic uplift and climatic changes.
- **CASCADE**: A LEM that integrates fluvial and hillslope processes to study landscape evolution in response to tectonic and climatic forcings.
- **Delft3D**: A hydrodynamic and morphodynamic model that can simulate coastal and riverine landscape evolution.
- **TopoFlow**: A LEM that focuses on simulating surface water flow and sediment transport in landscapes.
- **iSOSIA**: A LEM that simulates landscape evolution by integrating fluvial, hillslope, and glacial processes.
- **TopoToolbox LEM** (TTLEM): A MATLAB-based LEM that allows for the simulation of landscape evolution using digital elevation models (DEMs).



