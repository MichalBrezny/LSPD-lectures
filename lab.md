# Lab Outlines

This document provides outlines for weekly laboratory sessions, each designed for approximately 90 minutes, complementing the lecture material.

## Week 1 Lab: Introduction to Quantitative Geomorphology & Basic DEM Analysis (90 minutes)

**Objectives:**
*   Familiarize with a GIS environment (e.g., QGIS or SAGA GIS) for geomorphic analysis.
*   Understand and extract fundamental terrain metrics from Digital Elevation Models (DEMs).
*   Relate terrain metrics to basic hydrological concepts.

**Pre-lab Preparation:**
*   Ensure QGIS (or SAGA GIS) is installed and functional.
*   Review Lecture W1-systems and W1-quantitative.
*   Download the provided sample DEM data for the lab (link/location to be provided separately).

**Activities:**

**Part 1: Setting up the Environment & Exploring DEMs (30 minutes)**
1.  **Introduction to GIS Software (10 min):** Briefly review the interface of QGIS/SAGA GIS. Load the provided sample DEM.
2.  **DEM Visualization (10 min):** Experiment with different symbologies (e.g., hillshade, pseudocolor) to visualize the topography. Discuss the information conveyed by a DEM.
3.  **Basic DEM Information (10 min):** Inspect DEM properties (resolution, extent, coordinate system).

**Part 2: Deriving Basic Terrain Metrics (45 minutes)**
1.  **Slope Calculation (15 min):** Calculate slope (in degrees or percent) from the DEM. Discuss the interpretation of slope values.
2.  **Aspect Calculation (15 min)::** Calculate aspect from the DEM. Discuss its importance for solar radiation and microclimates.
3.  **Curvature (15 min):S** Calculate profile and planform curvature. Interpret what different curvature values represent in terms of water flow and erosion/deposition.

**Part 3: Discussion & Wrap-up (15 minutes)**
*   **Interpretation:** Discuss how the derived terrain metrics can be used to describe the landscape and infer geomorphic processes.
*   **Real-world Relevance:** Briefly discuss how these metrics are used in various fields (e.g., hazard assessment, land-use planning).
*   **Preview for next week:** Introduce the idea of using these metrics for hydrological analysis.

## Week 2 Lab: Hydrological Analysis from DEMs & Stream Networks (90 minutes)

**Objectives:**
*   Apply flow routing algorithms to DEMs to determine flow direction and accumulation.
*   Extract stream networks and delineate drainage basins.
*   Calculate stream orders and understand their significance.

**Pre-lab Preparation:**
*   Review Lectures W2-DEM_Terrain_metrics and W2-hydrology.
*   Have the processed DEM from Week 1 Lab available.

**Activities:**

**Part 1: Flow Routing & Accumulation (40 minutes)**
1.  **Pit Filling (15 min):** Understand why pit filling is necessary for hydrological analysis. Apply a pit-filling algorithm to the DEM.
2.  **Flow Direction (15 min):** Apply the D8 (or similar) flow direction algorithm. Visualize and interpret the output.
3.  **Flow Accumulation (10 min):** Calculate flow accumulation. Visualize the result and discuss how high accumulation values indicate potential stream channels.

**Part 2: Stream Network Extraction & Ordering (35 minutes)**
1.  **Stream Network Delineation (15 min):** Extract stream networks from the flow accumulation grid using a user-defined threshold. Discuss the impact of different thresholds on the resulting network density.
2.  **Stream Ordering (20 min):** Apply the Strahler (or similar) stream ordering method to the extracted network. Interpret the hierarchy of streams.

**Part 3: Discussion & Wrap-up (15 minutes)**
*   **Basin Delineation (Optional Demo):** Briefly demonstrate how to delineate a watershed for a specific outlet point.
*   **Interpretation:** Discuss how the extracted stream networks and ordering provide insights into hydrological processes and landscape organization.
*   **Challenges:** Discuss potential challenges and limitations of DEM-based hydrological analysis (e.g., DEM resolution, flat areas).

## Week 3 Lab: River Profiles and Drainage Metrics (90 minutes)

**Objectives:**
*   Extract and analyze drainage networks and their geometry.
*   Perform slope–area analysis to understand river profile concavity and steepness.
*   Generate and interpret longitudinal river profiles.
*   Identify and classify knickpoints based on their geomorphic characteristics.

**Pre-lab Preparation:**
*   Review Lectures W3-river_network and W3-long_prof.
*   Ensure a GIS environment (QGIS/SAGA GIS) is set up and functional, with an processed DEM from previous labs.

