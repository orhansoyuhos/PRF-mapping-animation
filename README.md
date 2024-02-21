# Population Receptive Field (PRF) Mapping Simulation

This repository contains MATLAB scripts for simulating neural activity in response to stimuli presented at specific locations on a grid and calculating the population receptive field (PRF) based on the simulated neural responses.

## Overview

The project simulates an experiment where visual stimuli are presented at predetermined locations on a grid. In each trial, three unique locations are sequentially shown, optimizing the experiment's duration while capturing a comprehensive range of neural responses. The neural responses to these stimuli are simulated based on specified parameters, including the sensitivity of neural channels to the stimuli's locations. Following the simulation, the code calculates the PRF mapping. 

## Prerequisites

    MATLAB (Recommended version: R2020a or later)
    Statistics and Machine Learning Toolbox (for some functions like heatmap)

## Repository Contents

    RF_mapping_simulation.m - The main script that orchestrates the simulation of neural activity, calculation of the PRF, and visualization of the results.
    simulate_neural_activity.m - Function that simulates neural activity in response to stimuli based on a Gaussian response profile.
    animate_trials.m - Function that visualizes the simulated neural activity as if being recorded in real-time during an experiment.
    calculate_population_receptive_field.m - Function that calculates and visualizes the PRF based on the simulated neural responses.
    plot_stimulus.m - Helper function for visualizing the location of stimuli on a grid during the simulation.

## Customization

You can customize the experiment simulation by adjusting the parameters at the beginning of the RF_mapping_simulation.m script:

    arraySize - The size of the grid for stimulus presentation (e.g., [4, 6] for a 4x6 grid).
    repetitionsPerLocation - The number of times each location is shown.
    baselineDuration, stimulusDuration, ISIDuration - Timing parameters for the experiment, specified in milliseconds.

## Data Simulation and RF Mapping Calculation
### Neural Activity Simulation

The simulation models neural responses to stimuli presented on a predefined grid, capturing the dynamics of experimental trials. Stimuli are shown at various locations with controlled timings for presentation, baseline, and inter-stimulus intervals. Neural responses are simulated based on a Gaussian response profile, reflecting how neurons react to stimuli relative to their peak sensitivity locations. This approach generates a dataset mimicking real neural activity patterns in response to spatially distributed stimuli.

### PRF Mapping Calculation

The Population Receptive Field (PRF) mapping is computed by isolating and averaging the neural activity elicited by stimuli at each grid location across all trials. This involves:

    1- Aggregating Activity: Collecting neural responses specific to the times when each location is presented.
    2- Averaging: Calculating the mean response for each location across trials and channels to determine the average activity elicited by stimuli at that location.
    3- Heatmap Visualization: The averaged responses are visualized on a grid as a heatmap. Color intensity on the heatmap correlates with the neural response magnitude, illustrating the spatial sensitivity of the neural population to different stimulus locations.

## Support

For issues, questions, or contributions, please open an issue or pull request in this repository.