---
title: W6 – Stream Power Incision Model – Theory and Implementation
slug: week6-stream-power-incision-model
abstract:
---



# Introduction: Closing the Loop 

In the previous weeks we have built a chain of observations:
- Tectonic uplift produces relief (W4).
- Rivers respond by steepening and incising (W3, W4).
- $\chi$ analysis and the steepness index *quantify the response* (W5).

All of these were descriptions. We measured that rivers in rapidly uplifting areas are steeper, and that steady-state profiles are straight lines in $\chi$ space, but we have not explained why. The key question of this week is:

> *What physical process explains the patterns we observe in chi space?*

The answer is a model of river incision into bedrock. The simplest one, and the one most widely used, is the stream power incision model (SPIM).

---

# Fluvial incision

Fluvial incision is a dominant erosion process in many landscapes. Bedrock rivers set the lower boundary for hillslopes, so the rate at which they incise controls the erosion rate of the whole landscape. The Stream Power Incision Model (SPIM) provides a framework to quantify how rivers erode their beds based on drainage area and channel slope. In this lecture, we will explore the theoretical basis of SPIM, its relationship to $\chi$ and $k_{sn}$, and its assumptions and limitations.

## Conceptual Foundation of SPIM

### Rivers as Energy Dissipation Systems
Water flowing downhill loses gravitational potential energy. Part of this energy becomes the kinetic energy of the flow, and most of it is dissipated by friction on the bed and banks and by turbulence. A small part does geomorphic work: it moves sediment and erodes the bed, by plucking blocks of rock and by abrasion of the bed by transported grains.

The more energy a river dissipates on a unit area of its bed, the faster we can expect it to erode. The erosion rate should therefore depend on:
- the water discharge,
- the channel slope,
- the resistance of the bedrock.

### The Stream Power Concept

The rate of energy dissipation per unit length of a channel is the **total stream power** (W/m):

$$ \Omega = \rho g Q S $$

where:
- $\rho$ is the water density (kg/m³),
- $g$ is the gravitational acceleration (m/s²),
- $Q$ is the discharge (m³/s),
- $S$ is the channel slope (m/m).

For erosion it is more relevant how much power acts on a unit area of the bed. This is the **unit stream power** (W/m²), obtained by dividing the total stream power by the channel width $W$:

$$ \omega = \frac{\rho g Q S}{W} $$

For example, a river with a discharge of 100 m³/s, a slope of 0.01 and a width of 20 m has a total stream power of about 9800 W/m and a unit stream power of about 490 W/m².

## Governing Equation and Its Meaning 

### From stream power to SPIM
The stream power incision model is based on the idea that the rate of river incision ($E$) is proportional to the unit stream power (Howard and Kerby, 1983; Whipple and Tucker, 1999). Discharge and channel width are not known along whole river networks, but both can be estimated from drainage area:

- discharge increases with drainage area, $Q = k_q A^c$, with $c \approx 1$ under uniform precipitation,
- channel width increases with discharge, $W = k_w Q^b$, with $b \approx 0.5$.

If the incision rate is a power function of the unit stream power, $E = k_e \omega^a$, substituting the two relationships gives the usual form of the model:

$$E = KA^mS^n$$

where:
- $E$ = incision rate (m/yr),
- $K$ = erodibility coefficient,
- $A$ = drainage area (m²),
- $S$ = channel slope (m/m),
- $m$, $n$ = positive exponents that describe how incision scales with area and slope.

The derivation shows where the parameters come from: $n = a$, $m = a c (1 - b)$, and all the constants ($\rho$, $g$, $k_q$, $k_w$, $k_e$) are collected in $K$. The ratio of the exponents is

$$ \frac{m}{n} = c\,(1 - b) \approx 0.5 $$

It depends only on the hydrology and the geometry of the channel and not on the erosion process. This is the reason why the concavity index of rivers is so similar in very different landscapes.

