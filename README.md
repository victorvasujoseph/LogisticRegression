

### Dataset Overview

The dataset, titled "RealEstate.xlsx," contains the following columns:

1. **No**: Index number of the data point.
2. **X1 transaction date**: The date of the transaction in year and month.
3. **X2 house age**: The age of the house in years.
4. **X3 distance to the nearest MRT station**: Distance to the nearest Mass Rapid Transit (MRT) station in meters.
5. **X4 number of convenience stores**: Number of convenience stores located within walking distance.
6. **X5 latitude**: The latitude of the property.
7. **X6 longitude**: The longitude of the property.
8. **Y house price of unit area**: The house price per unit area.

### Classification Problem

To use logistic regression, we need to frame the problem as a classification problem. One approach could be to classify properties into different price brackets or categories. For instance, we could classify properties as "High Price" or "Low Price" based on a threshold value for the house price per unit area.

For this problem, let's define:

- **High Price**: If the house price per unit area is above the median price in the dataset.
- **Low Price**: If the house price per unit area is below the median price.

This classification can help in understanding the factors influencing the property's value and making informed business decisions.

### Business Decision Support

By classifying properties into high and low price categories, real estate investors, property managers, and potential buyers can:

1. **Investment Decisions**: Identify properties with a high potential return on investment based on their characteristics (e.g., proximity to MRT stations, number of convenience stores, house age).
2. **Market Analysis**: Understand the factors that significantly impact property prices, which can be useful for pricing strategies or predicting market trends.
3. **Targeted Marketing**: Target specific segments of the market more effectively by understanding what drives property value in different locations or conditions.

Next, we will perform the logistic regression analysis and provide insights based on the model's output. Let's proceed with data preparation and model training.

The dataset has been updated with a new binary column, **Price Category**, where:

- **0** indicates a property price below the median price (38.45 per unit area).
- **1** indicates a property price above the median price.

This classification will allow us to explore which factors significantly contribute to a property being in the high or low price category.

Now, we'll perform logistic regression using the selected features to predict the Price Category. This will help in understanding the influence of different factors like house age, distance to MRT stations, the number of convenience stores, and geographical coordinates on the property's price category. Let's proceed with the logistic regression model training and evaluation.

### Logistic Regression Model Evaluation

The logistic regression model has been trained and evaluated on the test set. Here are the key metrics:

#### Classification Report:
- **Precision**: 
  - Class 0 (Low Price): 0.89
  - Class 1 (High Price): 0.69
- **Recall**:
  - Class 0 (Low Price): 0.71
  - Class 1 (High Price): 0.89
- **F1-Score**:
  - Class 0 (Low Price): 0.79
  - Class 1 (High Price): 0.78
- **Overall Accuracy**: 0.78

#### Confusion Matrix:
- True Positives (High Price correctly identified): 47
- True Negatives (Low Price correctly identified): 51
- False Positives (Low Price incorrectly identified as High Price): 21
- False Negatives (High Price incorrectly identified as Low Price): 6

### Insights and Business Decision Support

The logistic regression model can help real estate professionals understand the likelihood of a property being in the high or low price category based on various factors. The model's results indicate:

1. **Investment Strategies**: Investors can use this model to prioritize properties that are more likely to be in the high price category, focusing on attributes like proximity to MRT stations, property age, and the number of convenience stores nearby.

2. **Pricing Strategy**: Property managers can set competitive prices by understanding which features most significantly impact property values. For example, properties near MRT stations or with more convenience stores may be priced higher.

3. **Targeted Marketing**: Marketing efforts can be tailored based on the likelihood of properties being in the high or low price categories, focusing on different buyer segments accordingly.

