---
title: Week 4 – Chi Analysis and Transient Profiles
slug: Week4
abstract:
---

### Lecture 1: Chi Transformation
**Structure**
- **Introduction (5 min)**
  - Why chi analysis? Problem of nonlinear river profiles.
- **Core Concepts (25 min)**
  - Derivation of χ:
    - χ = ∫ (A0 / A)^m/n dx.
    - Normalization with reference area A0.
  - In steady state, χ–elevation plots are straight lines.
  - Disequilibrium: profile bends or breaks.
  - Sensitivity to m/n ratio choice.
- **Examples (10 min)**
  - Taiwan (active orogen) vs. Canadian Shield (stable craton).
- **Wrap-up (5–10 min)**
  - Quick discussion: What does a break in slope of χ-plot mean?



### Chi transformation - what is it and why we use it?

The Chi transformation is a mathematical approach used in geomorphology to analyze river profiles. It helps to identify and quantify changes in river morphology, particularly in response to tectonic or climatic forces. By transforming the river profile into a Chi plot, we can better understand the processes shaping the landscape.

We use the Chi transformation because it allows us to:

1. **Normalize river profiles**: By comparing different river segments on the same plot, we can identify patterns and anomalies more easily.
2. **Detect disequilibrium**: Changes in the slope of the Chi plot can indicate shifts in tectonic activity, sediment supply, or other factors influencing river behavior.
3. **Facilitate comparisons**: The Chi transformation enables us to compare river profiles across different regions and geological settings, providing insights into the underlying processes at work.

Overall, the Chi transformation is a valuable tool for understanding the complex interactions between tectonics, climate, and landscape evolution.

### How is the Chi transformation calculated?
The Chi transformation is calculated using the following integral formula:
$$ \chi = \int \left( \frac{A_0}{A(x)} \right)^{m/n} dx $$

Where:
- \( \chi \) is the Chi value at a given point along the river profile.
- \( A_0 \) is a reference drainage area (a constant).
- \( A(x) \) is the drainage area at point \( x \) along the river.
- \( m/n \) is the channel concavity index, which reflects the relationship between channel slope and drainage area.
- \( dx \) is a small segment of the river profile.
- The integral is evaluated from the river mouth (downstream) to the point of interest (upstream).
- The choice of \( m/n \) is crucial, as it influences the shape of the Chi plot. A common value used in many studies is \( m/n = 0.5 \), but this can vary depending on the specific characteristics of the river system being analyzed.
- By calculating the Chi values along the river profile, we can create a Chi-elevation plot, which helps to visualize and interpret the geomorphic processes affecting the river system.
- In a steady-state river profile, the Chi-elevation plot will appear as a straight line. Deviations from this linearity indicate disequilibrium conditions, such as changes in tectonic uplift rates or sediment supply.
- Overall, the Chi transformation provides a powerful framework for analyzing river profiles and understanding the dynamics of landscape evolution.

### Interpretation of Chi plots
Chi plots are graphical representations that plot the Chi values against elevation along a river profile. They are used to analyze the geomorphic state of river systems and to identify disequilibrium conditions. Here’s how to interpret Chi plots:




---
### Lab 4: Chi Analysis of River Networks
**Objectives**
- Gain hands-on skills in χ analysis.
- Learn to detect disequilibrium landscapes.

**Steps**
1. **Load DEM** and delineate catchments.
2. **Run χ-analysis tool** in TopoToolbox or Python script.
3. **Generate χ–elevation plots** for main stem and tributaries.
4. **Interpret breaks and slope changes**.
5. **Exercise**
   - Write a short interpretation: tectonic vs. lithologic vs. climatic control.

---