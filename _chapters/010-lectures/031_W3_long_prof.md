---
title: W3 – Longitudinal Profiles
slug: week3-longitudinal-profiles
abstract:
---

# River profile as a record of landscape evolution

Rivers are dynamic systems that respond to external forcing such as tectonics, climate and base-level change. A longitudinal river profile (channel elevation plotted against distance along the river) is the simplest way to see this response. The profile sets the relief of the whole landscape, because hillslopes are graded to the channels at their base. It also keeps a record of past changes for a long time, in some cases for millions of years. Longitudinal profiles can therefore provide important insights into the history of landscape evolution.

Two terms are needed before we start:

- **Base level** is the lowest elevation to which a river can erode. The ultimate base level is the sea. A lake, a resistant rock barrier or a confluence with a larger river acts as a local base level.
- **Longitudinal profile** is extracted from a DEM by following the flow path from the channel head to the outlet (see the previous lecture on flow routing).

# Concept of graded stream and equilibrium profile

The idea that a river adjusts its slope to the work it has to do goes back to Gilbert (1877), and Mackin (1948) developed it into the concept of the graded stream. A graded stream is one in which, over a period of years, slope is adjusted to provide exactly the velocity required to transport the sediment supplied from the basin with the available discharge. In this state the river neither aggrades nor degrades its bed over time, and its longitudinal profile is stable. A graded stream is a system in equilibrium: if one of the controlling factors changes, the river responds in a way that absorbs the effect of the change.

The equilibrium profile is typically smooth and concave-up, which means that the slope decreases downstream. There are two main reasons:

- **Discharge increases downstream** as tributaries join the river. A larger river is deeper and more efficient, so it can transport its sediment load and erode its bed on a gentler slope.
- **Grain size decreases downstream** due to abrasion and selective transport, and finer sediment can be moved on a gentler slope.

{% include figure.html
    caption="Graded longitudinal profile and departures from it – knickzones and knickpoints. (Source: Bierman and Montgomery, Key Concepts in Geomorphology)"
    url="/figures/W3/long_profile.png"
    class="row"
%}

> [!NOTE]
> More about the graded stream concept and its history can be found in Kesseli, J.E., 1941. The Concept of the Graded River. The Journal of Geology 49, 561–588. https://www.jstor.org/stable/30079638

> [!IMPORTANT]
> A smooth concave profile is not a proof of equilibrium, and a steep reach is not a proof of disequilibrium. A river can be in equilibrium and still have a steeper reach where it crosses more resistant rock or a zone of faster uplift.

## Slope-area relationships
Distance along the river is not the best variable for comparing rivers, because what matters for erosion and transport is discharge. We therefore replace distance with drainage area ($A$), which we use as a proxy for discharge (see W2).

In most rivers, the channel slope ($S$) decreases with drainage area as a power law known as Flint's law (Flint, 1974):

$$ S = k_s A^{-\theta} $$

where:
- $S$ is the local channel slope (m/m),
- $A$ is the upstream drainage area (m²),
- $\theta$ is the **concavity index**,
- $k_s$ is the **steepness index**.

Taking the logarithm of both sides gives the equation of a straight line:

$$ \log S = \log k_s - \theta \log A $$

In a plot of slope against drainage area with both axes logarithmic (a *slope–area plot*), a graded river profile forms a straight line. The two parameters have a clear graphical meaning:

- The **concavity index** $\theta$ is the slope of the line. It describes how fast the channel slope decreases downstream, i.e., how strongly the profile is curved. Values between about 0.4 and 0.6 are typical for bedrock and mixed bedrock–alluvial rivers. A river with $\theta = 0$ would have a straight profile.
- The **steepness index** $k_s$ is the intercept of the line. It describes how steep the channel is for a given drainage area. Of two rivers with the same drainage area and the same concavity, the one with the higher $k_s$ is steeper.

