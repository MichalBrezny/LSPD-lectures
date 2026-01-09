---
title: W2 – Terrain Metrics & Hydrology
slug: week2-terrain-metrics-hydrology
abstract:
---

<!--
### Lecture 2: Terrain Metrics & Hydrology
**Structure**
- **Introduction (5 min)**
  - DEM derivatives connect topography to processes.
- **Slope and Aspect (10 min)**
  - Definitions: first derivatives of elevation.
  - Importance for soil erosion, solar radiation, hydrology.
- **Curvature (10 min)**
  - Profile curvature: flow acceleration/retardation.
  - Planform curvature: convergence/divergence of flow.
- **Hypsometry (10 min)**
  - Hypsometric curve: cumulative area vs. elevation.
  - Hypsometric integral: youthful vs. mature basins.
- **Hydrological Indices (15 min)**
  - Topographic Wetness Index (TWI = ln(a / tanβ)).
  - Stream Power Index (SPI = a·tanβ).
  - Interpretation for soil moisture, flood risk.
- **Runoff Processes (10 min)**
  - Hortonian (infiltration excess).
  - Dunne (saturation excess).
  - Hydrograph: rising limb, peak, recession.
- **Wrap-up (5 min)**
  - Discuss: How does land cover affect hydrograph form?
-->

<!--
### Lab 2: Terrain Metrics and Runoff Modelling
**Objectives**
- Extract key terrain metrics from DEMs.
- Link terrain to hydrological processes.

**Steps**
1. **Load DEM** in QGIS or SAGA.
2. **Derive terrain attributes**
   - Slope, aspect, curvature.
   - TWI and SPI.
   - Hypsometric curve for selected basins.
3. **Compare metrics across basins**
   - Different lithologies and elevations.
4. **Run rainfall–runoff model (Excel/Python)**
   - Horton infiltration curve.
   - Produce hydrographs for two soils.
5. **Exercise**
   - Write 2-page lab report:
     - Compare hydrographs between sandy vs. clay catchments.
     - Relate results to DEM-derived wetness indices.
-->
---

# DEM and hydrology

## Flow routing
Flow routing is the process of determining the path that water takes as it moves across a landscape. Using a DEM, we can calculate flow direction and accumulation, which are essential for understanding watershed boundaries and stream networks. Common algorithms for flow routing include D8 (deterministic eight-node) and D∞ (infinite directions).

### D8 Algorithm
The simplest and most widely used method for flow routing is the D8 algorithm. In this method, each cell in the DEM directs flow to one of its eight neighboring cells (the one with the steepest descent). This creates a network of flow paths that can be used to delineate watersheds and identify stream channels.

{% include figure.html
  caption="D8 flow direction example (source: https://pro.arcgis.com/en/pro-app/3.4/tool-reference/spatial-analyst/how-flow-direction-works.htm)"
  url="/figures/W2/D8.gif"
  alt="D8 flow direction"
  %}


### D∞ Algorithm
The D∞ algorithm allows for flow to be distributed among multiple neighboring cells based on the slope gradients. This method provides a more realistic representation of flow paths, especially in complex terrains where water may not follow a single direction.


## Flow accumulation
Flow accumulation quantifies the amount of upstream area that contributes flow to each cell in the DEM. It is calculated by summing the number of cells that flow into each cell, providing insight into potential stream channels and watershed characteristics. High flow accumulation values typically indicate stream channels, while low values correspond to hillslopes.

{% include figure.html
  caption="Flow accumulation example (source: https://pro.arcgis.com/en/pro-app/3.5/tool-reference/spatial-analyst/how-flow-accumulation-works.htm)"
  url="/figures/W2/flow_accumulation.png"
  alt="Flow accumulation"
 %}



