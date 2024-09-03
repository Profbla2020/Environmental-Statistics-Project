# Estimating Common Parameters of the Distribution of a Successive Random Dilution: A Comparative Study
 **Overview**
 
This project aims to analyze dilution data through a series of experiments to identify the most appropriate statistical distribution model and estimate its parameters. This study is significant for understanding the behavior of pollutant dilution over successive random dilutions, which is crucial for environmental monitoring and decision-making.

**Objectives**

The specific objectives of this study are:

1. Fit the dilution data to the best statistical distribution.
   
2. Estimate the parameters of the selected distributions.
   
3. Assess the goodness of fit for each distribution.

# Methodology

**1. Data Simulation**
To simulate the dilution process, four sets of random samples were generated using the runif function in R, which creates random uniform distributions between 0.14 and 0.26.

The dilution product was calculated by multiplying these samples, which represents the combined effect of successive dilutions.

**set.seed(123)**

sample1 = runif(1500, 0.14, 0.26)

sample2 = runif(1500, 0.14, 0.26)

sample3 = runif(1500, 0.14, 0.26)

sample4 = runif(1500, 0.14, 0.26)

sample_product = sample1 * sample2 * sample3 * sample4

c4 = sample_product * 360.5

**2. Data Visualization**

We created a histogram of the concentration data (c4) to visualize the distribution of the dilution product. A blue vertical line represents the mean concentration, and 

text annotations provide the mean and standard deviation.

**3. Distribution Fitting**

To fit the data, we considered several candidate distributions: Normal, Gamma, Weibull, and Log-normal. Using the fitdist function from the fitdistrplus package in R, we

estimated the parameters of these distributions.

**4. Goodness of Fit Assessment**

We assessed the goodness of fit for each distribution using graphical methods such as density plots, Q-Q plots, P-P plots, and CDF plots. The gofstat function provided 

statistical metrics for comparing the fits.

**5. Comparative Analysis of Fits**

We compared the fits graphically using various plots to visualize how well each distribution represents the data. This includes plots for the actual vs. fitted graphs for 

each distribution and the goodness-of-fit plots.

**6. Additional Analyses**

We also plotted Gamma distributions with constant rates and different shapes to explore the impact of shape parameters on the distribution behavior.

# Results

**Best-Fit Distribution**: The Gamma distribution provided the best fit for the dilution data based on visual and statistical assessments.

**Parameter Estimation:** Parameters for each distribution were estimated, showing different shapes and scales that best match the observed data.

**Goodness of Fit:** The goodness-of-fit tests confirmed the Gamma distribution as the most appropriate model for the given data, with the lowest AIC and BIC values among 

the tested distributions.

# Getting Started

To replicate the analysis, follow these steps:

**Install R and RStudio:** Ensure you have R and RStudio installed on your system.

**Install Required Packages:** Install the necessary R packages (ggplot2, fitdistrplus, MASS, etc.) using the command install.packages("packageName").

**Run the Code:** Copy the provided R script into RStudio and run each section sequentially to replicate the analysis and generate the plots.

# Repository Contents

**scripts/:** R scripts used for data simulation, analysis, and visualization.

**results/:** Directory for output files, including plots and fit summaries.

**README.md:** This file provides an overview and instructions for reproducing the study.