> [!IMPORTANT]
> Do not confuse concavity with steepness. A high $\theta$ means a more curved profile and not a steeper one. It is the steepness index, not the concavity index, that increases with the rate of rock uplift and with rock resistance.

### Normalized steepness index
The value and even the units of $k_s$ depend on $\theta$ (the units are $\mathrm{m}^{2\theta}$). Small differences in $\theta$ between rivers lead to large differences in $k_s$, so the steepness indices of two rivers with different concavities cannot be compared. The solution is to fix the concavity to one **reference concavity** $\theta_{ref}$ for all rivers of the study area, usually 0.45, and to calculate the **normalized steepness index** $k_{sn}$ (Wobus et al., 2006):

$$ k_{sn} = S A^{\theta_{ref}} $$

With $\theta_{ref} = 0.45$ the units of $k_{sn}$ are $\mathrm{m}^{0.9}$. Maps of $k_{sn}$ are one of the most widely used tools of tectonic geomorphology, and we will return to them in W4–W6.

### Limits of slope–area analysis
- Flint's law holds only for the fluvial part of the network. Below a critical drainage area, typically of the order of 0.1–1 km², slope stops increasing upstream because hillslope and debris-flow processes dominate there. This break in the slope–area plot is often used to locate channel heads.
- Slope is a derivative of elevation, so the errors of the DEM are amplified. Raw slope–area data are very noisy and have to be smoothed or averaged in bins of drainage area. This is the main motivation for the $\chi$ transformation, which works with elevation instead of slope (W5).

## Knickpoints and knickzones
A **knickpoint** is an abrupt change in channel slope or elevation, often manifesting as a waterfall or rapids. A **knickzone** is a longer oversteepened reach, i.e., a reach that is steeper than the reaches upstream and downstream. Both are departures from the smooth graded profile.

{% include figure.html
    caption="Niagara Falls, a classic example of a knickpoint. (By Quistnix - Own work, CC BY-SA 3.0, https://commons.wikimedia.org/w/index.php?curid=185)"
    url="/figures/W3/Niagara_watervallen_canada.jpg"
    class="row"
%}

### How do knickpoints form?
- **Base-level fall**: a drop in sea or lake level, or the incision of the main river that leaves its tributaries hanging.
- **Tectonics**: displacement on a fault that crosses the river, or an increase in the rate of rock uplift.
- **Lithology**: a contact between resistant and weak rock.
- **Other local causes**: landslide and glacial dams, large tributaries supplying coarse sediment, glacially oversteepened valley steps, river capture.

### Mobile and fixed knickpoints
For the interpretation it is essential to distinguish two groups of knickpoints:

- **Mobile (transient) knickpoints** are created by a change at the downstream end of the river, such as a base-level fall or an increase in uplift rate. The river starts to incise at its mouth, and the incision propagates upstream as a wave. The knickpoint is the upstream front of this wave. It separates the lower part of the river, which is already adjusted to the new conditions, from the upper part, which still "does not know" about the change. Niagara Falls is an example: the falls have retreated about 11 km since the last deglaciation, some 12,000 years ago, and left the Niagara Gorge behind.
- **Fixed (stationary) knickpoints** are tied to the place where they formed, for example to a resistant rock unit or to an active fault. They stay there as long as their cause persists.

The upstream migration of a knickpoint is faster in larger rivers, because the migration rate increases with drainage area. A knickpoint therefore moves quickly along the main river and slows down as it enters smaller and smaller tributaries. Knickpoints formed by one event are thus found at a similar elevation across the river network. We will derive this behaviour from the stream power incision model in W6.

A knickpoint may also change its shape while it migrates. Where a resistant layer caps weaker rocks, the step retreats without losing its form (parallel retreat). In uniform rocks the step usually becomes gentler and wider with time (slope replacement).

{% include figure.html
    caption="Models for knickpoint migration: (A) parallel retreat, (B) slope replacement and (C) differential erosion without propagation. (Source: Burbank and Anderson, 2011, modified after Gardner, 1983)"
    url="/figures/W3/knickpoint_migration.png"
    class="row"
%}

