---
title: W8 – Coupling Channels, Hillslopes, and Mass Movements - Diffusion
slug: week8-coupling-channels-hillslopes-mass-movements-diffusion
abstract:
---

In this week, we will explore how hillslopes and channels interact to shape landscapes. We will cover hillslope diffusion processes that transport sediment downslope and how mass movements like landslides contribute to sediment flux. Understanding these coupled processes is crucial for modeling landscape evolution accurately.

## Diffusion processes
Diffusive processes round the landscape, softens the edges and transport sediment from hillslopes to channels.

### Hillslope Diffusion
**Rainsplash** is one of the diffusive processes that move soil particles downslope. Raindrops impact the soil surface and eject grains. On the flat surface the grains land close to the imapact point. However on sloped surface grains travel on longer distances downslope. This process results in net sediment transport downslope that can be described as diffusion.

**Creep** is another diffusive process that slowly moves soil and regolith downslope. Creep is driven by various mechanisms, including freeze-thaw cycles, wetting and drying, and biological activity (e.g., burrowing animals, root growth). These processes cause soil particles to move incrementally downslope over time, leading to gradual landscape evolution.

<!-- 
Obrazek hillslope diffusion 
-->
{% include figure.html
    caption="Hillslope diffusion processes"
    url="/figures/W8/hillslope_diffusion.png"
    class="row"
%}

**Tree throw** is a bioturbation process where trees uproot and displace soil as they fall. This action can contribute to sediment transport on hillslopes, especially in forested areas. The disturbance caused by tree throw can create microtopography that enhances other diffusive processes. Resulting microtopography is called pit-and-mound topography. 

For example in the Razula forest in the Outer Western Carpathians (study area about 25 ha) between 1972 and 2009 experienced nearly 1.5 uproots per hectare per year. Each uproot moved on average 2.9 m³ of soil and regolith. This results in pit-mound morphology on the 14 % of the area (Phillips et al., 2017).


{% include figure.html
    caption="Pit-and-mound topography caused by tree throw in the Razula forest, Outer Western Carpathians (Phillips et al., 2017)."
    url="/figures/W8/pit_mound1.jpg"
    class="row"
%}

The simplest model for hillslope diffusion is the linear diffusion equation:
$$ q = -D \frac{\partial z}{\partial x} $$
where:
- \( q \) = sediment flux (L^2/T)
- \( D \) = diffusion coefficient (L^2/T)     
- \( \frac{\partial z}{\partial x} \) = slope gradient (dimensionless)
- L = length, T = time
This equation states that sediment flux is proportional to the local slope gradient, with the diffusion coefficient \( D \) which integrates all diffusion processes and their efficiency of sediment transport. On steep slopes, nonlinear diffusion models may be more appropriate, accounting for threshold slopes beyond which sediment transport increases rapidly.





## References
Phillips, J.D., Šamonil, P., Pawlik, Ł., Trochta, J., Daněk, P., 2017. Domination of hillslope denudation by tree uprooting in an old-growth forest. Geomorphology 276, 27–36. https://doi.org/10.1016/j.geomorph.2016.10.006
