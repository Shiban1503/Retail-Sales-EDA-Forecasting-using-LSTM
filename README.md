# Retail Sales | EDA | Forecasting using LSTM

## Table of Contents
- [Purpose](#purpose)
- [Dataset Overview](#dataset-overview)
- [Steps and Implementation](#steps-and-implementation)
  - [Data Preprocessing](#data-preprocessing)
  - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
  - [Machine Learning - LSTM for Sales Prediction](#machine-learning---lstm-for-sales-prediction)
    - [Feature Engineering](#feature-engineering)
    - [Sequence Preparation](#sequence-preparation)
    - [Model Architecture](#model-architecture)
    - [Training and Evaluation](#training-and-evaluation)
- [Results](#results)
  - [Statistical Insights](#statistical-insights)
  - [Model Performance Metrics](#model-performance-metrics)
  - [Sales Analysis](#sales-analysis)
- [Conclusion](#conclusion)

## Purpose
This project aims to analyze and predict key sales metrics by leveraging historical sales, store, and macroeconomic data. By employing techniques such as Exploratory Data Analysis (EDA), data preprocessing, and advanced machine learning (specifically LSTM models), we provide actionable insights into weekly sales trends, store performance, and the impact of external factors like fuel prices, temperature, and holidays. The findings are intended to support inventory management, pricing strategies, and marketing efforts.

## Dataset Overview
The analysis is based on three datasets:

- **Features Data Set**: Contains store-specific details, such as fuel price, CPI, and markdown information.
- **Sales Data Set**: Includes weekly sales information for each store and department.
- **Stores Data Set**: Provides metadata on store types and sizes.

These datasets are merged into a single comprehensive dataset for analysis.

## Steps and Implementation

### Data Preprocessing
- Imported essential libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, etc.
- Uploaded datasets and examined data structures, missing values, and distributions.
- Converted date columns into datetime format and split them into Year, Month, and Day columns for better temporal analysis.
- Merged datasets into a single DataFrame and filled missing values with 0.
- Saved the preprocessed dataset as `processed_data.csv`.

### Exploratory Data Analysis (EDA)
EDA focused on uncovering trends and patterns in the data:

#### Fuel Price Analysis:
- Observed fluctuations over three years.
- Examined variations by store type during holidays.

#### Temperature Analysis:
- Rounded temperature into ranges for better visualization.
- Analyzed its relationship with fuel prices and CPI.

#### Weekly Sales Analysis:
- Studied weekly sales trends across three years.
- Compared holiday vs non-holiday sales through hypothesis testing.

#### Correlation Analysis:
- Identified relationships between key variables using a heatmap.

#### Store Performance:
- Ranked stores based on total weekly sales.
- Highlighted top-performing stores.

Visualizations:
- Created various plots (line, bar, scatter) to explain the data.
- Saved plots with unique filenames for easy referencing.

### Machine Learning - LSTM for Sales Prediction

#### Feature Engineering
- Selected relevant features such as temperature, fuel price, CPI, unemployment rate, markdowns, and holiday indicators.
- Encoded categorical variables (e.g., Store Type) using label encoding.
- Scaled features and target variables using `MinMaxScaler`.

#### Sequence Preparation
- Designed sequences for time-series data to feed into the LSTM model.

#### Model Architecture
- Built an LSTM model with 3 layers and dropout to prevent overfitting.
- Optimized the model using Adam optimizer and mean squared error as the loss function.

#### Training and Evaluation
- Trained the model on 80% of the data and validated it on the remaining 20%.
- Evaluated the model using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R-squared (R²).
- Visualized actual vs predicted sales and training history for deeper insights.

## Results

### Statistical Insights

#### Holiday Impact on Sales:
- A hypothesis test revealed statistically significant differences in weekly sales between holidays and non-holidays.
- T-statistic and p-value confirmed the impact of holidays on sales performance.

#### Store Rankings:
- Identified the top 3 performing stores based on total sales.

#### Feature Correlation:
- Weekly sales had notable correlations with fuel prices and CPI.

### Model Performance Metrics

- **Mean Absolute Error (MAE)**: 13,894.375
- **Mean Squared Error (MSE)**: 459,417,153.533
- **Root Mean Squared Error (RMSE)**: 21,434.019
- **R-Squared (R²) Score**: 0.126

### Sales Analysis

- **Total Sales During Holidays**: $505,299,551.56
- **Total Sales During Non-Holidays**: $6,231,919,435.55
- **Sales Difference (Holidays vs Non-Holidays)**: -$5,726,619,883.99

#### Final Insights:
- Non-holiday periods are significant for sales, with far greater sales volume than holiday periods.
- Businesses should focus their marketing efforts, promotions, and incentives during non-holiday weeks to capitalize on this trend and boost overall sales.

## Conclusion
This project provides a robust framework for analyzing and predicting retail sales data. By integrating statistical analysis, machine learning, and strategic insights, it equips stakeholders with actionable recommendations for improving store performance, optimizing inventory, and refining marketing strategies.

## Installation

To replicate this project:

1. Clone the repository:
   ```bash
   git clone https://github.com/Shiban1503/Retail-Sales-EDA-Forecasting-using-LSTM.git
   cd Retail-Sales-EDA-Forecasting-using-LSTM
   ```
2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

1. **Prepare the Data**:
   - Ensure all required CSV files (`Features data set.csv`, `sales data-set.csv`, `stores data-set.csv`) are in the project directory.

2. **Preprocess Data**:
   - Run the preprocessing script to generate `processed_data.csv`.

3. **Run the Jupyter Notebook**:
   - Open `Retail Sales Analyst - EDA.ipynb` to perform EDA and build the LSTM model.

4. **View Results**:
   - Examine visualizations and predictions stored in the `plots` folder.

---

## Project Structure
```
├── lstm_model/                # Contains the trained LSTM model files
├── plots/                     # Saved visualizations from EDA and predictions
├── Features data set.csv      # Input dataset with store-specific details
├── sales data-set.csv         # Weekly sales data
├── stores data-set.csv        # Metadata on store types and sizes
├── processed_data.csv         # Preprocessed dataset
├── Retail Sales Analyst - EDA.ipynb  # Jupyter Notebook for EDA and modeling
├── requirements.txt           # Dependencies for the project
├── README.md                  # Project documentation
└── LICENSE                    # License details
```

---

## Contributing

Contributions are welcome! If you'd like to enhance the project, follow these steps:

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add new feature"
   ```
4. Push your changes:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request describing your changes.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
