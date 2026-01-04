---
title: W3 – River Networks
slug: week3-river-networks
abstract:
---

<!-- 
## Overview

**Lecture 1: River Network Geometry**
- Drainage basin organization: Horton–Strahler ordering.
- Drainage density and bifurcation ratios.
- Slope–area relationships and scaling laws.
- Fractal properties and self-similarity of drainage networks.

**Lecture 2: Longitudinal River Profiles**
- Concept of graded stream and equilibrium profile.
- Processes of knickpoint formation and migration.
- Influence of tectonics, base-level changes, dams.
- Longitudinal profiles as archives of landscape history.

**Lab**
- Extract drainage networks from DEM.
- Calculate stream orders, slope–area relationships.
- Generate longitudinal profiles.
- Identify and classify knickpoints (tectonic vs. lithologic).

-->
---
## River Networks and Drainage Basins

### River Networks
River networks are hierarchical structures that efficiently channel water and sediment from upland areas to downstream sinks. Geometry of river networks reflects the underlying landscape processes, geology, and controls hydrological and sediment transport dynamics.

#### Basic geometric patterns
There are several types of river network patterns, including:
- Dendritic: tree-like branching, common in homogeneous substrates.
- Trellis: parallel main streams with short tributaries, typical in folded terrains.
- Radial: streams radiate outward from a central high point, such as a volcano.
- Rectangular: channels follow jointed or faulted bedrock, creating right-angle bends.
- Deranged: irregular patterns with no clear organization, often found in recently glaciated landscapes.
- Parallel: streams run parallel to each other, often found in areas with uniform slope.

<!-- upravit a doplnit obrazek -->

#### Key geometric properties
River networks can be characterized by several key geometric properties that describe their structure and organization. These include:

- **Stream Length**: The total length of all streams in a network.
- **Stream Density**: The total length of streams divided by the area of the drainage basin.
- **Bifurcation Ratio**: The ratio of the number of streams of one order to the number of streams of the next higher order.
- **Stream Length Ratio**: The ratio of the average lengths of streams of one order to the average lengths of streams of the next higher order.
- **Stream Slope**: The average slope of streams within a network, which can influence flow velocity and sediment transport.
- **Stream Order**: A method of classifying the hierarchy of streams.
- **Bifurcation Ratio**: The ratio of the number of streams of one order to the number of streams of the next higher order.
- **Drainage Density**: The total length of all streams divided by the area of the drainage basin.
- **Fractal Properties**: River networks often exhibit self-similarity and fractal characteristics.

#### Stream Order
Stream order is a hierarchical classification system for streams within a river network. The most commonly used method is the Strahler method, however other methods such as Shreve and Horton also exist. Their principles are as follows:

- **Strahler Method**: Assigns order based on the highest order of tributaries. For example, if a second-order stream receives a first-order tributary, it remains a second-order stream.
- **Shreve Method**: Assigns order based on the total number of upstream tributaries. Each stream segment is assigned a value of 1, and the values are summed at confluences.
- **Horton Method**: Focuses on the length of streams, with higher-order streams being longer on average than lower-order streams.

### Drainage Basins
Drainage basins are elementary units of the landscape, and their organization is crucial for understanding hydrological processes. Key concepts include:

- **Basin Morphology**: The shape and structure of a drainage basin, including its length, width, and slope.
- **Hydrological Connectivity**: The degree to which different parts of the basin are connected by the river network.
- **Land Use and Land Cover**: The impact of human activities and natural vegetation on the hydrology of the basin.
- **Sediment Transport**: The movement of sediment through the river network and its implications for basin evolution.


### Drainage density and bifurcation ratios.
Drainage density is the total length of mapped channels within a basin divided by the basin area:
$$ D_d = \frac{\sum L}{A_{basin}} $$
where:
- \( D_d \) = drainage density (L^-1)
- \( \sum L \) = total length of all streams in the basin (L)
- \( A_{basin} \) = area of the drainage basin (L^2)    
  
It expresses average channel length per unit area (e.g., km km^-2 or m m^-2, often reported simply as km^-1 or m^-1). Higher values indicate more closely spaced channels (greater dissection); lower values indicate more widely spaced channels (less dissection).

Drainage density is refers to a average spacing of channels in a drainage basin. It is inversely related to the average distance water must travel overland before reaching a channel ($\overline{L} \sim 1/2D_d$). Further the drainage density is related to the valley density (length of valleys per unit area) as valleys typically host channels.

#### What affects drainage density?
Drainage density is influenced by climatic factors, physical properties of the drainage basin, rock and soil properties, relief, vegetation. Very important is also the time, as landscapes evolve and drainage networks develop over time. 

For example soil permeability (how easily water can infiltrate into soil) and underlying rock type affect the runoff in a watershed. Impermeable ground or exposed bedrock will lead to an increase in surface water runoff and therefore to more frequent streams. Rugged regions or those with high relief will also have a higher drainage density than other drainage basins if the other characteristics of the basin are the same.

#### Drainage density vs. maturity of landscape
Drainage density is often used as an indicator of the maturity of a landscape. Young landscapes, which are still actively eroding and developing, tend to have higher drainage densities due to the presence of numerous small streams and channels. As landscapes mature, erosion processes tend to smooth out the terrain, leading to a reduction in drainage density.

## Inverse of drainage density as a physical quantity


# References
Horton, R.E., 1945. Erosional Development of Streams and Their Drainage Basins; Hydrophysical Approach to Quantitative Morphology. Geol Soc America Bull 56, 275. https://doi.org/10.1130/0016-7606(1945)56%255B275:EDOSAT%255D2.0.CO;2

Tucker, G.E., Catani, F., Rinaldo, A., Bras, R.L., 2001. Statistical analysis of drainage density from digital terrain data. Geomorphology 36, 187–202. https://doi.org/10.1016/S0169-555X(00)00056-8
