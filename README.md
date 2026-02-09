# Lab 03 — Exploring Linear Relationships and Assessing Model Fit

EAES 480: Modern Statistics in Earth & Environmental Science
University of Illinois Chicago
Instructor: Dr. Gavin McNicol

## Dataset & Study Context

This lab uses site- and canopy-structure data from the study:

Asner, G.P., Anderson, C.B., Martin, R.E., Knapp, D.E., Tupayachi, R., Sinca, F., Malhi, Y. (2014)
Landscape-scale changes in forest structure and functional traits along an Andes-to-Amazon elevation gradient
Biogeosciences, 11, 843–856
https://doi.org/10.5194/bg-11-843-2014

The dataset combines:
	•	site-level environmental variables (elevation, climate, soils), and
	•	canopy structural properties (height, gap structure, shape metrics),

allowing us to explore correlative relationships across a strong environmental gradient.

This system is ideal for learning linear models because:
	•	clear gradients exist,
	•	correlations are plausible but imperfect,
	•	and ecological meaning matters as much as statistical fit.

## Overview

This lab introduces simple linear models as descriptive tools in Earth & Environmental Science.

Rather than treating regression as a black box, this assignment emphasizes:
	•	visualizing relationships before modeling,
	•	understanding what coefficients actually mean,
	•	fitting and drawing regression lines explicitly,
	•	and diagnosing model assumptions using residuals.

You will work in a structured R Markdown (.Rmd) document that asks you to:
	•	complete missing code,
	•	inspect model outputs and plots,
	•	and write short interpretation responses throughout.

This lab prepares you for later units on inference, uncertainty, and explanatory modeling.

## Learning Goals

By the end of this lab, you should be able to:
	•	Join multiple tidy datasets into a single analysis table
	•	Visualize bivariate relationships using scatterplots
	•	Fit and interpret simple linear regression models
	•	Explain regression coefficients with units and context
	•	Plot fitted lines using both geom_smooth() and explicit coefficients
	•	Evaluate model assumptions using residual diagnostics
	•	Produce a fully reproducible R Markdown analysis

## What You’ll Do

In the provided R Markdown template, you will:
	•	Load and join site- and canopy-level datasets
	•	Choose a predictor–response pair grounded in environmental reasoning
	•	Create scatterplots to explore correlation
	•	Fit a simple linear model using lm()
	•	Inspect coefficients with broom::tidy()
	•	Draw the fitted line manually using geom_abline()
	•	Evaluate model fit using:
	•	residuals vs fitted plots,
	•	residual histograms and density plots,
	•	QQ plots for normality
	•	Answer short interpretation prompts in complete sentences
	•	Knit the document to confirm it runs cleanly from top to bottom

This is a reasoning-first lab: interpretation and diagnostics matter as much as code.

## Repository Contents

lab-03-linear-models.Rmd
→ The lab template you will complete and submit
	•	README.md
→ This file
	•	(optional) data/
→ Folder containing the provided Andes–Amazon CSV files

## Instructions
	1.	Fork or clone this repository to your own GitHub account
	2.	Open lab-03-linear-models.Rmd in RStudio
	3.	Work through the document from top to bottom
	4.	Fill in missing code only inside the existing code chunks
	5.	Respond to interpretation prompts in plain text (outside code chunks)
	6.	Knit the document regularly to catch errors early

⚠️ Code that runs in the Console but not in the .Rmd does not count.

## Reproducibility Requirements

Your submission must:
	•	Knit without errors
	•	Run top-to-bottom in a clean R session
	•	Include all required libraries in the setup chunk
	•	Avoid hard-coded local file paths
	•	Use na.rm = TRUE where appropriate
	•	Derive plots and results from model objects (not manual tweaking)

These are not stylistic preferences—they are core scientific skills.

## Submission
	•	Commit and push your completed .Rmd file to your GitHub repository
	•	Submit the GitHub repository link on Canvas
	•	You do not need to submit the knitted HTML unless instructed

Your work will be evaluated on:
	•	correctness of code,
	•	quality of interpretation,
	•	and reproducibility.

## Collaboration Policy
	•	You may discuss concepts and modeling strategies with classmates
	•	You may not copy code verbatim from others
	•	Code you submit must be written and understood by you

If you worked with someone, acknowledge them in a comment.

## Tips for Success

	•	Always look at the scatterplot before fitting a model
	•	Units matter: interpret slopes in physical terms
	•	Residuals tell you more than R² alone
	•	A statistically significant relationship can still be a poor model
	•	If a diagnostic plot surprises you, pause and think—don’t rush past it

## Why This Matters

In Earth & Environmental Science:
	•	correlation is not causation,
	•	gradients often confound interpretation,
	•	and models encode assumptions whether we check them or not.

Linear models are among the most widely used tools in environmental research.
This lab builds the intuition needed to use them responsibly, critically, and transparently—before we move on to more complex modeling frameworks.