**Activities:**

**Part 1: Drainage Network Analysis (30 minutes)**
1.  **DEM Preparation (10 min):** Recap pit filling and flow accumulation from Week 2.
2.  **Extract Drainage Network (10 min):** Use a flow accumulation threshold to extract the stream network. Discuss sensitivity to threshold choice.
3.  **Calculate Stream Orders (10 min):** Apply Strahler stream ordering to the extracted network. Visualize and interpret the stream hierarchy.

**Part 2: Longitudinal River Profiles & Slope-Area Analysis (45 minutes)**
1.  **Extract Longitudinal Profiles (15 min):** Select 2-3 main river channels and generate their longitudinal profiles (elevation vs. downstream distance).
2.  **Slope-Area Plots (15 min):** Generate log-log slope-area plots for the selected rivers. Fit a regression line to determine the concavity index (θ) and channel steepness index (ks).
3.  **Knickpoint Identification (15 min):** Identify obvious breaks in slope along the longitudinal profiles and in the slope-area plots. Discuss their potential causes (tectonic, lithologic, base-level).

**Part 3: Discussion & Wrap-up (15 minutes)**
*   **Interpretation:** Discuss how longitudinal profiles and slope-area relationships provide insights into fluvial processes and landscape response to forcing.
*   **Knickpoint Classification:** Engage in a discussion on how to differentiate between different types of knickpoints based on the data.
*   **Next Steps:** Introduce how these observations will lead into more advanced quantitative analysis with Chi-analysis.

## Week 4 Lab: Tectonic Geomorphology - Indicators & Metrics (90 minutes)

**Objectives:**
*   Identify and quantify geomorphic indicators of active tectonics from DEMs.
*   Analyze basin asymmetry and its relationship to tectonic tilting.
*   Interpret patterns of river deflection and knickpoints in a tectonic context.

**Pre-lab Preparation:**
*   Review Lectures W4-Tectonic_Geomorphology_Introduction and W4-Tectonic_Geomorphology_Indicators.
*   Have GIS software (QGIS/SAGA GIS) and a processed DEM of a tectonically active region ready.

**Activities:**

**Part 1: Basin-Scale Tectonic Indicators (45 minutes)**
1.  **Hypsometric Analysis (20 min):**
    *   Delineate several drainage basins within the study area (active and less active regions if possible).
    *   Generate hypsometric curves and calculate the hypsometric integral for each basin.
    *   Compare results and discuss interpretations in terms of landscape maturity and potential tectonic influence.
2.  **Basin Asymmetry Factor (AF) (25 min):**
    *   For selected basins, calculate the Asymmetry Factor (AF) using appropriate GIS tools.
    *   Map the spatial variation of AF across the study area.
    *   Interpret AF patterns in relation to known or inferred tectonic tilting/faulting.

**Part 2: Channel-Based Tectonic Indicators (30 minutes)**
1.  **Knickpoint Analysis (15 min):**
    *   Revisit longitudinal profiles from Week 3, or extract new ones.
    *   Focus on identifying significant knickpoints. Discuss their morphological characteristics and potential causes (linking to lecture on tectonic vs. lithologic).
2.  **River Deflection/Offset (15 min):**
    *   Visually inspect the DEM and stream network for signs of river deflection or offset, particularly near mapped fault lines.
    *   Discuss how these features can indicate active strike-slip faulting.

**Part 3: Discussion & Wrap-up (15 minutes)**
*   **Converging Evidence:** Discuss the importance of using multiple indicators to infer tectonic activity, rather than relying on a single metric.
*   **Limitations:** Acknowledge the limitations of DEM-based analysis for tectonic geomorphology (e.g., distinguishing tectonic signals from lithologic or climatic ones).
*   **Transition to Chi-Analysis:** Introduce how Chi-analysis will provide a more rigorous, quantitative framework for analyzing channel profiles in the next lab.

## Week 5 Lab: Chi Analysis of River Networks (90 minutes)

**Objectives:**
*   Apply Chi-analysis to river networks to linearize profiles and identify disequilibrium.
*   Interpret Chi-elevation plots to infer variations in tectonic uplift and erodibility.
*   Compare Chi-analysis results with observations from previous labs (knickpoints, basin asymmetry).

**Pre-lab Preparation:**
*   Review Lectures W5-Chi_Analysis and W5-application_chi.
*   Ensure Python environment with necessary libraries (e.g., TopoToolbox or specific Landlab components for Chi-analysis) is set up.
*   Have a processed DEM and extracted river network from previous labs ready.

**Activities:**

