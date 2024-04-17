Used Car Price Prediction: Machine Learning Project Report

1. Introduction

The objective of this project was to develop a machine learning model capable of predicting the prices of used cars based on various features such as make, model, age, mileage, and other relevant attributes. The ability to accurately estimate used car prices can provide valuable insights for both buyers and sellers in the automotive market, enabling informed decision-making and pricing strategies.

2. Business Understanding

From a data perspective, the task is to analyze a dataset of used car listings to identify the most important features that influence the price of a used car. This involves performing exploratory data analysis (EDA) to understand the distribution, relationships, and potential correlations among the available variables such as make, model, year, mileage, condition, and location. By employing statistical techniques like correlation analysis, feature importance ranking, and possibly machine learning algorithms such as linear regression, we aim to determine the key predictors that have the strongest impact on the price of a used car. The insights gained from this data-driven approach will provide actionable information to guide business decisions related to pricing strategies and inventory management in the used car market.

3. Data Understanding and Preparation

This project utilized a dataset containing information on 426,880 used car listings, including features such as the manufacturer, model, year, condition, mileage, and location.

The data understanding phase involved:
    1. Exploring the dataset and identifying potential data quality issues.
    2. Handling missing values by either imputing or dropping columns with a high percentage of missing data.
    3. Removing irrelevant or redundant features.
    4. One-hot encoding categorical variables.
    5. Removing outliers using the Interquartile Range (IQR) method for numerical features.

After the data preparation process, the dataset consisted of 280,508 instances and 107 features, including the encoded categorical variables.

4. Exploratory Data Analysis

To gain insights into the data and identify potential patterns or relationships, exploratory data analysis was performed. Key findings from this phase include:
    #1: The top features correlated with the price were age, vehicle type (e.g., pickup, truck, sedan), odometer (mileage), fuel type, and manufacturer.
    #2: Certain states, such as California and Oregon, had a significant impact on used car prices.
    #3: The distribution of prices and other numerical features exhibited skewness, indicating the presence of outliers.
    
5. Modeling and Evaluation

The modeling phase involved splitting the data into training and testing sets, with 80% of the data used for training and 20% for testing.

Ridge Regression Model: A Ridge regression model with hyperparameter tuning was employed to address potential multicollinearity.
    #1: The best hyperparameter (alpha) value was determined using GridSearchCV.
    #2: The model achieved an R-squared value of 0.4749, indicating that it could explain approximately 47.5% of the variance in the target variable (price).
    #3: The Mean Squared Error (MSE) was 87417142.18, and the Mean Absolute Error (MAE) was 6520.27, suggesting that the model's predictions deviated from the actual values by a considerable amount.
    #4: Feature Importance: The top 10 most important features influencing the price were: age, type_pickup, odometer, fuel_gas, type_truck, state_ca, state_or, type_sedan, manufacturer_ford, and manufacturer_nissan. The age of the vehicle, its mileage, fuel type, vehicle type, and manufacturer appeared to be the strongest drivers of used car prices.

Limitations and Recommendations: While the Ridge regression model provided some insights into the factors influencing used car prices, there were several limitations:

    #1: The relatively low R-squared value indicated that there were other important variables or complex interactions not fully accounted for in the current model.
    #2: The high MSE and MAE suggested that the model's predictions could deviate substantially from actual prices for individual instances.

To improve the model's performance and predictive power, the following recommendations were made:
    #1: Using more advanced modeling techniques, Hyperparameter Tuning, Cross-Validation. I have tried this path, however, due to the limitation of computation resources, it took too long, and I had to kill the process since I needed to use the laptop for work.
    #2: Feature engineering: I have tried to create new features by combining multiple related columns together, but the modeling result did not improve significantly, so I did not continue this path.
    #3: Better handling of outlier data: I have tried a few methods, but the result was not positive, so I decided to drop the outliers and was able to achieve slightly better accuracy with the same model.
    #4: Using domain knowledge to collect more data: The current dataset is missing some critical information, such as fuel efficiency and the car accident history.
    
6. Conclusion

In conclusion, this machine learning project aimed to predict used car prices based on various features. The Ridge regression model provided initial insights into the factors influencing prices, with age, mileage, fuel type, vehicle type, and manufacturer being the top drivers. However, the model's performance metrics indicated room for improvement.

To enhance the model's predictive power, recommendations such as feature engineering, advanced modeling techniques, hyperparameter tuning, cross-validation, handling outliers, data augmentation, domain expert collaboration, model interpretability, and continuous monitoring were proposed. By iteratively refining the modeling approach and incorporating these recommendations, a more accurate and robust used car price prediction model can be developed.

The insights gained from this project can be valuable for various stakeholders in the automotive industry, including buyers, sellers, dealerships, and online marketplaces. An accurate price prediction model can assist in making informed decisions, setting competitive prices, and optimizing inventory management strategies.

Moving forward, it is crucial to invest in high-performance servers to be able to run advanced models with large datasets, enabling us to improve the model with much higher accuracy.























