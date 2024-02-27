# Problem Statement
Housing price trend shows constant rise or sudden drop over the years depending on the state of the economy. To forecast a house price, people usually make a comparison with properties in similar neighborhoods. Many also utilize various websites displaying the market price of the properties. However, different websites may show different prices, making it difficult for house buyers to decide. There are also many variables that go into house pricing such as the number of bedrooms, the number of bathrooms, the square footage, the view from the house, or even its condition. Considering all these variables to make price prediction will be tedious, time-consuming and may cause biasness. This project aims to utilize machine learning for house price prediction. Multiple machine learning models are tested on the dataset containing property sales records in the USA.

# Business objective
To construct a successful price prediction model for the listed properties. This information can also be used in marketing that can attract more customers due to data transparency and competitive price.

# Data mining goals
Develop house price prediction model based on existing property sales records using machine learning, given their square footage, price, number of bedrooms, condition etc. We also want to increase accuracy in price prediction model of the listed properties.

# Dataset
For this project, the data we use is taken from [House price prediction dataset](https://www.kaggle.com/datasets/shree1992/housedata) in Kaggle.

# EDA
## Univariate Analysis
![](https://github.com/dimashidayat99/House_Price_Prediction/blob/main/result/CountFloor.png)
![](https://github.com/dimashidayat99/House_Price_Prediction/blob/main/result/CountBedroom.png)

Majority of the houses have 3 to 4 bedrooms and 1 to 2 floor.

![](https://github.com/dimashidayat99/House_Price_Prediction/blob/main/result/HistArea.png)

Majority of the houses contained around 2000 squared feet of total are of living space and around 1500 squared feet of total area above ground. While majority of the houses does not have any basement and little to no extra lot space.

## Correlation Analysis

![](https://github.com/dimashidayat99/House_Price_Prediction/blob/main/result/CorrelationPlot.png)

All the features has positive correlations with the house price except for year rennovated. The year rennovated, year built, condition, waterfront, floors and lot space have a least correlation with the house price. While unmentioned features is highly correlated with the house price.

# Modelling & Evaluation

There are 9 models will be used in this projects which are linear regression, sgd regressor, bayesian ridge, ridge, elastic net, random forest regressor, gradient boosting regressor, k-nearest neighbour regressor and xgb regressor. The models will be compared and evaluated using 2 performance metrics which are r-squared and RMSE. r-squared provides information of the gooodness of fit of a model. The higher the r-squared, the better model fits to the data. While RMSE is squared root of absolute error between predicted value and true value across the data. The lower the RMSE, the lower the error which indicate the better model.

![](https://github.com/dimashidayat99/House_Price_Prediction/blob/main/result/ModelR2.png)
![](https://github.com/dimashidayat99/House_Price_Prediction/blob/main/result/ModelR2.png)

The results of modelling shows, Ridge model achieved highest r-squared value and lowest RMSE value which are 0.64 and 285768 respectively.

# Error Analysis

![](https://github.com/dimashidayat99/House_Price_Prediction/blob/main/result/Error%20Plot%201.png)
![](https://github.com/dimashidayat99/House_Price_Prediction/blob/main/result/Error%20Plot%202.png)

The plots shows the difference between actual and predicted house price (absolute error). The plot shows, the model good enough to give correct and close price prediction since the absolute error between actual and predicted house price is relative small as shown in the plot where blue line and red line have almost similar pattern and point. However, some of the value may not be predicted accurately since as shown in the plot where the peaks of the plot have high difference between actual and predicted. This may due to the outliers in the data.



