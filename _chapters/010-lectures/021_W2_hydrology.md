---
title: Week 2 – Terrain Metrics
slug: Week2
abstract:
---


## Overview
**Lecture 1: Digital Elevation Models**
- Data sources: SRTM, ASTER, LiDAR, UAV-based DEMs.
- Strengths and weaknesses of different datasets.
- Vertical accuracy, resolution trade-offs.
- DEM preprocessing workflows.

**Lecture 2: Terrain Metrics & Hydrology**
- First- and second-order DEM derivatives: slope, aspect, curvature.
- Basin hypsometry as a maturity indicator.
- Hydrological indices: TWI, SPI.
- Infiltration theory: Horton vs. Dunne mechanisms.
- Hydrographs: stormflow, baseflow, lag time.

**Lab**
- Extract slope, aspect, curvature, hypsometry, TWI from DEM in GIS (QGIS/SAGA).
- Compare terrain metrics at different DEM resolutions.
- Spreadsheet hydrology: create a rainfall–runoff model.
- **Exercise:** Test infiltration capacity scenarios (sandy vs. clay soil).

---


## Week 2 – DEM Analysis, Terrain Metrics, and Hydrology

### Lecture 1: Digital Elevation Models
**Structure**
- **Introduction (5 min)**
  - DEM as foundation of quantitative geomorphology.
  - Ubiquity: hazard mapping, hydrology, tectonic analysis.
- **Sources of DEMs (15 min)**
  - SRTM: 30 m, global coverage, radar-based, voids in steep terrain.
  - ASTER GDEM: optical stereo, errors in flat areas.
  - LiDAR: very high resolution, vegetation penetration.
  - UAV/photogrammetry: local, flexible, but limited extent.
- **Resolution and Accuracy (10 min)**
  - Vertical error (±5–15 m typical for SRTM).
  - Trade-offs: higher resolution vs. larger file sizes.
  - Scale issues: slope underestimated in coarse DEMs.
- **Preprocessing Workflows (15 min)**
  - Projection to UTM for accurate measurements.
  - Pit filling and breaching.
  - Mosaic building.
  - Resampling methods (nearest neighbour vs. bilinear).
- **Examples (10 min)**
  - Compare slope histograms of LiDAR vs. SRTM in the same area.
- **Wrap-up (5 min)**
  - Short quiz: Which DEM to use for tectonic knickpoint study?

---

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

---




