# Retail Price Optimization
This project demonstrates how to use machine learning techniques to optimize retail prices in order to maximize revenue and profit. We analyze historical retail data and competitor pricing, build visualizations, and train a regression model to predict the ideal total price based on key product and competitive factors.

**Project Overview**
Retail price optimization involves determining the best price point for products to maximize profitability while staying competitive in the market. In this project, we:
 - Analyze product pricing, quantity, and competitor data
 - Visualize trends and patterns using Plotly
 - Calculate price difference against competitors
 - Build and evaluate a Decision Tree Regressor to predict total price
 - Create an interpretable dashboard of results and metrics

**Dataset**
The dataset contains 676 retail records and includes features such as:
 - Product ID and category
 - Quantity sold, unit price, total price
 - Freight charges, customer count
 - Product metadata (lengths, weights, photos)
 - Competitor prices (comp_1, comp_2, comp_3)
 - Review scores and previous pricing (lag_price
   
**Exploratory Data Analysis**
Performed the following EDA tasks:
 - Distribution of total and unit prices (Histogram, Boxplot)
 - Relationship between quantity and price (Scatter with trendline)
 - Price comparison by product category, weekday, and holidays
 - Correlation matrix to understand inter-feature relationships
 - Visualizations built using Plotly for interactivity

**Feature Engineering**
 - Created a new feature:
       comp_price_diff = unit_price - comp_1
       to capture price deviation from the primary competitor.

**Model Building**
Used Decision Tree Regressor to predict the total price based on selected features:
Features used:
['qty', 'unit_price', 'comp_1', 'product_score', 'comp_price_diff']
 - Split the data (80/20) for training and testing
 - Visualized actual vs. predicted prices
 - Evaluated model fit visually with scatter plot

**Results Visualization**
 - Actual vs Predicted retail prices plotted
 - Ideal prediction line shown for reference
 - Model learns non-linear relationships in data

**Key Learnings**
 - Competitor pricing greatly influences optimal retail price
 - Data visualization is essential for pricing strategy insights
 - Decision Trees can capture pricing dynamics in non-linear relationships

**Future Improvements**
 - Tune the model using GridSearchCV
 - Try other regressors (RandomForest, XGBoost, Lasso)
 - Include time series decomposition or lag features
 - Add profit margin optimization
