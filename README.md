# Home Value Forecasting: Enhancing Real Estate Insights

<p align="middle">
<img src="https://github.com/dimashidayat99/House_Price_Prediction/assets/69446089/c9bd7881-405f-4729-83d8-0f79fefcbf33"  width="800" />
</p>

# Problem Statement
The housing price trend shows a constant rise or sudden drop over the years depending on the state of the economy. To forecast a house price, people usually make a comparison with properties in similar neighborhoods. Many also utilize various websites displaying the market price of the properties. However, different websites may show different prices, making it difficult for house buyers to decide. Many variables go into house pricing such as the number of bedrooms, the number of bathrooms, the square footage, the view from the house, or even its condition. Considering all these variables to make price predictions will be tedious, time-consuming, and may cause biases. This project aims to utilize machine learning for house price prediction. Multiple machine learning models are tested on the dataset containing property sales records in the USA.

# Business objective
To construct a successful price prediction model for the listed properties. This information can also be used in marketing that attract more customers due to data transparency and competitive prices.

# Data mining goals
Develop a house price prediction model based on existing property sales records using machine learning, given their square footage, price, number of bedrooms, condition, etc. We also want to increase the accuracy of the price prediction model of the listed properties.

# Dataset
For this project, the data we use is taken from [House price prediction dataset](https://www.kaggle.com/datasets/shree1992/housedata) in Kaggle.

# EDA
## Univariate Analysis
![](https://github.com/dimashidayat99/House_Price_Prediction/blob/main/result/CountFloor.png)
![](https://github.com/dimashidayat99/House_Price_Prediction/blob/main/result/CountBedroom.png)

The majority of the houses have 3 to 4 bedrooms and 1 to 2 floors.

![](https://github.com/dimashidayat99/House_Price_Prediction/blob/main/result/HistArea.png)

The majority of the houses contained around 2000 square feet of total area of living space and around 1500 square feet of total area above ground. While majority of the houses do not have any basement and little to no extra lot space.

## Correlation Analysis

![](https://github.com/dimashidayat99/House_Price_Prediction/blob/main/result/CorrelationPlot.png)

All the features have positive correlations with the house price except for the year renovated. The year renovated, year built, condition, waterfront, floors, and lot space have the least correlation with the house price. While unmentioned features are highly correlated with the house price.

# Modelling & Evaluation

Nine models will be used in this project which are Linear Regression, SGD Regressor, Bayesian Ridge, Ridge, Elastic Net, Random Forest Regressor, Gradient Boosting Regressor, K-Nearest Neighbor Regressor, and XGB Regressor. The models will be compared and evaluated using 2 performance metrics which are r-squared and RMSE. r-squared provides information on the goodness of fit of a model. The higher the r-squared, the better the model fits the data. While RMSE is the squared root of absolute error between predicted value and true value across the data. The lower the RMSE, the lower the error which indicates the better model.

![](https://github.com/dimashidayat99/House_Price_Prediction/blob/main/result/ModelR2.png)
![](https://github.com/dimashidayat99/House_Price_Prediction/blob/main/result/ModelR2.png)

The results of modeling show, that the Ridge model achieved the highest r-squared value and lowest RMSE value which are 0.64 and 285768 respectively.

# Error Analysis

![](https://github.com/dimashidayat99/House_Price_Prediction/blob/main/result/Error%20Plot%201.png)
![](https://github.com/dimashidayat99/House_Price_Prediction/blob/main/result/Error%20Plot%202.png)

The plots show the difference between actual and predicted house prices (absolute error). The plot shows, that the model is good enough to give correct and close price predictions since the absolute error between actual and predicted house prices is relatively small as shown in the plot where the blue line and red line have almost similar patterns and points. However, some of the values may not be predicted accurately since as shown in the plot where the peaks of the plot have a high difference between actual and predicted. This may be due to the outliers in the data.



