---
title: W11 – Applications and Case Studies – Applied Geomorphology
slug: week11-applications-case-studies-applied-geomorphology
abstract: How quantitative geomorphology supports real-world decisions — hazards, restoration, and land-use impacts.
---

# Applied Geomorphology

## Learning goals for the week

* Explain how quantitative geomorphology supports real-world decisions (risk reduction, infrastructure planning, restoration design).
* Compare empirical/statistical models vs. process-based models and justify model choice for a given problem.
* Interpret case studies where climate, tectonics, and humans shape sediment fluxes and landscape change.
* Communicate uncertainty (data, model structure, parameters) and its implications for management.

---

## From theory to practice: the applied workflow

A typical applied workflow:

1. **Define the decision question** (e.g., “Where is landslide risk highest?” “How much sediment will reach a reservoir?”).
2. **Assemble data** (topography, rainfall, geology, land cover, inventories, discharge/sediment records).
3. **Choose a model family**

   * **Empirical / statistical** (correlations, ML, regressions, susceptibility mapping).
   * **Process-based** (hydraulics, sediment transport, slope stability, runout).
4. **Validate** (hindcasts, cross-validation, event comparisons, field constraints).
5. **Quantify uncertainty** (data error, parameter ranges, model structural limits).
6. **Deliver an actionable output** (maps, scenarios, thresholds, design values, decision rules).

---

## Hazard applications

### A. Flood risk modeling (concepts and outputs)

* Goal: predict **water depth/extent/velocity** given boundary conditions and terrain.
* Model spectrum:

  * **Fast 2D inundation models** (local/inertial shallow-water formulations) for efficient floodplain simulation. ([ScienceDirect][1])
* Typical outputs: hazard maps (depth/velocity), return-period maps, scenario comparisons.
* Validation ideas: observed inundation extents, gauge hydrographs, high-water marks; sensitivity to DEM resolution and roughness.

### B. Landslide susceptibility mapping

* Goal: map **where landslides are more likely**, typically using:

  * landslide inventory + terrain/land cover/lithology/hydrology proxies
  * statistical/ML models (e.g., RF, logistic regression)
* Performance metrics: ROC–AUC, confusion matrix (precision/recall), spatial cross-validation.

### C. Debris-flow routing / runout

* Goal: predict **where a debris flow can travel** and where deposition/impact is likely.
* Common modeling approaches:

  * 2D routing models used for flood + mud/debris flows (e.g., FLO-2D concept). ([ascelibrary.org][2])
  * Dedicated runout tools used in hazard assessment (e.g., RAMMS::Debrisflow). ([Basic box][3])
* Typical outputs: runout extent, maximum flow depth/velocity, impact pressure proxies.

---

## Restoration and river management

### A. Sediment budgets for restoration

* Sediment budget = accounting of **sources → transfers → storage → sinks** across a reach/catchment.
* Used to diagnose whether a river is **sediment-starved vs. sediment-rich**, and to design interventions.

### B. Reconnecting floodplains

* Floodplain reconnection can:

  * increase overbank storage, reduce peak stages locally, promote deposition, and support habitat complexity.
* Planning concept: provide sufficient **space for channel migration and flooding** (e.g., “erodible corridor” thinking). ([Salmonid Restoration Federation][4])

---

## Land-use impacts on surface processes

Key idea: land use can shift erosion and sediment delivery by orders of magnitude.

* Conventional tillage often produces erosion rates **1–2 orders of magnitude** above soil production and background geological rates. ([pnas.org][5])
* Implications: higher sediment yield, channel aggradation/incision, and altered flood hazards (via runoff “flashiness”).

---

## Short case examples

### Case 1 — Nepal: landslide susceptibility mapping (Baglung District)

* ML-based susceptibility mapping using an inventory + conditioning factors (e.g., slope, land use, geology).
* Typical output: susceptibility classes + model performance evaluation. ([nepjol.info][6])

### Case 2 — Mississippi River Basin: sediment trends under regulation and change

* Many stations show downward trends in suspended-sediment loads/concentrations (multi-decadal analyses). ([pubs.usgs.gov][7])
* Discussion point: sediment delivery can decline even when hydrologic drivers vary, due to dams, bank stabilization, and changing sources.

---

## Wrap-up question

**How can landscape evolution models (LEMs) and applied models support decision-making?**
Think: scenario testing, prioritization, communicating uncertainty, “what-if” planning, and design thresholds.

> The case studies that put these methods to work — Himalaya, Andes, and the Anthropocene — continue in the [Case Studies](week11-applications-case-studies) part.

[1]: https://www.sciencedirect.com/science/article/abs/pii/S0022169410001538 "A simple inertial formulation of the shallow water equations ..."
[2]: https://ascelibrary.org/doi/10.1061/%28ASCE%290733-9429%281993%29119%3A2%28244%29 "Two‐Dimensional Water Flood and Mudflow Simulation"
[3]: https://ramms.ch/ramms-debrisflow/ "RAMMS:: Debrisflow - RAMMS - Rapid Mass Movement ..."
[4]: https://calsalmon.org/sites/default/files/files/Kondolf_2011_SettingGoals.pdf "Setting Goals in River Restoration: When and Where Can ..."
[5]: https://www.pnas.org/doi/10.1073/pnas.0611508104 "Soil erosion and agricultural sustainability"
[6]: https://www.nepjol.info/index.php/NJG/article/download/50880/38019/150357 "Landslide Susceptibility Mapping Using Machine Learning ..."
[7]: https://pubs.usgs.gov/publication/sir20115200 "Trends in suspended-sediment loads and concentrations ..."
