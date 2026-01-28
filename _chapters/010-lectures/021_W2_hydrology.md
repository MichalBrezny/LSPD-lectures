---
title: W2 – Terrain Metrics & Hydrology
slug: week2-terrain-metrics-hydrology
abstract:
---


# DEM and hydrology

## Flow routing
Flow routing is the process of determining the path that water takes as it moves across a landscape. Using a DEM, we can calculate flow direction and accumulation, which are essential for understanding watershed boundaries and stream networks. Common algorithms for flow routing include D8 (deterministic eight-node) and D∞ (infinite directions).

### D8 Algorithm
The simplest and most widely used method for flow routing is the D8 algorithm. In this method, each cell in the DEM directs flow to one of its eight neighboring cells (the one with the steepest descent). This creates a network of flow paths that can be used to delineate watersheds and identify stream channels.

{% include figure.html
  caption="D8 flow direction example (source: https://pro.arcgis.com/en/pro-app/3.4/tool-reference/spatial-analyst/how-flow-direction-works.html)"
  url="/figures/W2/d8.png"
  alt="D8 flow direction"
%}


### D∞ Algorithm
The D∞ algorithm allows for flow to be distributed among multiple neighboring cells based on the slope gradients. This method provides a more realistic representation of flow paths, especially in complex terrains where water may not follow a single direction.

## Flow accumulation
Flow accumulation quantifies the amount of upstream area that contributes flow to each cell in the DEM. It is calculated by summing the number of cells that flow into each cell, providing insight into potential stream channels and watershed characteristics. High flow accumulation values typically indicate stream channels, while low values correspond to hillslopes.

{% include figure.html
  caption="Flow accumulation example (source: https://pro.arcgis.com/en/pro-app/3.5/tool-reference/spatial-analyst/how-flow-accumulation-works.html)"
  url="/figures/W2/flow_accumulation.png"
  alt="Flow accumulation"
%}



