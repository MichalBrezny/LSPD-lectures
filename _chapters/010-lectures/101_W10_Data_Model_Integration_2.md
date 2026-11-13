---
title: W10 – Data–Model Integration and Uncertainty 2
slug: week10-data-model-integration-uncertainty2
abstract:
---

# Sensitivity and Uncertainty

In the first part of this week we saw that data constrain models and that different combinations of parameters can produce similar landscapes (equifinality). Two practical questions follow. Which parameters actually matter for the result? And how much can we trust the result when the parameters and the data are uncertain? The first question is answered by sensitivity analysis and the second one by uncertainty analysis.

## Sensitivity Analysis

### What Is Sensitivity?
Sensitivity is the response of a model output to a change in a model input. A model is sensitive to a parameter if a small change in the parameter leads to a large change in the output. The key parameters of the stream power incision model (SPIM) and of the landscape evolution models (LEMs) that we used are:
- uplift rate ($U$),
- erodibility ($K$),
- concavity ($m/n$) and the slope exponent ($n$),
- diffusion coefficient ($D$).

Understanding sensitivity helps identify which parameters most influence model behavior and where to focus data collection efforts. For example, if subtle changes in $K$ lead to large changes in incision rates, then accurate estimation of $K$ is critical. A parameter to which the output is not sensitive can be fixed at a reasonable value, and there is no need to spend time and money on measuring it precisely.

Sensitivity depends on which output we look at. The steady-state steepness of a river, $k_{sn} = (U/K)^{1/n}$, is a good example:

- With $n = 1$, doubling the uplift rate doubles the steepness and therefore also the fluvial relief. With $n = 2$, the same change increases the steepness only by about 41 % ($\sqrt{2} \approx 1.41$). The sensitivity to $U$ depends on the value of another parameter.
- The steepness depends only on the ratio $U/K$. If we double both $U$ and $K$, the steady-state profile does not change at all. The time needed to reach it, however, becomes shorter, because the response time decreases with increasing $K$. Steady-state topography is thus insensitive to a change to which the transient behaviour is sensitive.
- The diffusion coefficient $D$ has almost no effect on river profiles, but it controls the shape of hillslopes: a higher $D$ gives smoother and more rounded hillslopes.

## How to Perform Sensitivity Analysis?

### One-At-a-Time Sensitivity
The simplest approach is to change one parameter while all the others are kept fixed at their reference values:

1. Define a reference run with the best estimates of all parameters.
2. Choose a plausible range for each parameter, e.g., from the literature.
3. Run the model repeatedly, changing only one parameter within its range.
4. Compare the outputs with the reference run, for example the incision depth, the profile shape (steepness, concavity, position of knickpoints) and the transient response time.

The emphasis is on patterns and not on exact values: does the output increase or decrease, is the response linear, is there a threshold?

The one-at-a-time approach is cheap and easy to interpret, which makes it a good first step. Its limitation is that it explores only a small part of the parameter space around the reference run, and it cannot detect interactions between parameters. As we saw above, the effect of $U$ depends on $n$ and can be compensated by $K$. This cannot be seen when each parameter is changed separately.

### Monte Carlo Simulations
Monte Carlo simulation changes all parameters at the same time:

1. Define a range or a probability distribution for each uncertain parameter.
2. Draw a random set of parameter values and run the model with it.
3. Repeat it many times, typically hundreds to thousands of runs, to generate an ensemble of model runs.
4. Analyze the distribution of the outputs and their relation to the parameters.

Benefits:
- It captures the interactions between parameters.
- It quantifies the range of uncertainty of the outputs. The result is not one number but a distribution, which can be shown as a confidence interval, a probability density function or an envelope of profiles.
- It identifies equifinality. If each run is compared with the observations, e.g., by the root-mean-square error between the modelled and the observed river profile, we usually find many different parameter sets that fit the data equally well (Beven, 2006).
- It helps to assess the robustness of the interpretation. A conclusion that holds for all acceptable parameter sets is robust.

The price is the computational cost. A model that runs for an hour cannot be run ten thousand times, so the size of the ensemble is a compromise. The number of necessary runs can be reduced by more efficient sampling strategies, e.g., Latin hypercube sampling, which covers the parameter space more evenly than purely random sampling.

