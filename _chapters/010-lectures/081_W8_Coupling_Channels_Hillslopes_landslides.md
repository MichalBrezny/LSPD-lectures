---
title: W8 – Coupling Channels, Hillslopes, and Mass Movements – Landslides
slug: week8-coupling-channels-hillslopes-mass-movements-landslides
abstract:
---


### Mass movements and slope stability
Mass movements, such as landslides and debris flows, are rapid downslope movements of soil and rock that occur when the driving forces exceed the resisting forces on a slope. The infinite slope model is commonly used to assess slope stability, calculating the Factor of Safety (FoS) as:
$$ FoS = \frac{c + (\sigma - u) \tan \phi}{\tau} $$
where:
- $ c $ = cohesion of the soil (force per unit area)
- $ \sigma $ = normal stress on the failure plane (force per unit area)
- $ u $ = pore water pressure (force per unit area)
- $ \phi $ = internal friction angle (degrees)
- $ \tau $ = shear stress driving the movement (force per unit area)
  
If $ FoS > 1 $, the slope is stable; if $ FoS < 1 $, failure is likely. Triggering mechanisms for mass movements include intense rainfall, earthquakes, and undercutting by rivers. Mass wasting plays a significant role in landscape evolution by rapidly delivering sediment to channels, influencing erosion rates and topographic development.

In landscape evolution models, stochastic landslide modules can be incorporated to simulate the effects of mass movements on sediment flux and topography over time.

# Landslides and rivers interactions

Landslides can significantly impact river systems by delivering large volumes of sediment to channels, altering flow paths, and affecting erosion and deposition patterns. The coupling between hillslopes and channels is essential for understanding landscape evolution, as sediment supply from hillslopes influences channel incision rates and morphology.

## Different scales of interactions
1.  Local scale
   - landslide dams, effects of debris slides or debris flows on low-order channels
2. Catchment scale
   - sediment budgets, modelling of induced sediment pulses in rivers
3. Moubtain belt scale
   - estimation of sediment fluxes 



Korup described individual itneractions like this:

{% include figure.html
    caption="Geomorphic coupling between landslides and rivers. Different types of interactions based on the spatial extent of landslide impact on river channels. From Korup (2005)."
    url="/figures/W8/Korup_geomorphic_coupling.png"
    class="row"
%}


- Areal: these can be large deep seated gravitational slope deformations
- Linear: Landslide hits river and its chanelized and forms debris flow
- Point: Landslide deposits sediment into a river channel, potentially causing aggradation or avulsion.
- Indirect 
- No interactions
  - Landslide does not interfere with a river channel.