### How to distinguish them?
No single criterion is sufficient, so several of them have to be combined:

| Observation | Mobile knickpoint | Fixed knickpoint |
|---|---|---|
| Position in the network | similar elevation in the main river and its tributaries | along a geological boundary (lithological contact, fault) |
| Geological map | no relation to lithology or structure | coincides with a contact or a fault |
| Steepness index upstream and downstream | similar on both sides after a single drop in base level, higher downstream (adjusted reach) than upstream (relict reach) after an increase in uplift rate | high only in the resistant unit, or different on the two sides of the fault |
| Associated landforms | terraces and steep inner gorge downstream, low-relief relict landscape upstream | none in particular |

{% include figure.html
    caption="Migrating knickpoints versus zones of differential uplift in a slope–area plot, in a longitudinal profile and in map view. (Source: Burbank and Anderson, 2011, modified after Wobus et al., 2006)"
    url="/figures/W3/knickpoint_propagation.png"
    class="row"
%}

## Influences on longitudinal profiles
- **Tectonics**: a higher rate of rock uplift requires a higher rate of incision, and the river achieves it by steepening. In steady state the profile keeps its concave shape, but its steepness index is higher. A change in the uplift rate creates a knickpoint that migrates upstream.
- **Base-level changes**: a fall in sea level or lake level induces incision that propagates upstream. A base-level rise leads to aggradation in the lower reaches.
- **Lithology**: resistant rocks require steeper slopes to be eroded at the same rate, so the profile is steeper where the river crosses them.
- **Climate**: precipitation controls discharge, and together with temperature and vegetation also the sediment supply from hillslopes. A wetter climate generally allows the river to do the same work on a gentler slope.
- **Sediment supply**: an increase in the amount or grain size of the supplied sediment leads to aggradation and steepening. A decrease leads to incision.
- **Dams**: a reservoir is a local base level and a sediment trap. Sediment accumulates upstream of the dam, while the sediment-starved river downstream of it incises.

## Summary
- A graded river has a smooth concave-up profile, on which slope is adjusted to transport the supplied sediment with the available discharge.
- Flint's law, $S = k_s A^{-\theta}$, describes the profile with two numbers: the concavity index $\theta$ (curvature of the profile) and the steepness index $k_s$ (steepness for a given drainage area).
- To compare rivers we use the normalized steepness index $k_{sn}$ calculated with a reference concavity.
- Knickpoints are departures from the graded profile. Mobile knickpoints record a change in base level or uplift rate and the time since it occurred. Fixed knickpoints record spatial differences in rock resistance or uplift rate.

# References
Burbank, D.W., Anderson, R.S., 2011. Tectonic Geomorphology, 2nd ed. Wiley-Blackwell, Chichester.

Flint, J.J., 1974. Stream gradient as a function of order, magnitude, and discharge. Water Resources Research 10, 969–973. https://doi.org/10.1029/WR010i005p00969

Gilbert, G.K., 1877. Report on the Geology of the Henry Mountains. U.S. Geographical and Geological Survey of the Rocky Mountain Region, Washington, D.C.

Mackin, J.H., 1948. Concept of the graded river. Geological Society of America Bulletin 59, 463–512. https://doi.org/10.1130/0016-7606(1948)59[463:COTGR]2.0.CO;2

Wobus, C., Whipple, K.X., Kirby, E., Snyder, N., Johnson, J., Spyropolou, K., Crosby, B., Sheehan, D., 2006. Tectonics from topography: Procedures, promise, and pitfalls, in: Willett, S.D., Hovius, N., Brandon, M.T., Fisher, D.M. (Eds.), Tectonics, Climate, and Landscape Evolution. Geological Society of America Special Paper 398, pp. 55–74. https://doi.org/10.1130/2006.2398(04)
