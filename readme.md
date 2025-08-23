# Distribution Change Studies

## Overview

This repository presents visual search experiments exploring how the local and global distribution of distractors influences search performance and attention allocation. We conducted an eye-tracking study using a singleton visual search task with two participant groups. In the first group—the “unequal distribution” group (Experiment 1)—the singleton distractor appeared four times more often in one region (the frequent distractor region) than in another (the rare distractor region) during the experiment’s first half. In the second half, while the rare region’s distractor frequency remained constant, the frequent region’s rate dropped to match that of the rare region. The second group—the “equal distribution” group (Experiment 2)—experienced a consistent low-frequency distractor occurrence across both regions throughout the entire experiment, matching the lower frequency used in the rare region of Experiment 1.

**Core Design**: 8-location circular visual search task investigating how the distribution of distractors affects search performance. The design for the uneqal group (Experiment 1) mirrors Valsecchi and Turatto (2021) Experiment 2 with some minor differences. The design is also a conceptual replication of Allenmark et al. (2022). 

### Key Manipulations:

1. **Spatial Distribution**:
   - **8 positions** arranged in a circle (positions 1-8)
   - **Frequency regions**: Bottom half (1-4) vs Top half (5-8)
   - **Counterbalanced**: Odd sequences (1,3,5...) have frequent distractors in top half, even sequences (2,4,6...) in bottom half

2. **Distractor Position Conditions**:
   - **Frequent distractor region**: 4x more likely to contain distractors
   - **Rare distractor region**: 1x baseline probability
   - **Distractor absent**: No distractor present (position 0)

3. **Trial Structure**:
   - **960 trials** total per participant
   - **2 sessions** of 480 trials each
   - **16 blocks** of 60 trials

4. **Session Distribution**:
   - **Session 1**: Heavy bias toward frequent region (4:1 ratio)
   - **Session 2**: Reduced bias (1:1 ratio) - adaptation/transfer test

5. **Visual Features**:
   - **Colors**: Red vs Green (always opposite for target/distractor)
   - **Shapes**: 2 shape types (coded as 0/1)
   - **Line orientations**: 0° vs 90° (independent for target/distractor)

6. **Constraints**:
   - Target and distractor never appear at same location
   - Target position equally distributed across all 8 locations for each distractor condition
   - All feature combinations systematically varied (16 conditions)

### Research Questions:
This design tests whether participants develop **spatial biases** based on distractor frequency, and whether these biases **transfer** when the distribution changes in session 2. The key dependent variables would be search efficiency (RT/accuracy) as a function of target location relative to the frequent/rare distractor regions.

## Repository Structure

- **Experiment 1/**: First experiment files and data
- **Experiment 2/**: Second experiment files and data  
- **Analysis scripts**: `dataana*.R` and `eye_dataana*.R` files
- **functions.R**: Shared utility functions
- **sequences/**: Experimental sequence files
- **Figures/**: Generated plots and visualizations