**Part 1: Setting up for Chi Analysis (30 minutes)**
1.  **Python Environment Setup (15 min):** Ensure Python script/notebook is ready to load DEM and river network data. Import relevant libraries.
2.  **M/N Ratio (15 min):** Discuss the importance of the m/n ratio for Chi-analysis. Decide on an appropriate reference m/n value based on literature or previous slope-area analysis.

**Part 2: Performing Chi Analysis & Interpretation (45 minutes)**
1.  **Calculate Chi (20 min):** Apply the Chi-transformation algorithm to the main river channels and their tributaries.
2.  **Generate Chi-Elevation Plots (15 min):** Plot Chi values against elevation for selected river profiles.
3.  **Interpret Chi Plots (10 min):**
    *   Identify deviations from linearity in Chi-elevation plots (e.g., breaks in slope, non-linear segments).
    *   Relate these deviations to potential changes in uplift rate, lithology, or base-level.
    *   Compare with knickpoints identified in Week 3 Lab.

**Part 3: Discussion & Wrap-up (15 minutes)**
*   **Strengths & Limitations:** Discuss the advantages of Chi-analysis over raw longitudinal profiles or slope-area plots, as well as its inherent assumptions and limitations.
*   **Tectonic Inferences:** Engage in a discussion about how Chi-analysis enhances our ability to infer tectonic signals in river networks.
*   **Transition to SPIM:** Introduce how the theoretical framework of the Stream Power Incision Model (SPIM) will provide a mechanistic explanation for the patterns observed in Chi space.

## Week 6 Lab: Stream Power Calculations and Parameter Fitting (90 minutes)

**Objectives:**
*   Apply the Stream Power Incision Model (SPIM) to river networks.
*   Derive SPIM parameters (concavity, steepness) from DEM-derived slope-area data.
*   Understand the physical meaning of SPIM parameters and their role in river incision.

**Pre-lab Preparation:**
*   Review Lectures W6-Stream_Power_Index_Intro and W6-Stream_Power_Index_application.
*   Ensure Python environment with necessary libraries (e.g., NumPy, Matplotlib, TopoToolbox or similar for slope-area regression) is set up.
*   Have a processed DEM and extracted river network from previous labs ready.

**Activities:**

**Part 1: Slope-Area Regressions (40 minutes)**
1.  **Extract Slope-Area Data (20 min):** For selected river channels, extract corresponding slope (S) and drainage area (A) data from the DEM and flow accumulation grids.
2.  **Log-Log Plotting & Regression (20 min):** Plot S vs. A on a log-log scale. Perform a linear regression to estimate the concavity index (θ, which equals m/n) and the channel steepness index (ks). Discuss the goodness of fit.

**Part 2: SPIM Parameterization & Conceptual Application (35 minutes)**
1.  **Estimate m and n (15 min):** Based on the derived θ (m/n) and theoretical considerations (e.g., values discussed in lectures), choose plausible values for m and n individually. Justify your choices.
2.  **Conceptual Incision Rates (20 min):**
    *   Using a simplified form of the SPIM equation (E = K A^m S^n), conceptually discuss how changes in K, m, n, or uplift (U) would affect river incision rates and profile evolution.
    *   If time permits, perform a very basic calculation of relative incision rates for two hypothetical river segments with different steepness/area.

**Part 3: Discussion & Wrap-up (15 minutes)**
*   **Physical Interpretation:** Discuss the physical meaning of the derived ks and θ values in the context of tectonic and climatic controls.
*   **Limitations of Regression:** Acknowledge the uncertainties and limitations inherent in deriving SPIM parameters from noisy topographic data.
*   **Transition to Landlab:** Introduce how these parameters will be used in numerical simulations with Landlab to model landscape evolution in the next lab.

## Week 7 Lab: Basic SPIM Modelling in Landlab (90 minutes)

**Objectives:**
*   Learn the basics of setting up and running a Landscape Evolution Model (LEM) using Landlab.
*   Implement a simple Stream Power Incision Model (SPIM) in Landlab.
*   Visualize and interpret basic model outputs, including topography maps and elevation changes.

**Pre-lab Preparation:**
*   Review Lectures W7-Landscape_evolution_models and W7-SPIM_in_Landlab.
*   Ensure Python environment with Landlab installed is set up.
*   Familiarize with basic Python scripting.

**Activities:**

**Part 1: Landlab Environment Setup & Grid Initialization (30 minutes)**
1.  **Landlab Setup (15 min):**
    *   Open a Python Jupyter Notebook or script.
    *   Import necessary Landlab modules (e.g., `RasterModelGrid`, `FlowAccumulator`, `StreamPowerEroder`).
