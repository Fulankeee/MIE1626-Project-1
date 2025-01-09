# MIE1626 Data Science Methods and Statistical Learning
# Project 1 

Python Basic Data Science Package
-	Wrangling tools  
Pandas; numpy;  
-	Visualization
matplotlib.pyplot; seaborn(pair plot, heatmap)  
-	Statistical learning  
statsmodels.api  
-	ISLP.models: ModelSpec as MS, summarize, poly  
-	statsmodels.stats.outliers_influence: variance_inflation_factor (VIF)  
-	statsmodels.stats.diagnostic: het_breuschpagan (Heteroscedasticity)
-	
Part 1 – Data Loading and Cleaning
-	Convert columns ‘FIPS’ to five-digital char-type.
-	Remove columns with high null-rate.
-	Identify the data type of each column for further analysis.
-	Merge the population data to the main data by ‘FIPS’.
-	Conduct EDAs for ‘Mortality_rate’
	Bar-plot of Mortality rate using 3 kinds of imputations (replace the null with estimated numbers like 1, 15,15/2)
	Bar-plot of Mortality rate removing all unknowns.
	Plot the relationship between Population Size and Number of Cases after removing missing data, and use this characteristic to estimate the missing reported case (less than 16) by their population.
	Divide the POP_ESTIMATE_2022 (325 rows in total) into 16 equal sized groups. Assign 0 reported cases to group 1, 1 to group 2, 2 to group 3 and so on until 15 to group 16. Replace the missing data with calculated mortality rate.

Part 2 – Data Visualization and analysis
-	Using pair plots to see the relationship between features.
-	Select the most significant features by analyzing the correlation between the features and removing the highly correlated features.
-	Identify slops and patterns from the scatterplot and remove redundant features by a threshold.

Part 3 – Model Application
-	Using heatmap to identify correlations between features to the mortality rate.
-	Model construction:
	Full model
	Model using selected features
	Model with interaction term (focus on features that have a high correlation with "Mortality_Rate" but low correlation with other independent variables to avoid multicollinearity.)
	Polynomial regression model
-	Model selection according to MSE and adjust R2

Part 4 – Model diagnostics
-	Consider VIF > 10 as an indicator of multicollinearity to apply for each model
-	Perform the Breusch-Pagan test for heteroscedasticity (variance of the errors (or residuals) is not constant)

Part 5 – Model Performance
-	MSE; CV for validation data

Part 6 – Alternative Model
-	Consider using Ridge and Lasso regression with GridSearchCV to tune alpha to handle the problem of overfitting.
