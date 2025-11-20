---
title: Week 3 – River Networks and Longitudinal Profiles
slug: Week3
abstract:
---


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


---
## Lecture 1: River Networks and Drainage Basins

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


Drainage density and bifurcation ratios.
**Drainage density** is a quantity used to describe physical parameters of a [drainage basin](https://en.wikipedia.org/wiki/Drainage_basin "Drainage basin"). First described by [Robert E. Horton](https://en.wikipedia.org/wiki/Robert_E._Horton "Robert E. Horton"), drainage density is defined as the total length of channel in a drainage basin divided by the total area.
![{\displaystyle D_{d}={\frac {\sum {L}}{A_{basin}}}.}](https://wikimedia.org/api/rest_v1/media/math/render/svg/c81f340109ab42d7fea6afb493e95c00b2ef5f8b)

The quantity represents the average length of channel per unit area of [catchment](https://en.wikipedia.org/wiki/Catchment "Catchment") and has units [L][L2]![{\displaystyle {\frac {\left[L\right]}{\left[L^{2}\right]}}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/153862de9928bcdc71663d8013c435afaa549463), which is often reduced to [L−1]![{\displaystyle \left[L^{-1}\right]}](https://wikimedia.org/api/rest_v1/media/math/render/svg/6726ab0af947d8cd3a9e0bed907cec0d07a6170d).

#### What affects drainage density?
Drainage density is influenced by climatic factors and physical properties of the drainage basin. Very important is also the time, as landscapes evolve and drainage networks develop over time. 

For example soil permeability (how easily water can infiltrate into soil) and underlying rock type affect the runoff in a watershed. Impermeable ground or exposed bedrock will lead to an increase in surface water runoff and therefore to more frequent streams. Rugged regions or those with high relief will also have a higher drainage density than other drainage basins if the other characteristics of the basin are the same.

#### Drainage density vs. maturity of landscape
Drainage density is often used as an indicator of the maturity of a landscape. Young landscapes, which are still actively eroding and developing, tend to have higher drainage densities due to the presence of numerous small streams and channels. As landscapes mature, erosion processes tend to smooth out the terrain, leading to a reduction in drainage density.

## Inverse of drainage density as a physical quantity

