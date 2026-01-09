---
title: W5 – Chi Analysis and Transient Profiles
slug: week5-chi-analysis-transient-profiles
abstract:
---

# Chi Transformation
<!-- **Structure**
- **Introduction**
  - Why chi analysis? Problem of nonlinear river profiles.
- **Core Concepts**
  - Derivation of χ:
    - χ = ∫ (A0 / A)^m/n dx.
    - Normalization with reference area A0.
  - In steady state, χ–elevation plots are straight lines.
  - Disequilibrium: profile bends or breaks.
  - Sensitivity to m/n ratio choice.
- **Examples**
  - Taiwan (active orogen) vs. Canadian Shield (stable craton).
- **Wrap-up**
  - Quick discussion: What does a break in slope of χ-plot mean?
-->

### Chi transformation - what is it and why we use it?
River profiles are inherently nonlinear due to the relationship between channel slope and drainage area. As rivers flow downstream, their slope typically decreases because the discharge increases with drainage area. This nonlinearity makes it challenging to compare river profiles directly or to assess their response to tectonic or climatic forcing.

The Chi transformation is a mathematical approach used in geomorphology to analyze river profiles. It helps to identify and quantify changes in river morphology, particularly in response to tectonic or climatic forces. By transforming the river profile into a Chi plot, we can better understand the processes shaping the landscape.

We use the Chi transformation because it allows us to:

1. **Normalize river profiles**: By comparing different river segments on the same plot, we can identify patterns and anomalies more easily.
2. **Detect disequilibrium**: Changes in the slope of the Chi plot can indicate shifts in tectonic activity, sediment supply, or other factors influencing river behavior.
3. **Facilitate comparisons**: The Chi transformation enables us to compare river profiles across different regions and geological settings, providing insights into the underlying processes at work.

Overall, the Chi transformation is a valuable tool for understanding the complex interactions between tectonics, climate, and landscape evolution.

### How is the Chi transformation calculated?
The Chi transformation is calculated using the following integral formula:
$$ \chi = \int \left( \frac{A_0}{A(x)} \right)^{m/n} dx $$

- $\chi$ is the Chi value at a given point along the river profile.
- $A_0$ is a reference drainage area (a constant).
- $A(x)$ is the drainage area at point $x$ along the river.
- $m/n$ is the channel concavity index, which reflects the relationship between channel slope and drainage area.
- $dx$ is a small segment of the river profile.
  
- The integral is evaluated from the river mouth (downstream) to the point of interest (upstream).
- The choice of $m/n$ is crucial, as it influences the shape of the Chi plot. A common value used in many studies is $m/n = 0.45$ to $0.5$, but this can vary depending on the specific characteristics of the river system being analyzed.

>[!IMPORTANT]
>Main assumptions: Uplift rate and erodibility are uniform spatially.  


>[!NOTE]
>For the details of Chi transformation derivation see (Mudd et al., 2014)

- By calculating the Chi values along the river profile, we can create a Chi-elevation plot, which helps to visualize and interpret the geomorphic processes affecting the river system.
- In a **steady-state river profile**, the Chi-elevation plot will appear as a **straight line**. Deviations from this linearity indicate disequilibrium conditions, such as changes in tectonic uplift rates or sediment supply.
- Overall, the Chi transformation provides a powerful framework for analyzing river profiles and understanding the dynamics of landscape evolution.

{% include figure.html
    caption="Sketch illustrating examples of linearity or nonlinearity of channels in χ-elevation space. Channel networks with spatially homogenous uplift and erodibility that are at steady state should have channels that are not just linear but collinear (after Mudd et al., 2014)."
    url="/figures/chi_plot_linear.jpg"
    class="row"}
%}

### Interpretation of Chi plots
Chi plots are graphical representations that plot the Chi values against elevation along a river profile. They are used to analyze the geomorphic state of river systems and to identify disequilibrium conditions. Here’s how to interpret Chi plots:

