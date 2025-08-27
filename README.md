# GSoC-2025-Evaluation

## Final Report:
**Contributor**: Andrea Storey

**Mentors**: Rebecca Killick and Colin Gallagher

**Project**: Modern time series estimation

**Organisation**: R Project For Statistical Computing

## Description:

This project will implement the recent techniques from Gallagher et al. (2024) and Gallagher et al. (2025) for improved time series simulation studies covering the whole parameter space of time series models (and not just cherry-pick one or two parameter settings) and also bring modern estimates of the acf/pacf and consistency in AIC selection of ar models (which is not currently available). Specifically, the project will: - create functions for acf and pacf estimation based on a dual shrinkage approach - create functions for ar estimation based on the dual shrinkage pacf - interface the new ar estimation function with standard methods such as AIC for consistent estimation - create new graphics for displaying these estimates that make clear to the user the effect of the dual shrinkage approach (as an option) - create functions to generate ARMA parameters that satisfy a correlation constraint (high/med/low or a fixed correlation strength) - create functions to generate random ARMA parameter values that cover the whole parameter space regardless of the model order - create a wrapper for the above two functions to generate simulation datasets for researchers in one line of code All this functionality will require appropriate documentation, testing and a vignette for users.

## What work was done: 
+ Create an R package using the existing research-level prototype code.
+ Created unit and functional tests
+ Added logical testing (to some functions in the package to fix errors)
+ I wrote the user-facing functionality which includes extending the existing S3 class from base R and associated summary, print and plot methods to the new functions.
+ Added documentation to functions.
+ Debugging and improvements.
+ Extend the existing research-level code to allow different user options for the different parameters with the defaults being those implemented in the research code. 
+ User options were created for lambda and target, then documentation was updated followed by unit and function testing using tiny test
+ Worked on creating a new function for banded and tapered called bandtap with documentation referencing forecast package. Then added an if statement to function acf to call bandtap, afterwards I did unit testing.
+ Write Vignette

## What code got merged:
My updates, code changes and merges can all be found here: [Commits · Andrea-S-8/PenalizedCorr](https://github.com/Andrea-S-8/PenalizedCorr/commits/new-branch)

## What’s left to do:
The package is in its final stage before being released to the wider community. 
Further tests for both unit and function would be beneficial.

## Acknowledgments:
I am sincerely grateful to my mentors, Rebbeca and Colin, for their invaluable guidance throughout my GSoC journey. It was my first time working with professional developers and contributing to an open-source community. The challenges and opportunities provided by this project have been instrumental for my growth and future development.

## Link to my GitHub:
[Andrea-S-8/PenalizedCorr at new-branch](https://github.com/Andrea-S-8/PenalizedCorr/tree/new-branch)
