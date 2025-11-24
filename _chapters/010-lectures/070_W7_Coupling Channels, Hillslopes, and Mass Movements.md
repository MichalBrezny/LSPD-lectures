---
title: Week 7 – Coupling Channels, Hillslopes, and Mass Movements
slug: Week7
abstract:
---
<!--
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

-->
In this week, we will explore how hillslopes and channels interact to shape landscapes. We will cover hillslope diffusion processes that transport sediment downslope and how mass movements like landslides contribute to sediment flux. Understanding these coupled processes is crucial for modeling landscape evolution accurately.

### Hillslope diffusion processes
Hillslope diffusion describes the gradual movement of soil and sediment down a slope due to processes like soil creep, bioturbation, and rainsplash. The simplest model for hillslope diffusion is the linear diffusion equation:
$$ q = -D \frac{\partial z}{\partial x} $$
where:
- \( q \) = sediment flux (L^2/T)
- \( D \) = diffusion coefficient (L^2/T)     
- \( \frac{\partial z}{\partial x} \) = slope gradient (dimensionless)
- L = length, T = time
This equation states that sediment flux is proportional to the local slope gradient, with the diffusion coefficient \( D \) controlling the efficiency of sediment transport. On steep slopes, nonlinear diffusion models may be more appropriate, accounting for threshold slopes beyond which sediment transport increases rapidly.
### Mass movements and slope stability
Mass movements, such as landslides and debris flows, are rapid downslope movements of soil and rock that occur when the driving forces exceed the resisting forces on a slope. The infinite slope model is commonly used to assess slope stability, calculating the Factor of Safety (FoS) as:
$$ FoS = \frac{c + (\sigma - u) \tan \phi}{\tau} $$
where:
- \( c \) = cohesion of the soil (force per unit area)
- \( \sigma \) = normal stress on the failure plane (force per unit area)
- \( u \) = pore water pressure (force per unit area)
- \( \phi \) = internal friction angle (degrees)
- \( \tau \) = shear stress driving the movement (force per unit area)

If \( FoS > 1 \), the slope is stable; if \( FoS < 1 \), failure is likely. Triggering mechanisms for mass movements include intense rainfall, earthquakes, and undercutting by rivers. Mass wasting plays a significant role in landscape evolution by rapidly delivering sediment to channels, influencing erosion rates and topographic development.

In landscape evolution models, stochastic landslide modules can be incorporated to simulate the effects of mass movements on sediment flux and topography over time.

