---
title: W11 – Applications and Case Studies – Applied Geomorphology
slug: week11-applications-case-studies-applied-geomorphology
abstract:
---
# Week 11 – Applications and Case Studies

# Applied Geomorphology and Case Studies
[![Three Gorges Dam Facts | Britannica](https://tse1.mm.bing.net/th/id/OIP.qGW69OSSom_TOvcOiiwVqAHaEL?pid=Api)](https://www.britannica.com/facts/Three-Gorges-Dam?utm_source=chatgpt.com)

## Learning goals for the week


* Explain how quantitative geomorphology supports real-world decisions (risk reduction, infrastructure planning, restoration design).
* Compare empirical/statistical models vs. process-based models and justify model choice for a given problem.
* Interpret case studies where climate, tectonics, and humans shape sediment fluxes and landscape change.
* Communicate uncertainty (data, model structure, parameters) and its implications for management.

---

# Applied Quantitative Geomorphology

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

## Short case examples (10 min)

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

---

## Case Studies & Anthropocene Geomorphology

## Humans as geomorphic agents

Humans move and redistribute enormous volumes of earth materials through mining, construction, and agriculture—often comparable to major natural agents at broad scales. ([exploreiowageology.org][8])

---

## Case study theme: tectonics vs. climate

### A. Himalaya: decoupling and coupling hypotheses

A core debate: Do precipitation gradients map directly onto long-term erosion patterns?

* One influential example shows **weak correspondence** between a strong precipitation gradient and geologic-scale erosion rates in the Greater Himalaya (Nepal), implying decoupling under some conditions. ([Scholars@Duke][9])
* Interpretation tools: thermochronometry, river profile metrics, landslide contributions, lithologic contrasts, transient response times.

### B. Andes: uplift and precipitation gradients

* Erosion rates can vary strongly across rainfall gradients; examples document **order-of-magnitude** differences across steep climatic transitions and interpret patterns with stream-power style frameworks. ([ScienceDirect][10])

---

## Anthropocene geomorphology: three major mechanisms

### A. Dams and sediment connectivity

* Dams trap sediment, interrupt downstream continuity, and can cause downstream channel/coastal sediment starvation.
* Global synthesis: humans can increase hillslope erosion yet reduce sediment reaching coasts due to reservoir trapping. ([PubMed][11])
* Management perspective: strategies exist to pass or manage sediment in regulated rivers and reservoirs. ([Wiley Online Library][12])

### B. Mining and large-scale earth moving

* Direct topographic reconfiguration, new sediment sources, altered hydrology, and long legacy impacts (tailings, spoil, drainage network changes).

### C. Urbanization and “urban stream syndrome”

Urban watersheds often show:

* flashier hydrographs, channel incision/widening, altered sediment regimes, degraded ecological function. ([journals.uchicago.edu][13])

---

## Focus example (10 min): Three Gorges Dam (Yangtze/Changjiang)

* Large reservoirs can trap substantial fractions of upstream sediment and shift downstream sediment budgets.
* Example analyses quantify deposition/trapping and discuss downstream/coastal implications after Three Gorges operation. ([hess.copernicus.org][14])

---

## Wrap-up debate prompt

**Humans vs. glaciers — which can reshape landscapes faster?**
Use at least one **order-of-magnitude** argument (e.g., volumes moved per year; spatial extent; timescales of dominance). ([exploreiowageology.org][8])

---

# Key terms (quick glossary)

* **Susceptibility**: relative likelihood of occurrence (where processes are more/less likely).
* **Hazard**: probability and intensity of a damaging process (depth/velocity/runout).
* **Risk**: hazard × exposure × vulnerability.
* **Connectivity**: how efficiently sediment/water moves through a landscape (sources → sinks).
* **Validation**: independent testing of model outputs against observations.
* **Uncertainty**: data error + parameter uncertainty + structural/model-form limits.

---

# Suggested reading (core list)

* Bates, P. D., et al. (2010). Efficient 2D flood inundation modeling using a (local/inertial) shallow-water formulation. ([ScienceDirect][1])
* Chalise, A., et al. (2022). Landslide susceptibility mapping (Baglung District, Nepal) using ML approaches. ([nepjol.info][6])
* O’Brien, J. S., Julien, P. Y., & Fullerton, W. T. (1993). FLO-2D concept for 2D flood and mud/debris-flow simulation. ([ascelibrary.org][2])
* Hooke, R. LeB. (2000). Humans as geomorphic agents (earth-moving at large scales). ([exploreiowageology.org][8])
* Syvitski, J. P. M., et al. (2005). Human impacts on global river sediment flux to coasts. ([PubMed][11])
* Hu, B., et al. (2009) and/or Yang, S. L., et al. (2014). Sediment trapping and downstream geomorphic impacts of Three Gorges. ([hess.copernicus.org][14])
* Heimann, D. C., et al. (2011). USGS trends in suspended-sediment loads in the Mississippi River Basin. ([pubs.usgs.gov][7])
* Montgomery, D. R. (2007). Soil erosion and agricultural sustainability (orders-of-magnitude argument). ([pnas.org][5])
* Walsh, C. J., et al. (2005). Urban stream syndrome. ([journals.uchicago.edu][13])
* Kondolf, G. M., et al. (2014). Sustainable sediment management in reservoirs and regulated rivers. ([Wiley Online Library][12])

[1]: https://www.sciencedirect.com/science/article/abs/pii/S0022169410001538?utm_source=chatgpt.com "A simple inertial formulation of the shallow water equations ..."
[2]: https://ascelibrary.org/doi/10.1061/%28ASCE%290733-9429%281993%29119%3A2%28244%29?utm_source=chatgpt.com "Two‐Dimensional Water Flood and Mudflow Simulation"
[3]: https://ramms.ch/ramms-debrisflow/?utm_source=chatgpt.com "RAMMS:: Debrisflow - RAMMS - Rapid Mass Movement ..."
[4]: https://calsalmon.org/sites/default/files/files/Kondolf_2011_SettingGoals.pdf?utm_source=chatgpt.com "Setting Goals in River Restoration: When and Where Can ..."
[5]: https://www.pnas.org/doi/10.1073/pnas.0611508104?utm_source=chatgpt.com "Soil erosion and agricultural sustainability"
[6]: https://www.nepjol.info/index.php/NJG/article/download/50880/38019/150357?utm_source=chatgpt.com "Landslide Susceptibility Mapping Using Machine Learning ..."
[7]: https://pubs.usgs.gov/publication/sir20115200?utm_source=chatgpt.com "Trends in suspended-sediment loads and concentrations ..."
[8]: https://www.exploreiowageology.org/assets/text/Gemorph/UNI_Geomorph_papers/hooke_2000.pdf?utm_source=chatgpt.com "On the history of humans as geomorphic agents"
[9]: https://scholars.duke.edu/display/pub759159?utm_source=chatgpt.com "Decoupling of erosion and precipitation in the Himalayas"
[10]: https://www.sciencedirect.com/science/article/abs/pii/S0012821X12000805?utm_source=chatgpt.com "Examples from the southern Central Andes"
[11]: https://pubmed.ncbi.nlm.nih.gov/15831750/?utm_source=chatgpt.com "Impact of humans on the flux of terrestrial sediment to ..."
[12]: https://agupubs.onlinelibrary.wiley.com/doi/10.1002/2013EF000184?utm_source=chatgpt.com "Sustainable sediment management in reservoirs and ..."
[13]: https://www.journals.uchicago.edu/doi/10.1899/04-028.1?utm_source=chatgpt.com "The urban stream syndrome: current knowledge and ..."
[14]: https://hess.copernicus.org/articles/13/2253/2009/?utm_source=chatgpt.com "Sedimentation in the Three Gorges Dam and the future ..."
