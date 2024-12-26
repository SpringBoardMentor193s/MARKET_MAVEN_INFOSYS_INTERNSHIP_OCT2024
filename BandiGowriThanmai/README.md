Market Maven

This project provides tools to preprocess, visualize, and forecast sales data for supermarkets. It uses machine learning models to optimize sales, predict profits, and generate insights for better decision-making.

Features

Preprocesses supermarket sales data for analysis.

Generates exploratory visualizations.

Trains a Random Forest Regressor for sales prediction.

Implements hyperparameter tuning for model optimization.

Calculates profit margins and optimized sales for better business insights.

Saves trained models for reuse.

Installation

Requirements

Python 3.8+

Libraries:

pandas

numpy

joblib

matplotlib

scikit-learn

openpyxl (for Excel file handling)

Steps

Clone this repository:

git clone https://github.com/your-repo-name/supermarket-sales-analysis.git

Install required dependencies:

pip install -r requirements.txt

Ensure your dataset is in Excel format and includes the following columns:

Date, Time, Invoice ID, Branch, City, Customer type, Gender,Product line, Unit price, Quantity, Tax 5%, Total, cogs,gross income, Rating, Payment.

Usage

1. Sales Prediction and Model Training

To train a Random Forest Regressor, save the trained model, and evaluate its performance:

from your_module_name import train_and_predict_model

# Example usage:
metrics = train_and_predict_model(input_file='sales_data.xlsx', model_file='rf_model.pkl')
print(metrics)

2. Profit Optimization and Hyperparameter Tuning

To perform profit optimization using sales data and hyperparameter tuning:

from your_module_name import hyperparameter_tuning

# Example usage:
hyperparameter_tuning(file_path='sales_data.xlsx', output_file='profits.csv', model_file='rf_optimized.pkl')

3. Visualizations

Generate visualizations for exploratory data analysis (EDA). Examples:

Revenue per unit trends

Total sales distribution

Product-line-specific insights

You can customize matplotlib or seaborn scripts based on your analysis needs.

Outputs

Trained Model: Saved as a .pkl file for reuse.

Metrics: Mean Squared Error (MSE) and R² values for model performance.

Processed Dataset: Adds columns like:

RevenuePerUnit, LogTotal, ProfitMargin, OptimizedSales.

Learning Curve: Visual representation of training and validation errors.

Dataset Description

Input Columns:

Invoice ID, Date, Time, Branch, City, Customer type,Gender, Product line, Unit price, Quantity, Tax 5%, Total,cogs, gross income, Rating, Payment.

Engineered Features:

RevenuePerUnit: Revenue generated per unit sold.

LogTotal: Log-transformed total sales for outlier handling.

ProfitMargin: Ratio of profit to total sales.

OptimizedSales: Predicted sales with optimized profits.

Model Details

Algorithms Used:

Random Forest Regressor:

Robust and efficient for structured data.

Tuned using RandomizedSearchCV.

Evaluation Metrics:

Mean Squared Error (MSE): Measures average squared error.

R² Score: Indicates variance explained by the model.

Contribution

Feel free to fork the repository and submit pull requests. Suggestions and improvements are always welcome!

License

This project is licensed under the MIT License.

