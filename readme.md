# Distractor Interference under Distribution Change

## Overview

This repository contains a visual search experiment examining how local and global distribution of distractors influences search performance and attention allocation. The study uses eye-tracking data from a singleton visual search task with two experimental groups investigating adaptation to changing distractor distributions.

**Core Design**: Eye-tracking experiment using an additional singleton visual search paradigm with 8-location circular arrangement. The unequal-distribution group (Experiment 1) closely mirrors Valsecchi and Turatto (2021) Experiment 2, while serving as a conceptual replication of Allenmark et al. (2022).

### Experimental Groups

**Experiment 1 (Unequal Distribution)**:
- First half: Distractors appear 4x more frequently in one region (frequent) than another (rare)
- Second half: Both regions have equal distractor frequency, matching the rare region frequency from first half

**Experiment 2 (Equal Distribution)**:
- Throughout experiment: Distractors appear with equal frequency in both regions
- Control condition matching the second half of Experiment 1

### Key Manipulations

1. **Spatial Layout**:
   - 8 positions arranged in a circle (positions 1-8)
   - Frequency regions: Bottom half (1-4) vs Top half (5-8)
   - Counterbalanced across participants

2. **Distractor Conditions**:
   - Frequent distractor region (4x probability in first half)
   - Rare distractor region (1x baseline probability)
   - Distractor absent trials (position 0)

3. **Trial Structure**:
   - 960 trials total per participant
   - 2 sessions of 480 trials each
   - 16 blocks of 60 trials

4. **Visual Features**:
   - Colors: Red vs Green (target/distractor always opposite)
   - Shapes: 2 types (coded as 0/1)
   - Line orientations: 0° vs 90°

## Analysis Framework

The study analyzes three distinct phases of visual search based on eye-tracking data:

1. **First Target Fixation (ftf_RT)**: Time from trial start until initial target fixation
2. **Middle Target Fixation (mtf_RT)**: Time between initial and final target fixations  
3. **Response Phase (resp_RT)**: Time from final target fixation until decision response


## Repository Structure

### Data Files
- `data/data.csv` - Raw experimental data with trial-level information
- `data/rt_data_both_phases.csv` - Preprocessed data for visual search phase analysis
- `data/qdata.csv` - Questionnaire data

### Analysis & Visualization
- `analysis_dist_change.Rmd` - Main R Markdown analysis file
- `analysis_dist_change.html` - Rendered HTML report with interactive elements
- `Figures/` - Publication-ready plots generated from analysis
  - `baseline_combined.png` - Baseline performance across conditions
  - `distractor_interference_phases.png` - Interference effects by search phase
  - `interference_detailed.png` - Detailed interference analysis


#### Interactive Analysis
Open `analysis_dist_change.Rmd` in RStudio and knit or run chunks interactively.

## Key Variables

- **DistPos**: Distractor position (0 = absent, 1-8 = spatial positions)
- **TarPos**: Target position (1-8)
- **group**: Experimental condition ("unequal" vs "equal" distribution)
- **blkType**: Experimental phase ("Before change" vs "After change")
- **freq_region**: Spatial region classification ("Top" vs "Bottom")
- **DistCond**: Distractor condition ("Absent", "Freq. dist.", "Rare dist.")

