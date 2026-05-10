
# Environmental Control of Auxotrophic Communities

Scripts and data used to produce figures and simulations related to the article:  
**Stabilizing Auxotrophic Consortia Through Dynamic Environmental Manipulations**  
*A. Fuentes-Hernandez, D. Reyes-González, and R. Peña-Miller*

* * *

This repository contains Jupyter notebooks implementing and analyzing a resource-explicit model of synthetic auxotrophic bacterial communities under different amino acid supplementation regimes.
The workflow reproduces the computational and experimental analysis pipeline, from growth-parameter calibration to constant, random, optimized, and feedback-controlled environmental simulations.

## Notebook Structure

### 1. [py-ProfileX_params.ipynb](py-ProfileX_params.ipynb)

Fits growth parameters for individual auxotrophic strains from monoculture growth curves.
The estimated parameters (`V_m/K_m`, `c`, `beta`) are used as inputs for downstream community simulations.

This notebook:

* imports growth-curve data,
* performs background correction and data preprocessing,
* fits strain-specific growth parameters,
* compares experimental growth trajectories with model fits,
* exports fitted parameter sets for simulation.

### 2. [py-ProfileX_data.ipynb](py-ProfileX_data.ipynb)

Analyzes experimental serial-transfer data from auxotrophic communities exposed to constant and feedback-controlled amino acid environments.

This notebook:

* imports OD and frequency data,
* processes replicate-level lineage trajectories,
* computes strain frequencies and Shannon diversity over time,
* calculates diversity and density summaries,
* compares endpoint outcomes across environmental conditions,
* generates experimental figures.

### 3. [py-ProfileX_simulations.ipynb](py-ProfileX_simulations.ipynb)

Runs numerical simulations of multi-strain auxotrophic communities under different environmental regimes.

This notebook:

* simulates constant amino acid supplementation environments,
* evaluates all community subsets across supplementation levels,
* classifies ecological outcomes as collapse, competitive exclusion, or coexistence,
* samples random environmental sequences,
* searches for high-performing environmental sequences,
* simulates feedback-controlled supplementation strategies,
* compares density, diversity, richness, and fitness metrics across treatments.

* * *

## Data Directory

The `data/` directory contains experimental datasets and intermediate files used by the notebooks.

These include:

* monoculture growth-curve data used for parameter fitting,
* serial-transfer OD measurements,
* endpoint and time-resolved strain-frequency data,
* fitted strain-parameter files used in simulations.

* * *

## Model Description

The model describes growth of auxotrophic strains in a shared resource environment with strain-specific amino acid requirements.
Community dynamics are simulated across serial-transfer cycles under prescribed or feedback-controlled amino acid supplementation schedules.


## License

This project is licensed under the [MIT](https://choosealicense.com/licenses/mit/) License - see the [license](LICENSE) file for details. 

