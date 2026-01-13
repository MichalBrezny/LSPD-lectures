---
title: W3 – Longitudinal Profiles
slug: week3-longitudinal-profiles
abstract:
---

# River profile as a record of landscape evolution

Rivers are dynamic system which react on the external forcings like tectonics, climate or base-level changes. Longitudinal river profiles (elevation vs. downstream distance) can therefore provide important insights into the history of landscape evolution.

# Concept of graded stream and equilibrium profile
The concept of graded stream was introduced by Gilbert (1877) and further developed by Mackin (1948). A graded stream is one that has achieved a balance between sediment supply and transport capacity, resulting in a stable longitudinal profile. In this state, the river neither aggrades nor degrades its bed over time. The equilibrium profile is typically concave-upward, reflecting the decreasing slope with increasing downstream distance. This concavity arises because steeper slopes are required in the upper reaches to provide sufficient energy for sediment transport, while gentler slopes in the lower reaches accommodate the reduced energy available as the river approaches its base level.

## Slope-area relationships
Slope-area relationships describe how channel slope (S) varies with drainage area (A).  Generally slope is proportional to drainage area raised to some negative exponent:
$$ S ∝ A^{-\theta} $$

This relationship reflects the balance between sediment transport capacity and sediment supply. The concavity index (θ) provides insights into the geomorphic processes shaping the river profile, with higher values indicating steeper profiles and potentially more active tectonic or climatic forcing.

## Knickpoints and knickzones
Knickpoints are abrupt changes in channel slope, often manifesting as waterfalls or rapids. They can form due to various factors, including tectonic uplift, lithologic boundaries, or base-level fall. Knickpoints can migrate upstream over time through processes such as vertical incision or upstream migration, leading to the adjustment of the river profile towards a new equilibrium state. 

{% include figure.html
    caption="Niagara Falls, a classic example of a knickpoint. (By Quistnix - Own work, CC BY-SA 3.0, https://commons.wikimedia.org/w/index.php?curid=185)"
    url="/figures/W3/Niagara_watervallen_canada.jpg"
    class="row"
%}

### Influences on longitudinal profiles
- **Tectonics**: Uplift can create knickpoints and steepen profiles.
- **Base-level changes**: Sea-level fall or lake level drop can induce incision.
- **Dams**: Artificial structures can create local base-level changes, leading to upstream aggradation and downstream incision.
- **Climate**: Changes in precipitation and temperature can affect erosion and sediment transport.

<!-- Fiona Clubb https://www.youtube.com/watch?v=zPFLuPouSLk -->
{% include youtube.html id="zPFLuPouSLk" %}


<!--
---

### Lab 3: River Profiles and Drainage Metrics
**Objectives**
- Learn how to extract and analyze drainage networks.
- Practice slope–area and profile analysis.

**Steps**
1. **DEM preparation**: preprocess with pit filling.
2. **Extract drainage network** with threshold contributing area.
3. **Calculate stream orders** (Strahler).
4. **Generate slope–area plots**.
5. **Extract longitudinal profiles** for 2–3 rivers.
6. **Identify knickpoints** and classify causes.
7. **Exercise**
   - Compare concavity index (θ) for tectonically active vs. stable basins.

-->

