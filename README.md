#  Car Price Prediction Project

## Project Overview
This project focuses on predicting car prices using a dataset of vehicle specifications. It demonstrates a complete machine learning workflow, including deep data cleaning,, and a comparative study between different regression models.

##  Data Cleaning & Challenges
The project involved handling significant data quality issues to improve model reliability:
* Handling Outliers: Addressed extreme price points (e.g., cars listed for $1 or negative values like $-5000 in the test set).
* String Cleaning: Processed columns like Mileage (removing 'km') and Engine volume (removing 'Turbo') to convert them into numerical formats.
* Missing Data: Implemented median imputation for Levy and Mileage, and handled 'unknown' values in categorical columns.
* Feature Encoding: Applied One-Hot Encoding to categorical features like Manufacturer and Category.

##  Modeling & Performance
We compared two primary models to find the best fit for our data:

### 1. Linear Regression
* Validation R² Score: Initially struggled with outliers.
* Final Test R² Score: 0.7006 (showing strong performance after final data tuning).

### 2. Random Forest Regressor
* R² Score: 0.6470.
* Mean Absolute Error (MAE): $4,585.21.
* Strength: Excellent at identifying non-linear relationships and providing feature importance insights.

##  Visual Insights (Top Drivers of Price)
According to our Random Forest analysis, the most influential factors are:
1. Production Year: The most critical factor in determining value.
2. Airbags: Significant impact, indicating a premium on safety features.
3. Mileage: A key indicator of vehicle wear and depreciation.

##  Future Additions
* Saving models in .pkl format for production use.

##  Project Structure
`text
└── src/
    ├── data/
    │   ├── test_car_price.csv      # Unseen testing dataset
    │   └── train_car_price.csv     # Training dataset
    ├── notebooks/
    │   ├── EDA-2.ipynb            # Main development, EDA, and training
    │   ├── car_price_model.pkl    # Final exported the model
    │   ├── scaler.pkl             # Exported RobustScaler for data normalization
    │   └── requirments.txt        # libraries needed
    ├── .gitignore                 # Files to exclude from version control
    └── README.md
