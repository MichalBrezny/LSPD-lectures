---
title: W5 – Application of Chi Analysis
slug: week5-application-chi
abstract:
---
<!--
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

### Lecture 2: Applications of Chi Analysis
**Structure**
- **Introduction (5 min)**
  - Using chi for tectonic interpretation.
- **Core Concepts (25 min)**
  - Channel steepness index (ksn) as proxy for uplift rate.
  - Identifying disequilibrium: tributary mismatches, knickpoints.
  - Detecting drainage divides migration.
  - Limitations: lithologic heterogeneity, climate variability.
- **Examples (10 min)**
  - Himalayas: high ksn near thrust fronts.
  - Appalachians: low ksn, stable divide.
- **Wrap-up (5–10 min)**
  - Small group exercise: interpret a χ plot of a sample basin.

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

-->>

# Interpreting Chi and Channel Steepness in Tectonic Context

## 1. Introduction: From Transformation to Interpretation (5 min)
- Chi transforms river profiles.
- Interpretation requires tectonic context.
- Reminder:
  > *Metrics do not interpret themselves.*

## Channel Steepness (ksn) Revisited

## What ksn Actually Represents
- ksn combines:
  - slope,
  - drainage area normalization,
  - assumed concavity (θref).
- Conceptual meaning:
  - relative measure of erosion demand.

## ksn and Uplift
- Higher uplift → higher required incision → higher ksn.
- Spatial patterns of ksn reflect:
  - fault zones,
  - uplift gradients,
  - tectonic segmentation.

---

## Detecting Tectonic Signals with Chi (25 min)

## Knickpoints in Chi Space
- Vertical offsets in χ–z plots.
- Interpreting:
  - migrating knickpoints (uplift or base-level change),
  - stationary knickpoints (lithologic control).

## Tributary Consistency
- In steady state:
  - tributaries align with main stem in chi space.
- Misalignment indicates:
  - transient response,
  - divide migration,
  - drainage capture.

---

## What Can Go Wrong 

## Lithologic Effects
- Resistant rock can mimic tectonic signal.
- Importance of independent geological information.

## Climatic Modulation
- Precipitation gradients affect discharge–area scaling.
- Chi assumes constant runoff efficiency.

## Choice of m/n Ratio
- Sensitivity to concavity index.
- Why standard values (e.g. 0.45–0.6) are used.

---

## Integrating Chi with Other Indicators

- Best practice:
  - chi + ksn + hypsometry + basin asymmetry.
- Spatial coherence:
  - alignment with mapped faults.
- Temporal reasoning:
  - knickpoint position as response time indicator.

---

##  Wrap-up & Transition to SPIM

- Key messages:
  - Chi quantifies tectonic response in river networks.
  - Interpretation must be cautious and contextual.
- Explicit bridge to SPIM:
  > *SPIM provides the process-based framework that explains why chi works.*