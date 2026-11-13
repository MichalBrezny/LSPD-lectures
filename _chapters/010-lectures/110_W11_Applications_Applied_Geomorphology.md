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

So far we have used quantitative methods to understand how landscapes evolve over thousands to millions of years. The same tools (DEM analysis, flow routing, process laws, numerical models) are used to answer practical questions on much shorter timescales: where a flood will spread, which slopes are likely to fail, how much sediment will reach a reservoir. The main difference is in the purpose. In research the result is an explanation, and in applied work it is a decision, usually made by someone who is not a geomorphologist.

---

## From theory to practice: the applied workflow

A typical applied workflow has six steps:

1. **Define the decision question** (e.g., “Where is landslide risk highest?” “How much sediment will reach a reservoir?”). The question determines the required output, its spatial scale and the acceptable uncertainty.
2. **Assemble data** (topography, rainfall, geology, land cover, inventories of past events, discharge and sediment records).
3. **Choose a model family**, empirical or process-based (see below).
4. **Validate** the model against information that was not used to build it (hindcasts of past events, cross-validation, field constraints).
5. **Quantify uncertainty** (data error, parameter ranges, structural limits of the model, see W10).
6. **Deliver an actionable output** (maps, scenarios, thresholds, design values, decision rules).

### Empirical vs. process-based models
The choice of the model family is the key decision of the workflow.

| | Empirical / statistical models | Process-based models |
|---|---|---|
| Principle | relationships found in data on past events (regression, machine learning) | equations describing the physics of the process (hydraulics, sediment transport, slope stability) |
| Data needs | a large and representative inventory of events | physical parameters (roughness, strength, rheology) and boundary conditions |
| Strengths | fast, applicable to large areas, few assumptions about the process | can simulate scenarios that have not happened yet, give physical quantities (depth, velocity) |
| Limitations | valid only for the conditions represented in the data, do not explain the mechanism | parameters are difficult to measure, computationally demanding |
| Typical use | regional susceptibility maps | design of a specific structure, hazard maps for a specific site |

In general, empirical models are suitable for regional screening, and process-based models for detailed studies of the sites that the screening identified. An empirical model should not be used outside the range of conditions on which it was trained. This is a serious limitation when the conditions are changing, for example the climate or the land use.

---

## Hazard applications

Three terms are often confused, and they should be kept apart:

- **Susceptibility** says *where* an event is likely to occur.
- **Hazard** adds *when and how large*: the probability that an event of a given magnitude occurs in a given area within a given time.
- **Risk** adds the consequences: it combines hazard with the exposure and vulnerability of people and property.

### A. Flood risk modeling (concepts and outputs)

The goal is to predict the **water depth, extent and velocity** for given boundary conditions (the discharge entering the area) and terrain. The models solve the shallow-water equations, which describe the conservation of mass and momentum of the flow, in full or in a simplified form. A good example of the simplified approach are fast 2D inundation models based on an inertial formulation of the shallow-water equations, which allow efficient simulation of floodplains over large areas ([Bates et al., 2010][1]).

Typical outputs are hazard maps of depth and velocity, maps of flood extent for a given return period (e.g., the 100-year flood) and comparisons of scenarios, such as with and without a levee.

The models are validated against observed inundation extents, gauge hydrographs and high-water marks. The results are most sensitive to the quality and resolution of the DEM and to the roughness of the surface. Small features such as embankments and culverts control where the water spreads, and a coarse DEM does not contain them (compare with the pitfalls of flow routing in W2).

### B. Landslide susceptibility mapping

The goal is to map **where landslides are more likely**. The usual approach is empirical and rests on the assumption that future landslides will occur under conditions similar to those of past ones:

1. Compile a landslide inventory, i.e., a map of known landslides.
2. Prepare maps of the conditioning factors: terrain (slope, curvature, aspect), lithology, land cover and hydrological proxies such as the topographic wetness index (W2).
3. Train a statistical or machine-learning model (e.g., logistic regression or random forest) to distinguish the places with landslides from the places without them.
4. Apply the model to the whole area and classify the result into susceptibility classes.

The performance is evaluated by the ROC curve and the area under it (AUC) and by the confusion matrix (precision and recall). The data should be split spatially for the validation. If the training and testing points are neighbours, they are not independent, and the performance of the model is overestimated.

The quality of the map depends above all on the inventory. An inventory that is incomplete or biased, for example towards landslides along roads, produces a biased map.

### C. Debris-flow routing / runout

The goal is to predict **where a debris flow can travel** and where deposition or impact is likely. A debris flow is a mixture of water and sediment that behaves differently from water, so the models need a rheological law describing the resistance of the mixture to flow.

