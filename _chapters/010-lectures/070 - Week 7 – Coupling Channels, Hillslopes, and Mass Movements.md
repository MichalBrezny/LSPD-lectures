---
title: Week 7 – Coupling Channels, Hillslopes, and Mass Movements
slug: Week7
abstract:
---

### Lecture 1: Hillslope Diffusion
**Structure**
- **Introduction (5 min)**
  - Hillslopes as sediment suppliers feeding channels.
- **Core Concepts (25 min)**
  - Linear diffusion law: q = –D ∂z/∂x.
    - D = transport coefficient (soil creep, bioturbation, rainsplash).
  - Nonlinear diffusion at high slopes:
    - Slope-dependent flux.
    - Threshold slopes.
  - Hillslope–channel coupling:
    - Sediment supply controls channel incision.
    - Response times and lag effects.
- **Examples (10 min)**
  - Oregon Coast Range: soil-mantled hillslopes.
  - Taiwan: threshold slopes under monsoon rains.
- **Wrap-up (5 min)**
  - Q: How would deforestation change hillslope diffusion?

### Lecture 2: Mass Movements and Slope Stability
**Structure**
- **Introduction (5 min)**
  - Landslides as threshold-driven processes.
- **Core Concepts (25 min)**
  - Infinite slope model:
    - Factor of Safety (FoS) = resisting/driving forces.
    - Role of cohesion, internal friction, pore pressure.
  - Triggering mechanisms:
    - Rainfall, earthquakes, undercutting.
  - Sediment cascades and landscape evolution.
  - Mass wasting in models: stochastic landslide modules.
- **Examples (10 min)**
  - Vargas 1999 debris flows (Venezuela).
  - 2014 Oso landslide (USA).
- **Wrap-up (5 min)**
  - Quick exercise: Calculate FoS for given slope parameters.

### Lab 7: Coupled Hillslope–Channel Modelling
**Objectives**
- Add hillslope diffusion to Landlab SPIM.
- Explore slope stability analysis.

**Steps**
1. **Modify Landlab script** to include LinearDiffuser component.
2. **Run coupled hillslope–channel simulation**.
3. **Vary diffusion coefficient (D)** and observe system response.
4. **Slope stability exercise**:
   - Compute FoS for a synthetic hillslope.
   - Map landslide susceptibility in GIS.
5. **Exercise**
   - Compare sediment delivery with vs. without landslides.

---