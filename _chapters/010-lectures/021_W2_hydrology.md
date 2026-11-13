---
title: W2 – Terrain Metrics & Hydrology
slug: week2-terrain-metrics-hydrology
abstract:
---


# DEM and hydrology

Water is the main agent that moves sediment across most landscapes, so a large part of quantitative geomorphology starts with one question: *where does the water go?* A DEM lets us answer it for every cell of a landscape. The workflow has three steps, and each of them builds on the previous one:

1. **Hydrological conditioning** – removing depressions so that water can leave every cell.
2. **Flow routing** – deciding to which neighbour(s) each cell passes its water.
3. **Flow accumulation** – counting how much upstream area drains through each cell.

Drainage area, stream networks, watershed boundaries, longitudinal profiles and later also $\chi$ and channel steepness are all derived from these three steps. An error made here propagates into everything that follows.

## Hydrological conditioning: sinks and flats
A *sink* (pit, depression) is a cell or a group of cells surrounded by higher terrain. Water that enters a sink has no way out, and the flow path ends there. Some sinks are real (karst depressions, glacial kettles, endorheic basins), but in most DEMs the majority are artefacts of the limited resolution, of interpolation, of vegetation and of structures such as road embankments and bridges, which act as dams in the data.

Two main approaches are used to remove them:

- **Filling** raises the elevation of the cells in the depression to the level of its lowest outlet (pour point). It is simple and robust, but it produces perfectly flat areas in which the flow direction is undefined and has to be assigned artificially.
- **Breaching** (carving) cuts a narrow trench through the barrier that closes the depression. It changes fewer cells and is usually the better choice for artificial dams such as road embankments (Lindsay, 2016).

Modern tools often combine both approaches: they breach where the required cut is short and shallow and fill the rest.

> [!IMPORTANT]
> Conditioning changes the DEM. Use the conditioned DEM only to derive flow directions and compute slope, curvature and other terrain metrics from the original one. Before you remove all depressions, check whether some of them are real landforms.

## Flow routing
Flow routing is the process of determining the path that water takes as it moves across a landscape. For every cell of a DEM, a flow-routing algorithm decides which neighbouring cell or cells receive its water. The algorithms differ mainly in whether the flow from a cell may be split:

- **single flow direction (SFD)** algorithms pass all the flow to one neighbour (D8),
- **multiple flow direction (MFD)** algorithms divide the flow among several neighbours (D∞, MFD).

