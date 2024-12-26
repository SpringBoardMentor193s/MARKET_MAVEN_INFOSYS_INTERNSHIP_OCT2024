# Supermarket Profit Prediction and Analysis

This repository contains a machine learning project for analyzing and predicting supermarket profits using Python. It leverages a Streamlit-based user interface for ease of interaction, data visualization, and model interpretation.

## Project Features

- **Data Preprocessing**:
  - Converts date information into year, month, and day features.
  - Handles missing values and encodes categorical data.
  - Creates a new feature for profit margin analysis.

- **Model Training**:
  - Uses a Random Forest Regressor for predicting profits.
  - Evaluates model performance with metrics like MAE, MSE, and R².

- **Visualizations**:
  - Correlation heatmap.
  - Profit distribution.
  - Sales vs. Profit, Discount vs. Profit scatter plots.
  - Actual vs. Predicted profit comparisons.

- **Recommendations**:
  - Insights into adjusting discounts, focusing on high-profit categories, and improving profit margins.

- **Download Options**:
  - Download the trained model (`random_forest_model.pkl`).
  - Download optimized sales data.

## Files in the Repository

1. **`Final_supermartdata.csv`**: The dataset used for training and analysis.
2. **`Model_train.py`**: The main Python script for data preprocessing, training the model, and deploying the Streamlit interface.

## Setup Instructions

1. Clone this repository:
   
   git clone (https://github.com/SpringBoardMentor193s/MARKET_MAVEN_INFOSYS_INTERNSHIP_OCT2024/Madhu_Project
cd MARKET_MAVEN_INFOSYS_INTERNSHIP_OCT2024/Madhu_Project
2. Install the required dependencies:

   pip install -r requirements.txt
  
   *(Note: Create a `requirements.txt` file with the libraries listed in your script.)*

3. Run the Streamlit application:

   streamlit run Model_train.py


4. Upload the dataset (`Final_supermartdata.csv`) through the Streamlit interface.

## Usage

- **Upload CSV Data**: Use the sidebar to upload your dataset.
- **View Metrics and Visualizations**: Observe model evaluation metrics and insights through interactive plots.
- **Download Results**: Save the trained model or optimized data for further analysis.

## Key Dependencies

- Python
- Pandas
- NumPy
- Scikit-learn
- Streamlit
- Matplotlib
- Seaborn
- Joblib

## Project Insights

This project offers actionable insights for supermarkets to optimize their sales strategies and boost profitability. The predictive model and visualizations assist in understanding sales trends and profit influencers.
##License
This project is licensed under the MIT License.
