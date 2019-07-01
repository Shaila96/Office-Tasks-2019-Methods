# Multimodal-Email-Study

## Requirements
- R and packages

## Dataframe making Scripts (Please follow the serial bellow):
- **curate-and-process-physiological-data.R**
    - For each group and subjects the script does the following:
        - Read the *pp.csv (raw perinasal perspiration signal file), remove noise, downsample by 1 fps
        - Read the session markers file and split the session with the PP signal.
        - Read the files from E4 and Zephyr Bioharness signal, downsample each signal and merge with PP signal.
- **quality-control-first-phase.Rmd**
    - This script is for generating the combined file for all signals, for
        - Merged 1fps data - without quality control
            - Change the variable value to FALSE: **is\_filter\_data = F**
        - Filtered data - quality control phase 1
            - Change the variable value to TRUE: **is\_filter\_data = T**
- **quality-control-second-phase.Rmd**
    - This script is cleaning data in the second phase
- **nlp-processor.R**
    - **Note:** Run the following line once:
- initCoreNLP(mem = "4g")
-
-
-
- **essay-email-extractor.R**
    - Gather and merge all report and email response for 63 subjects
- **final-data-formation.R**
    - Making all the final dataset user-friendly version






## Plot Scripts:
- **time-series-plots.Rmd**
    -
- **validation_plots.R**
	-
- **supplementary_plots.Rmd**
    -
- **mean_signal-distribution.Rmd**
    -
- **hr-regression-and-distribution-plot.Rmd**
    -
- **c-hr-w-hr-comparison-plot.Rmd**
    -


## Other Scripts:
- **filter-pp.R**
    - Script to remove noise from PP signal
- **down-sample-pp.R**
    - Script to downsample data to 1 frame per second
- **common-functions.R**
- The common functions are used in almost all files
- **score-psychometrics.R**
    - The scoring calculation for psychometrics variables
