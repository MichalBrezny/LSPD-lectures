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
## Lecture 1: River Network Geometry
- Drainage basin organization: Strahler (Horton–Strahler) ordering.

![[Pasted image 20250916104413.png]]

- Drainage density and bifurcation ratios.
**Drainage density** is a quantity used to describe physical parameters of a [drainage basin](https://en.wikipedia.org/wiki/Drainage_basin "Drainage basin"). First described by [Robert E. Horton](https://en.wikipedia.org/wiki/Robert_E._Horton "Robert E. Horton"), drainage density is defined as the total length of channel in a drainage basin divided by the total area.
![{\displaystyle D_{d}={\frac {\sum {L}}{A_{basin}}}.}](https://wikimedia.org/api/rest_v1/media/math/render/svg/c81f340109ab42d7fea6afb493e95c00b2ef5f8b)

The quantity represents the average length of channel per unit area of [catchment](https://en.wikipedia.org/wiki/Catchment "Catchment") and has units [L][L2]![{\displaystyle {\frac {\left[L\right]}{\left[L^{2}\right]}}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/153862de9928bcdc71663d8013c435afaa549463), which is often reduced to [L−1]![{\displaystyle \left[L^{-1}\right]}](https://wikimedia.org/api/rest_v1/media/math/render/svg/6726ab0af947d8cd3a9e0bed907cec0d07a6170d).

#### What affects drainage density?
It depends upon both [climate](https://en.wikipedia.org/wiki/Climate "Climate") and physical characteristics of the drainage basin. Soil [permeability (infiltration difficulty)](https://en.wikipedia.org/wiki/Permeability_\(earth_sciences\) "Permeability (earth sciences)") and underlying rock type affect the runoff in a watershed; [impermeable](https://en.wikipedia.org/wiki/Permeability_\(earth_sciences\) "Permeability (earth sciences)") ground or exposed [bedrock](https://en.wikipedia.org/wiki/Bedrock "Bedrock") will lead to an increase in [surface water runoff](https://en.wikipedia.org/wiki/Surface_runoff "Surface runoff") and therefore to more frequent streams. Rugged regions or those with high [relief](https://en.wikipedia.org/wiki/Terrain#Relief "Terrain") will also have a higher drainage density than other drainage basins if the other characteristics of the basin are the same.

When determining the total length of [streams](https://en.wikipedia.org/wiki/Stream "Stream") in a basin, both [perennial](https://en.wikipedia.org/wiki/Perennial_stream "Perennial stream") and [ephemeral streams](https://en.wikipedia.org/wiki/Ephemeral_stream "Ephemeral stream") should be considered.[[2]](https://en.wikipedia.org/wiki/Drainage_density#cite_note-Horton1945-2) If a drainage basin contained only ephemeral streams, then the drainage density by the equation above would be calculated to be zero if the total length of streams was calculated using only perennial streams. Ignoring ephemeral streams in the calculations does not consider the behavior of the basin during flood events and is therefore not completely representative of the drainage characteristics of the basin.

Drainage density is indicative of [infiltration](https://en.wikipedia.org/wiki/Infiltration_\(hydrology\) "Infiltration (hydrology)") and [permeability](https://en.wikipedia.org/wiki/Hydraulic_permeability "Hydraulic permeability") of a drainage basin, and relates to the shape of the [hydrograph](https://en.wikipedia.org/wiki/Hydrograph "Hydrograph"). Drainage density depends upon both [climate](https://en.wikipedia.org/wiki/Climate "Climate") and physical characteristics of the drainage basin.

#### Drainage density vs. maturity of landscape




High drainage densities also mean a high [bifurcation ratio](https://en.wikipedia.org/wiki/Bifurcation_ratio "Bifurcation ratio").


## Inverse of drainage density as a physical quantity

Drainage density can be used to approximate the average length of [overland flow](https://en.wikipedia.org/wiki/Overland_flow "Overland flow") in a catchment. Horton (1945) used the following equation as an approximation to describe the average length of overland flow as a function of drainage density:[[2]](https://en.wikipedia.org/wiki/Drainage_density#cite_note-Horton1945-2)


![{\displaystyle l_{O}={\frac {1}{2D_{d}}},}](https://wikimedia.org/api/rest_v1/media/math/render/svg/f4f4fc605c72773d5eefa8eaf0727e79eed393f3)

where l0![{\displaystyle l_{0}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/e26bea7ddadf1817f47b2d4ce7dc199185823989) is the length of overland flow and Dd![{\displaystyle D_{d}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/32802f4382ff2086a583f602d649ae8a80d367c7) is the drainage density of the catchment.

Considering the geometry of channels on the hillslope, Horton also proposed the following equation[[2]](https://en.wikipedia.org/wiki/Drainage_density#cite_note-Horton1945-2)

![{\displaystyle l_{O}={\frac {1}{2D_{d}{\sqrt {1-\left({\frac {s_{c}}{s_{g}}}\right)^{2}}}}},}](https://wikimedia.org/api/rest_v1/media/math/render/svg/707df25742975aded6a8e2a4da6f46afd2dc909a)

where sc![{\displaystyle s_{c}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/91c4d1b073949e8f032e50ff913afbf43bb5acb7) is the channel slope and sg![{\displaystyle s_{g}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/27343f630c6c4c80749f5640dc98186869cfc050) is the average slope of the ground in the area.






- Slope–area relationships and scaling laws.

![[Pasted image 20250916110331.png]]


- Fractal properties and self-similarity of drainage networks.
![[Pasted image 20250916104818.png]]

**Lecture 2: Longitudinal River Profiles**
- Concept of graded stream and equilibrium profile.
![[Pasted image 20250916110537.png]]


- Processes of knickpoint formation and migration.

![[Pasted image 20250916112311.png]]

![[Pasted image 20250916112412.png]]

![[Pasted image 20250916112940.png]]

- Influence of tectonics, base-level changes, dams.







- Longitudinal profiles as archives of landscape history.








##### Lab
###### Extract drainage networks from DEM.
Stažení DEM
Spravny souradnicovy system
Cely preprocessing pro hydrologicky korektni DEM
Vytvoreni Hydr. site

###### Calculate stream orders, slope–area relationships.
Vytvoreni radu vodnich toku
Slope area relationship - binning
###### Generate longitudinal profiles.
Longitudinal prof.
##### Identify and classify knickpoints (tectonic vs. lithologic).






## Week 3 – River Networks and Longitudinal Profiles

### Lecture 1: River Network Geometry
**Structure**
- **Introduction (5 min)**
  - River networks as self-organizing systems.
  - Why network geometry matters: water routing, sediment transport, tectonic signal.
- **Core Concepts (25 min)**
  - Horton’s laws of stream numbers and lengths.
    - Bifurcation ratio.
    - Stream length ratio.
  - Strahler stream ordering.
  - Drainage density:
    - Definition: total channel length / basin area.
    - Controls: lithology, climate, vegetation.
  - Slope–area relationships.
    - Critical area for channel initiation.
    - Transition from hillslope → channel domain.
- **Examples (10 min)**
  - Amazon Basin: low drainage density, gentle slopes.
  - Alpine catchments: high drainage density, rapid response.
- **Wrap-up (5–10 min)**
  - Short exercise: Students classify stream orders on printed maps.

### Lecture 2: Longitudinal River Profiles
**Structure**
- **Introduction (5 min)**
  - River profile as a window into landscape history.
- **Core Concepts (25 min)**
  - Graded stream concept (Gilbert, Mackin).
  - Equilibrium vs. non-equilibrium profiles.
  - Knickpoints and knickzones:
    - Causes: tectonic uplift, lithologic boundaries, base-level fall.
    - Mechanisms of retreat (vertical incision vs. upstream migration).
  - Profile concavity and convexity.
  - Effects of dams and reservoirs on profile shape.
- **Examples (10 min)**
  - Nile River: tectonic knickpoints linked to rift.
  - Mississippi: near-equilibrium long profile.
- **Wrap-up (5–10 min)**
  - Student sketch: draw expected profiles for uplift vs. base-level fall.

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

---