2.  **Grid Initialization (15 min):**
    *   Create a `RasterModelGrid` with specified dimensions (e.g., 50x50 cells) and cell spacing (dx).
    *   Initialize uniform elevation (e.g., `mg.add_zeros('node', 'topographic__elevation')`).
    *   Visualize the initial grid (e.g., `imshow_grid`).

**Part 2: Implementing SPIM & Running a Simulation (45 minutes)**
1.  **Add Uplift (10 min):**
    *   Define a uniform uplift rate (`U`) and apply it to the `topographic__elevation` field.
2.  **Instantiate Components (15 min):**
    *   Add a `FlowAccumulator` component to handle flow routing.
    *   Add a `StreamPowerEroder` component with parameters `K`, `m`, and `n` (using values from previous labs or lecture discussions).
3.  **Simulation Loop (20 min):**
    *   Set total simulation time and a suitable time step (`dt`).
    *   Run a simulation loop, calling `fa.run_one_step()` and `spe.run_one_step()` repeatedly.
    *   Track and plot mean elevation over time to observe system evolution.

**Part 3: Visualization & Basic Interpretation (15 minutes)**
*   **Visualize Final Topography:** Generate and interpret a hillshade or color map of the final topography. Discuss features like river channels and divides.
*   **Compare to Initial:** Briefly compare the final topography to the initial flat surface.
*   **Discussion:** Discuss the influence of the chosen parameters (`U`, `K`, `m`, `n`) on the resulting landscape.
*   **Next Steps:** Introduce how to add more complexity (hillslope processes, stochastic events) to LEMs.

## Week 8 Lab: Coupled Hillslope–Channel Modelling & Slope Stability (90 minutes)

**Objectives:**
*   Implement a coupled hillslope-channel model in Landlab.
*   Explore the interaction between hillslope processes (diffusion) and fluvial incision.
*   Understand the basic principles of slope stability analysis using the Factor of Safety (FoS).

**Pre-lab Preparation:**
*   Review Lectures W8-Coupling_Channels_Hillslopes_Mass_Movements.
*   Ensure Python environment with Landlab installed is set up.

**Activities:**

**Part 1: Hillslope Diffusion in Landlab (45 minutes)**
1.  **Modify Landlab Script (20 min):**
    *   Start with the basic SPIM script from Week 7.
    *   Add a `LinearDiffuser` component to simulate hillslope processes.
    *   Instantiate the `LinearDiffuser` with a diffusion coefficient (`D`).
2.  **Run Coupled Simulation (25 min):**
    *   Integrate the `LinearDiffuser` into the simulation loop, running it alongside `FlowAccumulator` and `StreamPowerEroder`.
    *   Run the simulation to a quasi-steady state.
    *   Visualize the topography and observe how hillslopes evolve compared to a purely fluvial model.
    *   Experiment with different `D` values and discuss their impact on hillslope gradient and sediment delivery.

**Part 2: Slope Stability Analysis (30 minutes)**
1.  **Conceptual FoS Calculation (15 min):**
    *   Using provided parameters (cohesion, internal friction angle, pore pressure, slope angle), calculate the Factor of Safety (FoS) for a hypothetical hillslope using the infinite slope model equation.
    *   Discuss how changes in each parameter affect slope stability.
2.  **Mapping Landslide Susceptibility (15 min):**
    *   (Conceptual or simple GIS exercise) Discuss how FoS could be calculated spatially using DEM-derived slopes and assumed material properties to create a landslide susceptibility map.
    *   Identify areas of high and low susceptibility on a given map.

**Part 3: Discussion & Wrap-up (15 minutes)**
*   **Hillslope-Channel Coupling:** Discuss the importance of coupling hillslope and channel processes for realistic landscape evolution.
*   **Landslide Role:** Reflect on the role of landslides as episodic events that can rapidly reshape landscapes and interact with river systems.
*   **Model Limitations:** Discuss the simplifications and limitations of the models used (linear diffusion, infinite slope model).
*   **Next Steps:** Introduce how glacial and periglacial processes also create distinct geomorphic signatures.

## Week 9 Lab: Glacial and Periglacial DEM Analysis (90 minutes)

**Objectives:**
*   Identify and interpret geomorphic signatures of past and present glacial and periglacial processes in DEMs.
*   Compare glaciated and non-glaciated landscapes using quantitative metrics.
*   Understand the impact of glacial processes on valley morphology and hypsometry.