### D8 Algorithm
The simplest and most widely used method for flow routing is the D8 (deterministic eight-node) algorithm (O'Callaghan and Mark, 1984). Each cell directs all of its flow to the one of its eight neighbours that lies in the direction of the steepest descent. The steepness is the elevation drop divided by the distance between the cell centres, which is one cell size for the four cardinal neighbours and $\sqrt{2}$ times the cell size for the four diagonal ones.

{% include figure.html
  caption="D8 flow direction example (source: https://pro.arcgis.com/en/pro-app/3.4/tool-reference/spatial-analyst/how-flow-direction-works.html)"
  url="/figures/W2/d8.png"
  alt="D8 flow direction"
%}

Because every cell has exactly one receiver, D8 produces a tree-like network of flow paths that never split. This is a good description of channels, where flow is concentrated, and it makes D8 the standard choice for delineating watersheds and extracting stream networks and river profiles.

The limitation of D8 is that flow can go in only eight directions, in steps of 45°. On planar or divergent hillslopes this produces artificial parallel flow lines and cannot represent the spreading of water on ridges and fans.

### D∞ Algorithm
The D∞ (D-infinity) algorithm (Tarboton, 1997) removes the restriction to eight directions. The flow direction is a continuous angle between 0 and 360°, determined as the steepest downward slope on eight triangular facets formed between the cell and its neighbours. If the direction points exactly at a neighbouring cell, that cell receives all the flow. Otherwise the flow is divided between the two neighbours that bound the facet, in proportion to how close the flow direction is to each of them.

D∞ therefore gives smoother and more realistic patterns of contributing area on hillslopes than D8, while it keeps dispersion small.

### Multiple flow direction (MFD) algorithms
MFD algorithms (Freeman, 1991; Quinn et al., 1991) divide the flow from a cell among *all* of its lower neighbours, in proportion to the slope towards each of them. They represent divergent flow on convex hillslopes well, but they also spread the flow in valleys, where it should stay concentrated.

### Which algorithm to use?

| Algorithm | Receivers per cell | Strengths | Limitations | Typical use |
|---|---|---|---|---|
| D8 | 1 | simple, fast, unambiguous flow paths | only 8 directions, no divergence | stream networks, watersheds, river profiles |
| D∞ | 1–2 | continuous flow direction, little dispersion | more complex, flow paths can split | contributing area on hillslopes, wetness index |
| MFD | up to 8 | represents divergent flow | too much dispersion in valleys | hillslope hydrology, soil moisture |

As a rule of thumb, use D8 when you need a channel network and D∞ or MFD when you are interested in hillslopes. In this course we mostly work with river networks, so D8 will be our default.

## Flow accumulation
Flow accumulation quantifies the upstream area that contributes flow to each cell in the DEM. It is calculated by counting all the cells that drain through a given cell. Multiplied by the area of one cell it gives the **drainage area** (contributing area) $A$:

$$ A = N \cdot \Delta x^2 $$

where $N$ is the number of contributing cells and $\Delta x$ is the cell size. For example, a cell with a flow accumulation of 5,000 cells in a DEM with a 30 m resolution has a drainage area of $5000 \times 900\ \mathrm{m^2} = 4.5\ \mathrm{km^2}$.

High flow accumulation values indicate valley bottoms and stream channels. Low values correspond to hillslopes, and cells with zero accumulation lie on ridges and drainage divides.

{% include figure.html
  caption="Flow accumulation example (source: https://pro.arcgis.com/en/pro-app/3.5/tool-reference/spatial-analyst/how-flow-accumulation-works.html)"
  url="/figures/W2/flow_accumulation.png"
  alt="Flow accumulation"
%}

Drainage area is one of the most important variables in quantitative geomorphology, because it serves as a proxy for discharge. Discharge is rarely measured along a whole river, but it increases with drainage area, commonly approximated as a power law $Q \propto A^c$ with $c$ close to 1 where precipitation is uniform. We will rely on this substitution throughout the course: in slope–area analysis (W3), in the $\chi$ transformation (W5) and in the stream power incision model (W6).

## From flow accumulation to stream networks and watersheds

### Stream network extraction
A DEM does not tell us where channels begin. The most common solution is to define a **threshold drainage area**: every cell with a larger flow accumulation is classified as a channel.

The choice of the threshold controls the extent of the extracted network and therefore also the drainage density and stream orders (see W3). A low threshold places channels on hillslopes where no channels exist, while a high threshold misses real headwater streams. In reality, the area needed to maintain a channel head varies with climate, lithology, slope and vegetation, so a single threshold is always a simplification. Compare the extracted network with a map, an orthophoto or a high-resolution hillshade whenever possible.

### Watershed delineation
A watershed (drainage basin, catchment) is the set of all cells that drain to a chosen outlet, called the pour point. It is delineated by following the flow directions upstream from the outlet. The boundary of the watershed is the drainage divide.

In practice the outlet has to lie exactly on the cell with high flow accumulation. A gauging station or a GPS point is often located a few cells away from the modelled channel, and it must be moved ("snapped") to the channel first. Otherwise the result is a watershed of a few cells instead of a whole basin.

## Common pitfalls
- **Flat areas and filled depressions**: flow directions there are assigned by the algorithm and not by the topography. The resulting straight or parallel channels are artefacts.
- **DSM instead of DTM**: vegetation and buildings deflect the modelled flow paths.
- **Bridges, culverts and embankments**: they block the flow in the DEM, although water passes through them in reality. This matters mainly in high-resolution LiDAR data.
- **DEM edges**: a basin cut by the edge of the DEM has an underestimated drainage area. Always check that the DEM covers the whole basin.
- **Resolution**: a coarser DEM gives lower slopes and shorter, straighter channels. Results obtained from DEMs with different resolutions are not directly comparable.

## Summary
- Every DEM-based hydrological analysis consists of conditioning, flow routing and flow accumulation.
- D8 sends the flow to one neighbour and is suited to channels. D∞ and MFD divide the flow and are suited to hillslopes.
- Flow accumulation multiplied by the cell area gives the drainage area, which is used as a proxy for discharge.
- Stream networks are extracted with a drainage-area threshold and watersheds are delineated from a pour point. Both depend on the choices made by the analyst.

# References
Freeman, T.G., 1991. Calculating catchment area with divergent flow based on a regular grid. Computers & Geosciences 17, 413–422. https://doi.org/10.1016/0098-3004(91)90048-I

Lindsay, J.B., 2016. Efficient hybrid breaching-filling sink removal methods for flow path enforcement in digital elevation models. Hydrological Processes 30, 846–857. https://doi.org/10.1002/hyp.10648

O'Callaghan, J.F., Mark, D.M., 1984. The extraction of drainage networks from digital elevation data. Computer Vision, Graphics, and Image Processing 28, 323–344. https://doi.org/10.1016/S0734-189X(84)80011-0

Quinn, P., Beven, K., Chevallier, P., Planchon, O., 1991. The prediction of hillslope flow paths for distributed hydrological modelling using digital terrain models. Hydrological Processes 5, 59–79. https://doi.org/10.1002/hyp.3360050106

Tarboton, D.G., 1997. A new method for the determination of flow directions and upslope areas in grid digital elevation models. Water Resources Research 33, 309–319. https://doi.org/10.1029/96WR03137