### Physical Interpretation of Parameters
- **$K$ (erodibility)** expresses how efficiently a river erodes its bed. It increases with decreasing rock strength and with increasing precipitation (more discharge from the same area), and it also includes the effects of sediment load and channel geometry. Its values span several orders of magnitude (Stock and Montgomery, 1999). Its units depend on $m$: they are $\mathrm{m}^{1-2m}\,\mathrm{yr}^{-1}$, which is $\mathrm{yr}^{-1}$ for $m = 0.5$. Values of $K$ calculated with different $m$ therefore cannot be compared.
- **$n$ (slope exponent)** depends on the erosion process. Theoretical values range from about 2/3 to 5/3 (Whipple and Tucker, 1999). The value $n = 1$ is used very often, mainly because it makes the equation linear, but field data from many regions suggest that $n$ is larger than 1 (Lague, 2014).
- **$m/n$ ratio** controls the concavity of the profile and directly links SPIM to the $\chi$ transformation.
- **$U$ (rock uplift rate)** is not a parameter of SPIM itself. It is the external forcing against which incision works.

The parameters are usually treated as constants, but they vary in space and time. Erodibility differs between lithologies, and it can differ between glacial and interglacial periods.

### Evolution of a river profile
The elevation of a point on the river bed changes as a result of the competition between rock uplift and incision:

$$ \frac{\partial z}{\partial t} = U - K A^m S^n $$

where $z$ is the elevation of the bed, $t$ is time and $S = \partial z / \partial x$ is the slope, with the distance $x$ measured upstream. This is the governing equation of the detachment-limited river and the core of most landscape evolution models (W7). It is solved with a boundary condition at the downstream end of the river, which is the base level.

---

## SPIM, Chi, and Steady State

### Steady-state profile
In steady state the elevation does not change, $\partial z / \partial t = 0$, and incision balances uplift everywhere along the river:

$$ U = K A^m S^n $$

Rearranging for the slope gives

$$ S = \left( \frac{U}{K} \right)^{1/n} A^{-m/n} $$

This is exactly Flint's law, $S = k_s A^{-\theta}$, which we introduced in W3 as an empirical relationship. SPIM gives a physical meaning to both of its parameters:

$$ \theta = \frac{m}{n} \qquad\qquad k_s = \left( \frac{U}{K} \right)^{1/n} $$

### Why Chi Linearizes SPIM
The steady-state profile is obtained by integrating the slope upstream from the base level $x_b$, with uniform $U$ and $K$:

