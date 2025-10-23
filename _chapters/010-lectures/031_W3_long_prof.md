---
title: Week 3 – River Networks and Longitudinal Profiles
slug: Week3
abstract:
---





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