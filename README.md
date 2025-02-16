Project Summary: Recipe Site Traffic Prediction
Introduction:

The project aims to build a predictive model to identify high-traffic recipes for a recipe website. This is crucial for optimizing content strategy, attracting more visitors, and potentially boosting subscriptions. The project uses a dataset named "recipe_site_traffic_2212.csv" containing information about recipes and their website traffic.

1. Data Validation:

The dataset was validated and cleaned to ensure data quality. Steps included:

- Handling missing values: Missing values in nutritional columns were dropped, and NaN values in 'high_traffic' were replaced with "Low".
- Data type conversion: The 'servings' column was cleaned and converted to integer type, and 'category' was converted to categorical type.
- Data consistency: Invalid entries in the 'category' column were replaced with correct values.

2. Exploratory Data Analysis:

Analysis was conducted to understand data characteristics and relationships between variables. Key findings include:

- Recipe categories like 'Chicken', 'Dessert', and 'Breakfast' are popular, while 'One Dish Meal' is less common.
- Recipes designed for 4 servings are most prevalent.
- There's a correlation between high traffic and recipes for 6 servings.
- Vegetable, Potato, and Pork categories attract the most visitors.
- The Beverages category has the lowest traffic.

3. Model Development:

Binary classification models were used to predict high-traffic recipes. The process involved:

- Encoding: Categorical features were encoded using pandas get_dummies().
- Data splitting: The dataset was split into training (80%) and testing (20%) sets, with stratification to maintain target variable proportions.
- Data scaling: Numerical features were scaled using PowerTransformer to handle skewed distributions.
- Model selection: Logistic Regression, KNeighborsClassifier, and Decision Tree were chosen as baseline and comparison models.

4. Model Evaluation:

Models were evaluated using accuracy, precision, and recall.

- Logistic Regression performed best on the test set with 81.56% accuracy and 83.64% precision.
- KNN and Decision Tree showed signs of overfitting on the training set, resulting in lower performance on the test set.

5. Business Metrics:

- Precision@K was used to measure the model's ability to identify high-traffic recipes with 80% precision.
- Logistic Regression achieved a High Traffic Conversion Rate of 88%.

6. Recommendations:

Based on the findings, the following recommendations were made:

- Prioritize 6-serving recipes and categories like Vegetable, Potato, and Pork for content creation.
- Investigate and improve engagement in the Beverages category.
- Continuously collect data to enhance model accuracy.
- Conduct A/B testing to validate model predictions.

Submission:
The workspace containing the report and code will be published and submitted through the DataCamp Certification Dashboard and Github.
