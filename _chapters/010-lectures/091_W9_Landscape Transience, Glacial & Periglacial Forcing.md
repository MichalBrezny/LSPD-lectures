---
title: W9 – Landscape Transience, Glacial & Periglacial Forcing 2
slug: week9-landscape-transience-glacial-periglacial-forcing2
abstract:
---
<!--

### Lecture 2: Glacial & Periglacial Processes
**Structure**
- **Introduction (5 min)**
  - Cold-region processes as strong forcings on topography.
- **Core Concepts (25 min)**
  - Glacial erosion laws:
    - Basal sliding.
    - Abrasion and quarrying.
  - Landforms:
    - U-shaped valleys, cirques, overdeepenings, fjords.
  - Periglacial processes:
    - Frost creep, solifluction, ice wedges, permafrost thaw.
  - Paraglacial sediment pulses:
    - Postglacial overloading of channels.
- **Examples (10 min)**
  - Patagonian fjords.
  - European Alps deglaciation.
- **Wrap-up (5 min)**
  - Compare glacial vs. fluvial incision efficiency.

### Lab 8: Glacial and Periglacial DEM Analysis
**Objectives**
- Identify glacial and periglacial signatures in DEMs.
- Compare glaciated vs. fluvial valley cross-sections.

**Steps**
1. **Load DEMs** from glaciated and non-glaciated basins.
2. **Extract valley cross-sections**.
3. **Calculate valley-shape indices** (V-shaped vs. U-shaped).
4. **Hypsometry of glaciated basins**.
5. **Landlab exercise**:
   - Simulate base-level fall to mimic deglaciation.
6. **Exercise**
   - Write interpretation of paraglacial adjustment.
-->

# Core concepts of glacial and periglacial processes
Glacial and periglacial processes play a significant role in shaping landscapes, particularly in cold regions. Glaciers erode the underlying bedrock through mechanisms such as basal sliding, abrasion, and quarrying, leading to distinctive landforms like U-shaped valleys, cirques, and fjords. Periglacial processes, which occur in areas adjacent to glaciers, include frost creep, solifluction, ice wedge formation, and permafrost thawing. These processes contribute to mass wasting and sediment transport in cold environments.

## Basal sliding




## Glacier modelling
### Glacier movement
Glacier movement can be modelled using equations that describe the flow of ice under stress. The most common approach is to use Glen's Flow Law, which relates the strain rate of ice to the applied stress:
$$ \dot{\epsilon} = A \tau^n $$
Where:  
- \( \dot{\epsilon} \) is the strain rate (deformation rate) of the ice.  
- \( A \) is a temperature-dependent rate factor (higher values at warmer temperatures).
- \( \tau \) is the shear stress acting on the ice.
- \( n \) is the flow law exponent, typically around 3 for glacier ice.

This equation indicates that ice deforms more rapidly under higher stress and at warmer temperatures. The flow of glaciers is also influenced by basal sliding, which occurs when the glacier slides over its bed due to meltwater lubrication or deformation of subglacial sediments.

### Glacier erosion
Glacier erosion can be modelled using empirical relationships that relate erosion rates to glacier velocity and basal shear stress. A common formulation is:
$$ E = k \tau^m V^p $$
Where:  
- \( E \) is the erosion rate (e.g., in mm/year).
- \( k \) is an empirical erosion coefficient.
- \( \tau \) is the basal shear stress.
- \( V \) is the basal sliding velocity of the glacier.
- \( m \) and \( p \) are empirical exponents that describe the sensitivity of erosion to shear stress and velocity, respectively.
This equation suggests that higher basal shear stress and faster glacier movement lead to increased erosion rates. The values of \( m \) and \( p \) can vary depending on the specific glacier and bedrock conditions.








# Paraglacial transience

Ballantyne (2002) defined paraglacial as "the suite of processes, landforms, and sedimentary deposits that result from the adjustment of Earth's surface to the removal of glacial ice." Following deglaciation, landscapes often experience a period of heightened geomorphic activity as they adjust to the new conditions. This adjustment can include increased rates of mass wasting, fluvial incision, and sediment transport.

Glaciation profoundly reshapes landscapes through processes such as abrasion and quarrying, leading to characteristic landforms like U-shaped valleys and fjords. The efficiency of glacial incision often exceeds that of fluvial processes, resulting in overdeepened valleys that can influence postglacial landscape evolution.


## References
- Ballantyne, C. K. (2002). Paraglacial geomorphology. Quaternary Science Reviews, 21(18-19), 1935-2017.