$$ z(x) = z_b + \left( \frac{U}{K A_0^m} \right)^{1/n} \chi \qquad \text{with} \qquad \chi = \int_{x_b}^{x} \left( \frac{A_0}{A(x')} \right)^{m/n} dx' $$

All the dependence on the shape of the river network is hidden in $\chi$, and what remains is the equation of a straight line. Its slope is $(U/K)^{1/n} A_0^{-m/n}$, which equals the steepness index for $A_0 = 1\ \mathrm{m^2}$ (Perron and Royden, 2013).

> *Chi is mathematically consistent with SPIM under steady-state assumptions.*

The $\chi$ transformation is therefore not an arbitrary mathematical trick. It is the coordinate in which the steady-state solution of SPIM is linear. This also explains the assumptions listed in W5: the profile is straight only if $U$ and $K$ are uniform and if the correct $m/n$ is used.

### What Steepness (ksn) Means Physically
The steepness index reflects the slope that the river needs to balance uplift:
- A higher uplift rate requires faster incision and therefore a steeper channel: higher $U$ → higher $k_{sn}$.
- More resistant rock or a drier climate make incision less efficient, and a steeper channel is needed to achieve the same rate: lower $K$ → higher $k_{sn}$.

Steepness is thus a *relative measure* of incision demand. It reflects the ratio $U/K$ and not $U$ alone.

The exponent $n$ determines how sensitive steepness is to uplift. With $n = 1$ the steepness is proportional to the uplift rate. With $n = 2$ a fourfold increase in the uplift rate only doubles the steepness.

---

## Transient Landscapes and SPIM 

Landscapes are rarely in perfect steady state. SPIM also predicts what happens after the forcing changes.

For $n = 1$ the governing equation can be written as

$$ \frac{\partial z}{\partial t} + K A^m \frac{\partial z}{\partial x} = U $$

This is a wave (advection) equation. It says that any change of the profile travels upstream as a wave with the velocity (celerity)

$$ C = K A^m $$

After an increase in the uplift rate, the river first steepens only at its downstream end. The boundary between the steepened lower reach and the unchanged upper reach is a knickpoint, and it migrates upstream with the celerity $C$. SPIM thus predicts both the rate of knickpoint retreat and the pattern of incision through time.

Three consequences follow:
- The celerity increases with drainage area. Knickpoints move fast in large rivers and slow down as they enter small tributaries (as described in W3).
- For $n = 1$ the celerity does not depend on the slope or on the height of the knickpoint, so the knickpoint keeps its shape. For $n \neq 1$ the celerity is $C = K A^m S^{n-1}$, and the shape of the knickpoint changes as it migrates (Royden and Perron, 2013).
- The time a knickpoint needs to travel from the base level to a point $x$ is

$$ \tau(x) = \int_{x_b}^{x} \frac{dx'}{K A(x')^m} = \frac{\chi}{K A_0^m} $$

The response time is proportional to $\chi$. This is why knickpoints generated by one event are found at the same $\chi$ in all tributaries, and why $\chi$ at the channel head is a measure of the response time of the whole river (Whipple and Tucker, 1999).

In $\chi$ space, deviations from a straight line show where the balance between uplift and incision is violated.

---

## Assumptions and Limitations

SPIM assumes:
- **detachment-limited incision**: the incision rate is limited by the ability of the river to detach bedrock, and all eroded material is carried away,
- a simple scaling of discharge and channel width with drainage area,
- spatially uniform climate (to first order),
- one effective discharge that represents the whole range of floods.

SPIM does **not**:
- account for sediment explicitly. Sediment has two opposite effects: grains are the tools that abrade the bed, and a continuous cover of sediment protects it (Sklar and Dietrich, 2001). 
- resolve the dynamics of channel width, although rivers are known to narrow in zones of fast uplift,
- include an erosion threshold and the variability of floods. If only large floods are able to erode the bed, the relationship between steepness and erosion rate becomes non-linear, which appears as $n > 1$ (Lague, 2014).

> *SPIM explains first-order patterns, not all details.*

---

## Summary
- SPIM assumes that the incision rate is a power function of drainage area and slope, $E = K A^m S^n$. It can be derived from unit stream power.
- In steady state, SPIM gives Flint's law with $\theta = m/n$ and $k_s = (U/K)^{1/n}$, and a straight line in $\chi$ space.
- In transient state, changes travel upstream as knickpoints with a celerity that increases with drainage area. The response time is proportional to $\chi$.
- SPIM gives a physical basis to $\chi$ and $k_{sn}$ and a bridge from observation to modelling. In the next lecture we will apply it to real rivers, and in W7 we will implement it numerically in landscape evolution models.

# References
Howard, A.D., Kerby, G., 1983. Channel changes in badlands. Geological Society of America Bulletin 94, 739–752. https://doi.org/10.1130/0016-7606(1983)94<739:CCIB>2.0.CO;2

Lague, D., 2014. The stream power river incision model: evidence, theory and beyond. Earth Surface Processes and Landforms 39, 38–61. https://doi.org/10.1002/esp.3462

Perron, J.T., Royden, L., 2013. An integral approach to bedrock river profile analysis. Earth Surface Processes and Landforms 38, 570–576. https://doi.org/10.1002/esp.3302

Royden, L., Perron, J.T., 2013. Solutions of the stream power equation and application to the evolution of river longitudinal profiles. Journal of Geophysical Research: Earth Surface 118, 497–518. https://doi.org/10.1002/jgrf.20031

Sklar, L.S., Dietrich, W.E., 2001. Sediment and rock strength controls on river incision into bedrock. Geology 29, 1087–1090. https://doi.org/10.1130/0091-7613(2001)029<1087:SARSCO>2.0.CO;2

Stock, J.D., Montgomery, D.R., 1999. Geologic constraints on bedrock river incision using the stream power law. Journal of Geophysical Research: Solid Earth 104, 4983–4993. https://doi.org/10.1029/98JB02139

Whipple, K.X., Tucker, G.E., 1999. Dynamics of the stream-power river incision model: Implications for height limits of mountain ranges, landscape response timescales, and research needs. Journal of Geophysical Research: Solid Earth 104, 17661–17674. https://doi.org/10.1029/1999JB900120
