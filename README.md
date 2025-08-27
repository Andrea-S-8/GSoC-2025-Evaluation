# GSoC Final Evaluation:
**Contributor**: Andrea Storey

**Mentors**: Rebecca Killick and Colin Gallagher

**Project**: Modern time series estimation

**Organisation**: R Project For Statistical Computing

## Link to my GitHub Repositry:
[Andrea-S-8/PenalizedCorr at new-branch](https://github.com/Andrea-S-8/PenalizedCorr/tree/new-branch)

## Description:

This project implemented the recent techniques from Gallagher et al. (2024) and Gallagher et al. (2025) for improved time series simulation studies covering the whole parameter space of time series models (and not just cherry-pick one or two parameter settings) and also brought modern estimates of the acf/pacf and consistency in AIC selection of ar models (which is not currently available). Specifically, the project: - created functions for acf and pacf estimation based on a dual shrinkage approach - created functions for ar estimation based on the dual shrinkage pacf - interface the new ar estimation function with standard methods such as AIC for consistent estimation - created new graphics for displaying these estimates that make clear to the user the effect of the dual shrinkage approach (as an option) - created functions to generate ARMA parameters that satisfy a correlation constraint (high/med/low or a fixed correlation strength) - created functions to generate random ARMA parameter values that cover the whole parameter space regardless of the model order - created a wrapper for the above two functions to generate simulation datasets for researchers in one line of code All this functionality required appropriate documentation, testing and a vignette for users.

## What work was done: 
+ Created an R package using the existing research-level prototype code.
  + Manipulated the existing research-level prototype code into the correct format for an R package. Learnt how to make an R package from existing functions. 
+ Created unit and function tests.
  + This testing focused on function parameters within the package PenalizedCorr.
  + Wrote extensive test cases using tinytest, borrowing ideas from other time series packages.
+ Added logical testing
  + This was done to fix errors found during testing.
+ Wrote the user-facing functionality which includes extending the existing S3 class from base R and associated summary, print and plot methods to the new functions.
  +  I have mimiced the existing base R function structure to make the functions easy to use for those familiar with those functions.  I have added additional arguments to allow for the new options.  Equally, the plotting functionality has mimiced the existing base R functionality. 
+ Added documentation to the functions.
+ Debugging and improvements.
+ Extend the existing research-level code to allow different user options for the different parameters with the defaults being those implemented in the research code. 
  + User options were created for parameters, lambda and target, then documentation was updated followed by unit and function testing using tiny test
+ Worked on creating a new function for banded and tapered called bandtap, as well as up-to-date documentation. Then added an if statement to the function acf to call new function bandtap, following this unit testing was completed.
+ Wrote the Vignette

## What code got merged:
My updates, code changes and merges can all be found here: [Commits · Andrea-S-8/PenalizedCorr](https://github.com/Andrea-S-8/PenalizedCorr/commits/new-branch)

## What’s left to do:
The package is in its final stage before being released to the wider community. 
Further tests for both unit and function would be beneficial.

#### Acknowledgments:
I am sincerely grateful to my mentors, Rebbeca and Colin, for their invaluable guidance throughout my GSoC journey. This was my first time working with professional developers and contributing to an open-source community. The challenges and opportunities provided by this project have been instrumental for my growth and future development.
