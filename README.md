Adstock Modeling for Marketing Mix Analysis

This project is focused on implementing adstock modeling for marketing mix analysis using Bayesian statistics. The goal is to understand the effectiveness of different marketing channels in driving sales for an online shop. The data used in this analysis is provided in the "MMM_test_data.csv" file, which contains information about weekly revenue and marketing spend across seven different channels.
Project Overview

The project follows the following steps:

    Importing Required Libraries: The necessary libraries for Bayesian modeling, data manipulation, visualization, and Bayesian inference diagnostics are imported using import statements.

    Reading Data: The data is read from the CSV file using the pandas library. The 'revenue' column is separated as the target variable, and the remaining columns are stored as features.

    Data Exploration: Exploratory data analysis (EDA) is performed on the loaded data to understand the data distribution, visualize missing data using the missingno library, and check for correlations between features using a heatmap.

    Adstock Modeling: The adstock_delayed() function is defined, which implements the delayed adstock transformation. This function takes spend data for a specific channel, alpha and theta parameters for the adstock transformation, and a maximum time span for the carry-over effect as inputs, and returns the delayed vector.

    Data Preprocessing: The spend data for each channel is scaled and normalized using the min-max scaler function. Additionally, the target variable (revenue) is also scaled using the same function.

    Bayesian Model: A Bayesian model is built using PyMC library to estimate the parameters of the adstock model. The likelihood function is defined based on the normal distribution, and priors are set for the alpha and theta parameters. The adstock_delayed() function is used to calculate the delayed spend vectors for each channel.

    Model Inference: Bayesian inference is performed to estimate the posterior distribution of the model parameters using Markov Chain Monte Carlo (MCMC) sampling. The trace plots and summary statistics of the parameters are visualized using the ArviZ library.

    Model Evaluation: The model performance is evaluated based on the convergence of MCMC sampling, posterior predictive checks, and model diagnostics using ArviZ diagnostics functions.

    Channel Performance Analysis: The estimated adstock parameters are used to calculate the effectiveness of each marketing channel in driving sales. The adstock values for each channel are visualized and compared to identify the best-performing channel in terms of the carry-over effect.

    ROI Analysis (Bonus): The estimated adstock parameters and revenue data are used to calculate the return on investment (ROI) for each marketing channel, which is a measure of the effectiveness of marketing spend. The ROI values are compared to identify the best-performing channel in terms of ROI.

Files Included

    MMM_test_data.csv: The input data file containing weekly revenue and marketing spend data for different channels.
    Read.md: The markdown file containing the documentation of the project.
   

Conclusion

This project demonstrates the implementation of adstock modeling for marketing mix analysis using Bayesian statistics. The adstock model helps in understanding the delayed effects of marketing spend on sales, and the Bayesian approach allows for uncertainty estimation and posterior inference. The model performance can be evaluated using diagnostic checks, and the estimated parameters can be used to analyze the effectiveness of different marketing channels in driving sales. Additionally, ROI analysis can also be performed to identify the best-performing channel in terms of ROI.