### Slope area vs Chi plots
- **Slope-Area Plots**: These plots show the relationship between channel slope (S) and drainage area (A). They are often used to assess the concavity of river profiles and to infer tectonic or climatic influences. However, slope-area plots can be noisy and difficult to interpret, especially when comparing different river systems.
- **Chi Plots**: In contrast, Chi plots transform the river profile into a linear space, making it easier to identify patterns and anomalies. In a Chi plot, the x-axis represents the Chi values, while the y-axis represents elevation. A straight line in a Chi plot indicates a steady-state river profile, while deviations from linearity suggest disequilibrium conditions.



<!-- 
## Lecture 1: Why Chi? From Tectonic Forcing to River Profiles

### 1. Introduction: The Problem We Are Trying to Solve (10 min)
- Recap from tectonic geomorphology:
  - Tectonic uplift creates relief.
  - Rivers respond by adjusting slope and incision rate.
- Key difficulty:
  - River profiles are **nonlinear**.
  - Slope varies systematically with drainage area.
- Central question:
  > *How can we objectively compare rivers and quantify their response to tectonic forcing?*
- Chi analysis is introduced as a **coordinate transformation**, not a new process.

---

### 2. Rivers as Tectonic Sensors (15 min)

#### 2.1 Conceptual Link
- Uplift increases erosion demand.
- Rivers steepen to keep up with uplift.
- Steepness is therefore a **proxy**, not a direct measurement.

#### 2.2 Why Slope Alone Is Not Enough
- Channel slope decreases downstream due to increasing discharge.
- Two rivers with the same uplift rate can have very different slopes.
- Need to normalize slope for drainage area.

---

### 3. From Slope–Area to Chi (25 min)

#### 3.1 Slope–Area Scaling
- Empirical relationship:
  - S ∝ A^(-θ)
- Interpretation:
  - θ reflects concavity.
  - k reflects channel steepness.
- Problem:
  - Slope–area plots are noisy and difficult to compare across basins.

#### 3.2 The Idea Behind Chi
- Replace downstream distance with an **integrated drainage-area coordinate**.
- Chi accumulates the effect of drainage area upstream.
- Key idea:
  > *If uplift and erodibility are uniform, river profiles become linear in chi space.*

---

### 4. Physical Meaning of Chi (20 min)

#### 4.1 What Chi Represents
- Chi is proportional to:
  - time-integrated erosion potential,
  - normalized upstream incision demand.
- Higher chi values upstream = greater cumulative resistance to incision.

#### 4.2 What a Linear Chi Profile Means
- Linear χ–elevation profile implies:
  - steady-state conditions,
  - balance between uplift and incision,
  - spatially uniform forcing (within assumptions).

#### 4.3 What Breaks in Chi Mean
- Changes in slope of χ–z plot indicate:
  - transient adjustment,
  - uplift rate change,
  - base-level perturbation,
  - drainage reorganization.

---

### 5. Assumptions and Limits (15 min)

- Assumes:
  - detachment-limited incision,
  - power-law erosion,
  - uniform climate and lithology (first order).
- Chi does **not**:
  - prove active tectonics,
  - give absolute uplift rates,
  - replace field observations.
- Emphasize:
  > *Chi quantifies response, not cause.*

---

### 6. Wrap-up & Transition (5 min)
- Chi is a **formalization** of ideas introduced in tectonic geomorphology.
- Sets stage for:
  - channel steepness indices (ksn),
  - SPIM parameters,
  - landscape evolution modeling.

---
-->


## References
Mudd, S.M., Attal, M., Milodowski, D.T., Grieve, S.W.D., Valters, D.A., 2014. A statistical framework to quantify spatial variation in channel gradients using the integral method of channel profile analysis. Journal of Geophysical Research: Earth Surface 119, 138–152. https://doi.org/10.1002/2013JF002981
