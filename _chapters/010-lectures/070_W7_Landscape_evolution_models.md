---
title: W7 – Landscape Evolution Models – Introduction
slug: week7-landscape-evolution-models-introduction
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
- **OpenLEM**: An open-source LEM that provides a platform for simulating landscape evolution under various environmental conditions. 

## Key Components of Numerical LEMs
Numerical LEMs typically consist of the following key components:
- **Grid Representation**: Landscapes are represented using grids (raster, hexagonal, or irregular meshes) that define the spatial resolution of the model.
  - These grids store eleation data, flow directions and accumulation, information about lithology etc.
- **Process Modules**: Mathematical representations of geomorphic processes such as erosion, sediment transport, and uplift.
  - Stream power erosin model, diffusion model, model of landsliding, glacial erosion etc.
- **Boundary Conditions**: Definitions of how the model interacts with its surroundings, such as fixed or open boundaries.
  - Fixed boundaries (e.g., base level) vs open boundaries (e.g., inflow/outflow).
- **Initial Conditions**: The starting state of the landscape, which can be a flat surface, a pre-existing topography, or a synthetic landscape.
- **Uplift and Forcing Functions**: Parameters that define tectonic uplift rates, climatic inputs, or other external forcings that drive landscape evolution.
- **Time Stepping**: Numerical methods to advance the simulation through time while ensuring stability (e.g., CFL condition).
- **Visualization Tools**: Methods for visualizing model outputs, including elevation grids, slope maps, and χ-plots.

## LANDLAB Overview
Landlab is an open-source, runs in Python, easy to use LEM framework that allows users to build and run landscape evolution models. It provides a modular approach, enabling users to combine different process components and customize their simulations. Landlab supports various grid types and includes built-in tools for flow routing, erosion modeling, and visualization.

## Example: Simple Landscape Evolution Model in Landlab
Here is a basic example of setting up and running a simple landscape evolution model using Landlab:
```python
from landlab import RasterModelGrid
from landlab.components import FlowAccumulator, StreamPowerEroder
from landlab.io import read_esri_ascii
import numpy as np

# Create a raster grid
mg = RasterModelGrid((100, 100), xy_spacing=10.0)

# Initialize elevation data with some random noise
initial_noise = 0.1 # You can adjust this value
elevation = mg.add_field('topographic__elevation', initial_noise * np.random.rand(mg.number_of_nodes), at='node')

# Add flow accumulator component
fa = FlowAccumulator(mg)

# Add stream power eroder component
spe = StreamPowerEroder(mg, K_sp=0.0001, m_sp=0.5, n_sp=1.0)

# Define uplift rate
uplift_rate = 0.001 # meters per timestep, adjust as needed

# Run the model for a specified number of time steps
for _ in range(1000):
    fa.run_one_step()
    spe.run_one_step(dt=1000)
    # Apply uplift to all nodes (or core nodes)
    mg.at_node['topographic__elevation'] += uplift_rate * 1.0 # dt is 1.0 from spe.run_one_step
```
---
<!-- Video embed https://youtu.be/jrpabwebOGY?si=hBEDRUOUI0LY4UwJ -->
{%include youtube.html id="si=hBEDRUOUI0LY4UwJ" title="Landlab - Overview"%}