> [!NOTE]
> The result of a Monte Carlo analysis depends on the ranges chosen in the first step. Ranges that are too narrow give a false impression of certainty.

## Sources of Uncertainty

Uncertainty enters the modelling at three levels: in the data, in the structure of the model, and in our concept of how the landscape works. They are ordered here from the one that is easiest to quantify to the one that is hardest.

### Data Uncertainty
**DEM errors.** All topographic metrics inherit the errors of the DEM from which they were calculated:
- resolution: coarse DEMs underestimate slopes and smooth out narrow valleys and knickpoints,
- vegetation and building bias in DEMs that are in fact surface models,
- artefacts, voids and the effects of hydrological conditioning.

For details see the previous lectures on DEM processing (W2).

**Measurement uncertainty.** The data used to constrain rates have their own uncertainties, which are often larger than those of the topography:
- Cosmogenic nuclides: besides the analytical error, the calculation of erosion rates assumes steady erosion and well-mixed sediment. Large landslides, nuclides inherited from an earlier period of exposure or an uneven distribution of quartz in the basin violate these assumptions.
- Sediment yields: they vary strongly from year to year, the records are short and often affected by dams and land use, and rare large events may be missing.
- Different methods average over different timescales, from decades (gauging) through thousands of years (cosmogenic nuclides) to millions of years (thermochronology). A disagreement between them may be a real change of rates in time and not an error.

### Model Structural Uncertainty
Every model is a simplification, and the simplifications are a source of uncertainty that remains even with perfect data and perfectly known parameters.

- Simplified physics:
  - SPIM assumes detachment-limited incision, discharge proportional to drainage area and no erosion threshold,
  - sediment is ignored, although it can both protect the bed (cover effect) and erode it (tools effect),
  - channel width is not modelled explicitly.
- Scale mismatch between the model grid and the real landscape: a channel a few metres wide is represented by a cell tens to hundreds of metres wide, and processes that operate below the grid resolution have to be parameterized.
- Simplified boundary and initial conditions: uniform uplift, constant climate, an arbitrary initial surface.

Structural uncertainty is difficult to quantify. In practice it is assessed by comparing models with different process laws.

### Conceptual Uncertainty
The most serious errors are made before the model is run, in the choice of what to model and how to read the results:
- Incorrect process dominance: for example, a fluvial model applied to a landscape that was shaped mainly by glaciers or debris flows.
- Over-interpreting metrics: reading every $k_{sn}$ anomaly as tectonic (see W5).
- Assuming steady state where none exists: many methods, including the estimation of uplift from $k_{sn}$, are valid only in steady state.

No sensitivity analysis can reveal a conceptual error, because all runs of the ensemble share it. The only protection is independent evidence and a critical evaluation of alternative hypotheses.

## Interpreting Model–Data Agreement 

- Good agreement may indicate:
  - a plausible forcing,
  - reasonable parameter choices.
- Poor agreement may indicate:
  - missing processes,
  - wrong boundary conditions,
  - a transient landscape.

Good agreement shows that the model is *consistent* with the data. It does not prove that the model is correct, because another model or another parameter set might fit equally well (Oreskes et al., 1994). On the other hand, poor agreement is a clear result: something in the model, in the data or in our assumptions is wrong, and finding out what it is often teaches us more than a good fit.

> *Disagreement is informative, not failure.*

### Good Practice
- State all assumptions and parameter values, including those that were fixed.
- Report ranges and distributions and not single values.
- Show which parameters control the result.
- Test the model against data that were not used to constrain it.
- Distinguish clearly between what the data show and what the model suggests.

## Summary
- Sensitivity analysis shows which parameters control the model output. The one-at-a-time approach is simple but misses the interactions between parameters, which Monte Carlo simulations capture.
- Uncertainty comes from the data, from the structure of the model and from our concepts. Only the first one is easy to quantify.
- Agreement between model and data means consistency and not proof, and disagreement is a source of information.

# References
Beven, K., 2006. A manifesto for the equifinality thesis. Journal of Hydrology 320, 18–36. https://doi.org/10.1016/j.jhydrol.2005.07.007

Oreskes, N., Shrader-Frechette, K., Belitz, K., 1994. Verification, validation, and confirmation of numerical models in the earth sciences. Science 263, 641–646. https://doi.org/10.1126/science.263.5147.641
