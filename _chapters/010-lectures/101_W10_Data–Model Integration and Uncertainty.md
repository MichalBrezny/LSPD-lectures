---
title: W10 – Data–Model Integration and Uncertainty 2
slug: week10-data-model-integration-uncertainty2
abstract:
---

## Sensitivity Analysis

### What Is Sensitivity?
- Response of model output to parameter changes.
- Key SPIM/LEM parameters:
  - uplift rate (U),
  - erodibility (K),
  - concavity (m/n),
  - diffusion coefficient (D).

Understanding sensitivity helps identify which parameters most influence model behavior and where to focus data collection efforts. For example if subtle changes in $K$ lead to large changes in incision rates, then accurate estimation of $K$ is critical.

## How to Perform Sensitivity Analysis?

### One-At-a-Time Sensitivity
- Change one parameter while others fixed.
- Observe:
  - incision depth,
  - profile shape,
  - transient response time.
- Emphasis:
  - patterns, not exact values.

### Monte Carlo Simulations
- Randomly sample parameter space.
- Generate ensemble of model runs.
- Analyze distribution of outputs.
- Benefits:
  - captures interactions between parameters,
  - quantifies uncertainty ranges.
  - Identifies equifinality (multiple parameter sets yield similar results).
  - Helps assess robustness of interpretations.
  - Visualize uncertainty with confidence intervals or probability density functions.
  

## Sources of Uncertainty

### Data Uncertainty
DEM errors:
- resolution,
- vegetation bias.

For details see previous lectures on DEM processing.

Measurement uncertainty:
  - cosmogenic inheritance,
  - sediment yield variability.

### Model Structural Uncertainty
- Simplified physics:
  - SPIM assumptions,
  - absence of sediment cover.
- Scale mismatch:
  - model grid vs. real landscape.


### Conceptual Uncertainty
- Incorrect process dominance.
- Over-interpreting metrics.
- Assuming steady state where none exists.


### Interpreting Model–Data Agreement 

- Good agreement may indicate:
  - plausible forcing,
  - reasonable parameter choices.
- Poor agreement may indicate:
  - missing processes,
  - wrong boundary conditions,
  - transient landscape.
- Important message:
  > *Disagreement is informative, not failure.*

