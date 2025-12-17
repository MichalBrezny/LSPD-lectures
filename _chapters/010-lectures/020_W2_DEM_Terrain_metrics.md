---
title: W2 – DEM Analysis, Terrain Metrics
slug: week2-dem-analysis-terrain-metrics
abstract:
---


---
<!-- ## Week 2 – DEM Analysis, Terrain Metrics, and Hydrology
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

---

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


This will be probably for most of you repetition of what you already know from previous courses, but it is important to have a good understanding of these terrain metrics as they are widely used in geomorphology and hydrology.

## Digital Elevation Models (DEMs)
Digital Elevation Models (DEMs) are raster representations of the Earth's surface, where each cell contains an elevation value. DEMs are fundamental for terrain analysis and are used to derive various topographic metrics that describe the shape and characteristics of the landscape. We can distinguish two main types of DEMs: 
- Digital Terrain Models (DTMs): Represent the bare earth surface, excluding vegetation and anthropogenic features like houses, bridges, etc.
- Digital Surface Models (DSMs): Include all surface features, such as vegetation and buildings.

Many global DEMs are in fact DSMs, as they are derived from remote sensing techniques that capture the first reflective surface. 

Many DEMs are freely available for download, e.g., SRTM (Shuttle Radar Topography Mission) or its succesor NASADEM, ASTER GDEM, ALOS DEM and more. Recently, there area attempts to create DTMs using machine learning to remove vegetation and buildings like FABDEM. High-resolution DEMs from LiDAR surveys have become increasingly accessible for detailed local studies. For regional to global scale studies, usage of high resolution DEMs might be problematic due to data volume and processing requirements. Further the high detail of LiDAR DEMs might introduce high frequency noise and artifacts due to man made structures. Thus resampling to coarser resolution DEMs (e.g., 30 m or 90 m) is often performed for larger scale studies.

> [!NOTE]  
> Open topography portal (https://opentopography.org/) is a good resource to search and download high-resolution DEMs from LiDAR surveys and also global DEMs.


### Topography metrics to process

#### Slope and Aspect
Slope is the first derivative of elevation. It indicates the steepness or incline of the terrain. Steeper slopes are more prone to erosion and landslides. Aspect is the compass direction that a slope faces. It influences microclimate conditions, such as sunlight exposure and moisture retention, which affect vegetation patterns.

<!-- Obrazek sklony -->

#### Curvature
Curvature describes the rate of change of slope. Profile curvature affects the acceleration or deceleration of flow along the slope, influencing erosion and deposition processes. Horizontal (planform) curvature indicates whether the terrain is converging or diverging, which affects water flow paths and sediment transport.  


{% include figure.html
  caption="Profile and planform curvature (source: https://pro.arcgis.com/en/pro-app/latest/help/analysis/raster-functions/curvature-function.html)"
  url="/figures/W2/curvature_profile.png"
  alt="Profile curvature"
  %}

{% include figure.html
  caption="Profile and planform curvature (source: https://pro.arcgis.com/en/pro-app/latest/help/analysis/raster-functions/curvature-function.html)"
  url="/figures/W2/curvature_plan.png"
  alt="Plan (horizontal) curvature"
   %}

{% include figure.html
  caption="Combinations of profile and horizontal curvature (source: https://pro.arcgis.com/en/pro-app/latest/help/analysis/raster-functions/curvature-function.html)"
  url="/figures/W2/curvature_combo.png"
  alt="Profile and planform curvature"
  %}


> [!NOTE]
> There area many other types of curvatures, but plan and profile curvatures are the mostly used and easiest to interpret. For more information on other types of curvatures, see e.g., . 

#### Hypsometry
The hypsometric curve represents the cumulative distribution of elevation within a drainage basin. The hypsometric integral quantifies the stage of landscape development, with higher values indicating youthful landscapes and lower values indicating mature landscapes.

#### Hydrological Indices
The Topographic Wetness Index (TWI) is calculated as 
$$ TWI = \ln\left(\frac{a}{\tan\beta}\right) $$
where \( a \) is the upslope contributing area per unit contour length and \( \beta \) is the local slope angle. TWI helps predict soil moisture distribution and potential saturation zones. 

#### Runoff Processes
Hortonian runoff occurs when rainfall intensity exceeds the soil's infiltration capacity, leading to surface runoff. Dunne runoff happens when the soil becomes saturated, causing excess water to flow over the surface. The hydrograph illustrates the temporal variation of streamflow, with key features including the rising limb, peak flow, and recession limb, which reflect the catchment's response to rainfall events.