**Pre-lab Preparation:**
*   Review Lectures W9-Landscape_Transience_Glacial_Periglacial_Forcing.
*   Ensure GIS software (QGIS/SAGA GIS) is functional.
*   Download provided DEMs of glaciated and non-glaciated regions (link/location to be provided separately).

**Activities:**

**Part 1: Glacial Geomorphology - Visual Interpretation & Metrics (45 minutes)**
1.  **Visual Interpretation of Glaciated Landscapes (20 min):**
    *   Load and visualize DEMs of a glaciated region (e.g., Alps, Patagonia).
    *   Identify classic glacial landforms (U-shaped valleys, cirques, arêtes, fjords) using hillshades, slope maps, and contour lines.
2.  **Valley Cross-Section Analysis (25 min):**
    *   Extract multiple valley cross-sections from both glaciated and non-glaciated valleys.
    *   Quantify valley shapes (e.g., using width-to-depth ratios or shape factors) and compare U-shaped vs. V-shaped profiles. Discuss the implications for glacial erosion.

**Part 2: Periglacial and Paraglacial Signatures (30 minutes)**
1.  **Hypsometric Analysis of Glaciated Basins (15 min):**
    *   Delineate a glaciated basin and generate its hypsometric curve and integral.
    *   Discuss how glacial modification affects hypsometry compared to purely fluvial basins.
2.  **Conceptual Paraglacial Adjustment (15 min):**
    *   Using a conceptual diagram or a simple Landlab exercise (if time permits, or as a demo), illustrate how a landscape might adjust (e.g., increased sediment delivery) after rapid deglaciation. Discuss the concept of paraglacial sediment pulses.

**Part 3: Discussion & Wrap-up (15 minutes)**
*   **Glacial vs. Fluvial Impact:** Discuss the distinct geomorphic signatures and erosional efficiencies of glacial vs. fluvial processes.
*   **Landscape Transience:** Revisit the concept of landscape transience in the context of glacial-interglacial cycles and post-glacial adjustments.
*   **Next Steps:** Introduce how data and models are integrated, and the role of uncertainty in geomorphic studies.

## Week 10 Lab: Calibration and Sensitivity Testing (90 minutes)

**Objectives:**
*   Integrate empirical data (e.g., erosion rates) into Landlab SPIM simulations for model constraint.
*   Perform sensitivity analysis to understand the influence of model parameters on outputs.
*   Explore the concept of equifinality and its implications for geomorphic modeling.

**Pre-lab Preparation:**
*   Review Lectures W10-Data_Model_Integration_and_Uncertainty.
*   Have Landlab Python script from Week 7/8 Labs ready.
*   Be familiar with the provided dataset of field-measured erosion rates for a specific region.

**Activities:**

**Part 1: Data Integration & Model Constraint (45 minutes)**
1.  **Load Field Data (15 min):**
    *   Load the provided field data (e.g., cosmogenic nuclide-derived erosion rates) into the Python environment.
    *   Spatially align this data with the model grid (if necessary, conceptually discuss how this would be done in practice).
2.  **Model Calibration/Constraint (30 min):**
    *   Run the Landlab SPIM simulation (from Week 7/8).
    *   Experimentally adjust the erodibility coefficient (`K`) to "fit" the model's predicted erosion rates to the observed field data. Discuss the challenges and assumptions involved in this process.
    *   Focus on achieving a "plausible range" rather than an exact match, emphasizing the concept of constraint over exact calibration.

**Part 2: Sensitivity Analysis & Equifinality (30 minutes)**
1.  **One-at-a-Time Sensitivity (20 min):**
    *   Choose a key SPIM parameter (e.g., `m` or `n`, or uplift rate `U`).
    *   Run several simulations, varying only this parameter within a plausible range, while keeping others constant.
    *   Analyze the impact of this variation on key model outputs (e.g., mean elevation, average slope, ksn distribution).
2.  **Conceptual Equifinality (10 min):**
    *   Discuss how different combinations of parameters might produce similar model outputs, illustrating the concept of equifinality.
    *   Consider how this complicates the interpretation of model results.

**Part 3: Discussion & Wrap-up (15 minutes)**
*   **Uncertainty Reporting:** Discuss the importance of reporting uncertainties in model predictions and parameter estimates.
*   **Model Limitations:** Reflect on how structural model limitations and data uncertainties influence our ability to interpret landscape evolution.
*   **Future Work:** Briefly discuss advanced techniques for uncertainty quantification (e.g., Monte Carlo simulations, inverse modeling).
*   **Next Steps:** Introduce the final project design workshop.
