# DietHealthLink-2
Analysis of Dietary Inflammation Index (DII) and Osteoarthritis (OA) Risk

This repository contains code and methods for analyzing the relationship between the Dietary Inflammation Index (DII) and the risk of osteoarthritis (OA) using NHANES data. The analysis involves data processing, modeling, prediction, visualization, and result interpretation.

Overview
The analysis aims to explore how different levels of the Dietary Inflammation Index (DII) influence the risk of osteoarthritis (OA). The process involves constructing a complex sampling design, performing descriptive statistical analysis, building a nonlinear model, making predictions, and visualizing the results.

Data Processing and Modeling
1.Constructing a Complex Sampling Design
Use svydesign() to account for stratification, sampling units, and sample weights in the NHANES data. This ensures the representativeness and robustness of the analysis.

2.Variable Recoding
Recode the arthritis variable into two categories: osteoarthritis (OA = 1) and non-osteoarthritis (non-OA = 0). This recoding optimizes the data structure for subsequent analysis.

3.Descriptive Statistical Analysis
Use CreateTableOne() to generate a descriptive statistical table comparing the distribution of age, gender, BMI, and other variables between OA and non-OA patients. This provides a reference for further modeling.

4.Nonlinear Model Construction
Construct a weighted binary generalized linear model. Use restricted spline functions to capture the nonlinear relationship between DII_ALL and OA, adjusting for gender, age, and BMI.

Prediction and Visualization
5.Model Prediction and Confidence Interval Calculation
Generate prediction data for different levels of DII_ALL. Calculate the corresponding osteoarthritis risk (Odds Ratio, OR) and its 95% confidence interval.

6.Visualization Analysis
Use ggplot2 to create a trend chart of OR values changing with DII_ALL. This visualizes the impact of the dietary inflammation index on osteoarthritis risk.

Result Interpretation
7.Nonlinear Trend Identification
Identify the nonlinear relationship between DII_ALL and OA risk. The risk is higher at low DII_ALL values, relatively stable in the middle range, and increases again at high DII_ALL values.

8.High DII_ALL Increases Risk
When DII_ALL exceeds 3, the risk of osteoarthritis significantly increases. This suggests that a high dietary inflammation index may elevate the risk of osteoarthritis.
