# House-Price-Prediction-by-Using-Lasso-and-Ridge-Regression-
House Price Prediction by Linear Regression Methods(Lasso and Ridge)

## Outline and Brief descrption of the project

A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia. The data is provided in the CSV file below.
The company is looking at prospective properties to buy to enter the market. You are required to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.


The company wants to know:

Which variables are significant in predicting the price of a house, and

How well those variables describe the price of a house.

Also, determine the optimal value of lambda for ridge and lasso regression.

Also, determine the optimal value of lambda for ridge and lasso regression.

# Business Goal
You are required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.

# Technolgies used:
 ## Python pandas - Version : 1.2.4
 ## numpy - Version : 1.20.1
 ## seaborn - Version : 0.11.1
 ## matplotlib - Version : 3.3.4
 ## statsmodels - Version : 0.12.2
 ## pandasql - Version : 0.7.3
 ## sklearn - Version :0.24.2

 # Approach:


## 1 Importing modules, Reading the data
## 2 Analyzing Numerical Features
###### Checking Statistical summary
###### Checking Distribution of numerical features
###### Outlier Treatment
###### Inspecting Correlation
###### Missing Value Handling
###### Extracting new features and drop redundant ones
###### Correcting datatype
###### Univaritate and Bivariate Analysis, Data Visualization
## 3 Analyzing Categorical Features
###### Missing Value Handling
###### Encoding Categorical Features
###### Data Visualization
###### Dropping Redundant Features
## 4 Splitting data into Train and Test data
###### Transformation of Target Variable
###### Imputing Missing Values
###### Feature Scaling
## 5 Primary Feature Selection using RFE
## 6 Ridge Regression
## 7 Lasso Regression
## 8Comparing model coefficients
## 9 Model Evaluation
## 10 Choosing the final model and most significant features.



# Conclusion

###### SalePrice is the target column here.

###### All the features are then analyzed, missing data handling, outlier detection, data cleaning are done. Trend of SalePrice is observed for change in individual features.

###### New features are extracted, redundant features dropped and categorical features are encoded accordingly.

###### Then the data in split into train and test data and feature scaling is performed.

###### Target variable SalePrice is right skewed. Natural log of the same is Normal distributed, hence for model building, natural log of SalePrice is considered.

###### Creating dummy variables increased the number of features greatly, highly imbalanced columns are dropped.

###### Top 50 features are selected through RFE and adjusted R-square. 50 features : ['MSSubClass', 'LotArea', 'LandSlope', 'OverallQual', 'OverallCond', 'YearBuilt', 'BsmtQual', 'BsmtExposure', 'BsmtFinSF1', 'BsmtUnfSF', 'HeatingQC', 'CentralAir', '1stFlrSF', '2ndFlrSF', 'BsmtFullBath', 'HalfBath', 'KitchenQual', 'Functional', 'Fireplaces', 'GarageFinish', 'GarageArea', 'GarageQual', 'OpenPorchSF', 'MSZoning_RL', 'Street_Pave', 'LotConfig_CulDSac', 'Neighborhood_Edwards', 'Neighborhood_NAmes', 'Neighborhood_NWAmes', 'Neighborhood_NridgHt', 'Neighborhood_Somerst', 'Condition1_Feedr', 'Condition1_Norm', 'Condition2_Norm', 'BldgType_TwnhsE', 'RoofStyle_Gable', 'RoofStyle_Hip', 'Exterior1st_HdBoard', 'Exterior1st_Wd Sdng', 'Exterior2nd_HdBoard', 'Exterior2nd_Wd Sdng', 'MasVnrType_BrkFace', 'MasVnrType_None', 'MasVnrType_Stone', 'Foundation_PConc', 'Heating_GasA', 'GarageType_Not_applicable', 'PavedDrive_Y', 'SaleCondition_Normal', 'SaleCondition_Partial']

###### Ridge and Lasso Regression Model are built with optimum alpha calculated in GridSearchCV method. Optimum alpha = 9.0 for ridge and 0.0001 for lasso model.

###### Model evaluation is done with R2 score and Root Mean Square Error.

###### Lasso Regression is chosen as final model for having slightly better R-square value on test data.

###### Out of 50 features in the final model, top 10 features in order of descending importance are ['1stFlrSF', '2ndFlrSF', 'OverallQual', 'OverallCond', 'SaleCondition_Partial', 'LotArea', 'BsmtFinSF1','SaleCondition_Normal', 'MSZoning_RL', 'Neighborhood_Somerst']

###### Model coefficients are listed in a table along with the corresponding features , for example natural log of SalePrice will change by 0.124911 with unit change in the feature '1stFlrSF' when all the features remain constant. Negative sign in the coefficient signifies negative correlation between the predictor and target variable.

###### Predicted value of SalePrice is tranformed into its original scale by performing antilog.