Common modeling approaches:
* 2D routing models used for floods as well as for mud and debris flows, such as FLO-2D ([O'Brien et al., 1993][2]).
* Dedicated runout tools used in hazard assessment, such as [RAMMS::Debrisflow][3].

Typical outputs are the runout extent, the maximum flow depth and velocity and the impact pressure. The rheological parameters cannot be measured directly. They are calibrated by back-calculation of past events in the same or a similar catchment, and the release volume of the future event remains the largest source of uncertainty.

---

## Restoration and river management

### A. Sediment budgets for restoration

A sediment budget is an accounting of sediment along its way through a reach or a catchment: **sources → transfers → storage → sinks**. It follows from the conservation of mass:

$$ I - O = \Delta S $$

where $I$ is the sediment input, $O$ is the output and $\Delta S$ is the change in storage. If the input exceeds the output, sediment accumulates and the channel aggrades. If the output exceeds the input, the channel erodes its bed and banks.

A budget is used to diagnose whether a river is **sediment-starved** (typically downstream of dams and gravel mines) or **sediment-rich**, and to design the interventions accordingly. A restoration project that ignores the sediment budget often fails: a channel form constructed in a sediment-starved river will not be maintained by the river.

### B. Reconnecting floodplains

Many rivers were cut off from their floodplains by levees and by incision of the channel. Floodplain reconnection can increase overbank storage of water, locally reduce flood peaks, promote deposition of fine sediment and support the diversity of habitats.

The planning concept is to provide sufficient **space for channel migration and flooding** (the “erodible corridor”) and to let the river do the work, instead of constructing a fixed channel form. This is possible only where the river still has enough stream power and sediment supply to rework its bed and banks. Where it does not, more active intervention is needed ([Kondolf, 2011][4]).

---

## Land-use impacts on surface processes

The key idea is that land use can shift erosion and sediment delivery by orders of magnitude.

Conventional tillage often produces erosion rates **1–2 orders of magnitude** above the rates of soil production and above background geological erosion rates ([Montgomery, 2007][5]). Soil is lost much faster than it forms, so such agriculture is not sustainable in the long term. Erosion rates under no-till farming and under natural vegetation are close to the rates of soil production.

The implications go beyond the fields: a higher sediment yield, aggradation or incision of channels, and altered flood hazard, because cleared and compacted surfaces produce faster runoff with higher peaks (“flashier” hydrographs).

---

## Short case examples

### Case 1 — Nepal: landslide susceptibility mapping (Baglung District)

A machine-learning susceptibility model was built for a district in the Nepal Himalaya from a landslide inventory and a set of conditioning factors (e.g., slope, land use, geology) ([source][6]). The output is a map of susceptibility classes together with an evaluation of the model performance. It is a typical example of the empirical workflow described above.

### Case 2 — Mississippi River Basin: sediment trends under regulation and change

Multi-decadal analyses show downward trends in suspended-sediment loads and concentrations at many stations in the basin between 1950 and 2009 ([Heimann et al., 2011][7]).

Discussion point: sediment delivery can decline even when the hydrologic drivers vary, due to sediment trapping in reservoirs, bank stabilization and changing sources. The consequence is felt far downstream, where the delta depends on the supply of sediment.

---

## Wrap-up question

**How can landscape evolution models (LEMs) and applied models support decision-making?**
Think: scenario testing, prioritization, communicating uncertainty, “what-if” planning, and design thresholds.

> The case studies that put these methods to work — Himalaya, Andes, and the Anthropocene — continue in the [Case Studies](week11-applications-case-studies) part.

# References
Bates, P.D., Horritt, M.S., Fewtrell, T.J., 2010. A simple inertial formulation of the shallow water equations for efficient two-dimensional flood inundation modelling. Journal of Hydrology 387, 33–45. https://doi.org/10.1016/j.jhydrol.2010.03.027

Heimann, D.C., Sprague, L.A., Blevins, D.W., 2011. Trends in suspended-sediment loads and concentrations in the Mississippi River Basin, 1950–2009. U.S. Geological Survey Scientific Investigations Report 2011–5200. https://doi.org/10.3133/sir20115200

Kondolf, G.M., 2011. Setting goals in river restoration: When and where can the river “heal itself”?, in: Simon, A., Bennett, S.J., Castro, J.M. (Eds.), Stream Restoration in Dynamic Fluvial Systems. Geophysical Monograph Series 194. American Geophysical Union, Washington, D.C., pp. 29–43. https://doi.org/10.1029/2010GM001020

Montgomery, D.R., 2007. Soil erosion and agricultural sustainability. Proceedings of the National Academy of Sciences 104, 13268–13272. https://doi.org/10.1073/pnas.0611508104

O'Brien, J.S., Julien, P.Y., Fullerton, W.T., 1993. Two-dimensional water flood and mudflow simulation. Journal of Hydraulic Engineering 119, 244–261. https://doi.org/10.1061/(ASCE)0733-9429(1993)119:2(244)

[1]: https://www.sciencedirect.com/science/article/abs/pii/S0022169410001538 "A simple inertial formulation of the shallow water equations ..."
[2]: https://ascelibrary.org/doi/10.1061/%28ASCE%290733-9429%281993%29119%3A2%28244%29 "Two‐Dimensional Water Flood and Mudflow Simulation"
[3]: https://ramms.ch/ramms-debrisflow/ "RAMMS:: Debrisflow - RAMMS - Rapid Mass Movement ..."
[4]: https://calsalmon.org/sites/default/files/files/Kondolf_2011_SettingGoals.pdf "Setting Goals in River Restoration: When and Where Can ..."
[5]: https://www.pnas.org/doi/10.1073/pnas.0611508104 "Soil erosion and agricultural sustainability"
[6]: https://www.nepjol.info/index.php/NJG/article/download/50880/38019/150357 "Landslide Susceptibility Mapping Using Machine Learning ..."
[7]: https://pubs.usgs.gov/publication/sir20115200 "Trends in suspended-sediment loads and concentrations ..."
