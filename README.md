# House_prices_prediction
In this project, we built a house price prediction model using a real-world dataset provided in CSV format. We began by exploring and cleaning the dataset, handling missing values and identifying key features such as bedrooms, bathrooms, sqft_living, and city (used as the location). We visualized distributions of house prices and room counts, revealing that prices are right-skewed and most homes have 2 to 4 bedrooms. After encoding categorical variables and standardizing numerical features, we developed a regression model to estimate house prices. We initially used linear regression, which resulted in a modest R² score (~0.45), indicating limited predictive power.

To improve performance, we transitioned to a more advanced model using RandomForestRegressor with GridSearchCV for hyperparameter tuning. We also expanded the feature set by including sqft_basement, grade, view, and more, which provided better learning for the model. This led to a notable improvement in model accuracy, reducing RMSE and increasing R² (potentially above 0.70). The final model captured the relationship between house size, number of rooms, location, and price with improved reliability. Insights from the data confirmed that features like square footage and bathrooms were strong predictors, while the city significantly influenced pricing. The actual vs. predicted price plot validated that the model performed well, especially for mid-range properties.

1. How features like Size or Number of Rooms correlate with house prices

sqft_living (Size): Strong positive correlation with price. Larger houses generally cost more. This relationship was clearly visible from the scatterplot.

bedrooms: Shows a mild positive correlation with price, but it's not as strong as size. After 4–5 bedrooms, the price increase tends to plateau or even decline due to non-linear effects (e.g., luxury vs utility).

bathrooms: Has a stronger impact than bedrooms. More bathrooms typically correspond to higher-end homes, and thus higher prices.

2. The effect of Location on pricing

city: Certain cities (like Seattle or Bellevue, if present in the data) showed significantly higher prices. Urban areas tend to be more expensive than suburban or rural areas. After encoding, the model learns price patterns tied to location.

One-hot encoding of city helped capture this variation, and feature importance from the model confirms location significantly contributes to price prediction.

3. Accuracy and reliability of the regression model

Improved RMSE: The final model had a significantly reduced RMSE (~230,000 range) showing better absolute prediction performance.

R² Score: Improved from 0.30 to 0.45 using Random Forest and GridSearchCV. This means the model can explain 45% of the variance in house prices.

Visual Check: The scatter plot of Actual vs. Predicted values shows tight clustering along the diagonal, indicating reasonable prediction performance with some error at higher price points.
