# Market Maven 

## Overview
This project uses a **Random Forest Regressor** model to predict the total sales (`Product_Store_Sales_Total`) for products in stores based on various features in the dataset. The dataset undergoes preprocessing, feature engineering, hyperparameter tuning, and evaluation to ensure an optimized and accurate prediction model.

---

## Dataset
The dataset (`SuperKart.csv`) contains the following columns:
- `Product_Id`: Unique identifier for each product (dropped during preprocessing).
- `Product_Weight`: Weight of the product.
- `Product_Type`: Type of the product.
- `Product_Allocated_Area`: Allocated shelf area for the product in the store.
- `Product_Sugar_Content`: Sugar content in the product (e.g., No Sugar, Low Sugar).
- `Product_MRP`: Maximum retail price of the product.
- `Store_Id`: Unique identifier for each store (dropped during preprocessing).
- `Store_Size`: Size of the store (Small, Medium, Large).
- `Store_Type`: Type of store.
- `Store_Location_City_Type`: Type of city where the store is located.
- `Store_Establishment_Year`: Year the store was established (used to compute `Store_Age`).
- `Product_Store_Sales_Total`: Total sales of the product (Target column).

---

## Preprocessing Steps
1. **Handling Missing Values:**
   - Numerical columns (e.g., `Product_Weight`, `Product_Allocated_Area`, `Product_MRP`) were filled with their mean values.
   - Categorical columns (e.g., `Store_Size`) were filled with their mode values.
   - `Product_Sugar_Content` missing values were filled with "Unknown."

2. **Categorical Encoding:**
   - `Product_Sugar_Content` and `Store_Size` were mapped to numeric values.
   - Other categorical columns (e.g., `Product_Type`, `Store_Type`) were label-encoded using `LabelEncoder`.

3. **Feature Engineering:**
   - `Store_Age` was calculated as `2024 - Store_Establishment_Year`.

4. **Outlier Handling:**
   - Outliers in numerical columns were removed using the Z-score method (threshold = 3).

5. **Normalization:**
   - Numerical columns were scaled using `MinMaxScaler` to bring all values into the range [0, 1].

6. **Dropped Irrelevant Columns:**
   - `Product_Id`, `Store_Id`, and `Store_Establishment_Year` were dropped as they do not contribute directly to the predictions.

---

## Model Building and Tuning
1. **Model Selection:**
   - A **Random Forest Regressor** was chosen for its ability to handle complex relationships and avoid overfitting.

2. **Hyperparameter Tuning:**
   - The `RandomizedSearchCV` function was used to optimize hyperparameters:
     - `n_estimators`: Number of trees in the forest (100, 200).
     - `max_depth`: Maximum depth of each tree (10, 20, None).
     - `min_samples_split`: Minimum samples required to split a node (2, 5).
     - `min_samples_leaf`: Minimum samples required at a leaf node (1, 2).

3. **Cross-Validation:**
   - A 3-fold cross-validation was applied during hyperparameter tuning.

---

## Evaluation Metrics
The model's performance is evaluated using:
- **Mean Absolute Error (MAE):** Measures average magnitude of errors in predictions.
- **Mean Squared Error (MSE):** Penalizes larger errors more heavily.
- **Root Mean Squared Error (RMSE):** Square root of MSE, interpretable in the same units as the target variable.
- **R-squared (R2):** Proportion of variance in the target variable explained by the model.

---

## Results
After hyperparameter tuning, the model achieved the following metrics on the test data:
- **Mean Absolute Error (MAE):** [Insert Value]
- **Mean Squared Error (MSE):** [Insert Value]
- **Root Mean Squared Error (RMSE):** [Insert Value]
- **R-squared (R2):** [Insert Value]

---

## How to Use the Code
1. **Prerequisites:**
   - Python 3.x
   - Libraries: `scikit-learn`, `pandas`, `numpy`, `scipy`

2. **Run the Code:**
   - Place the `SuperKart.csv` file in the same directory as the script.
   - Execute the script to preprocess the data, train the model, and evaluate it.

3. **Modify Hyperparameters:**
   - Update the `param_grid` dictionary in the code to test different hyperparameter values.

---

## Future Enhancements
- Implement additional feature engineering techniques.
- Explore advanced models like Gradient Boosting Machines or Neural Networks.
- Visualize feature importance for better interpretability.

---

## Acknowledgments
Special thanks to the contributors of the **scikit-learn** and **pandas** libraries for making machine learning accessible and efficient.

