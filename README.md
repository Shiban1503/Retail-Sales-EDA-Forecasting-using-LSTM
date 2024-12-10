# Retail-Sales-EDA-Forecasting-using-LSTM
Purpose

This project aims to analyze and predict key sales metrics by leveraging historical sales, store, and macroeconomic data. By employing techniques such as Exploratory Data Analysis (EDA), data preprocessing, and advanced machine learning (specifically LSTM models), we provide actionable insights into weekly sales trends, store performance, and the impact of external factors like fuel prices, temperature, and holidays. The findings are intended to support inventory management, pricing strategies, and marketing efforts.

**Dataset Overview**

The analysis is based on three datasets:

Features Data Set: Contains store-specific details, such as fuel price, CPI, and markdown information.
Sales Data Set: Includes weekly sales information for each store and department.
Stores Data Set: Provides metadata on store types and sizes.
These datasets are merged into a single comprehensive dataset for analysis.

**Steps and Implementation**

1. Data Preprocessing

Imported essential libraries: pandas, numpy, matplotlib, seaborn, etc.
Uploaded datasets and examined data structures, missing values, and distributions.
Converted date columns into datetime format and split them into Year, Month, and Day columns for better temporal analysis.
Merged datasets into a single DataFrame and filled missing values with 0.
Saved the preprocessed dataset as processed_data.csv.

2. Exploratory Data Analysis (EDA)

EDA focused on uncovering trends and patterns in the data:

**Fuel Price Analysis:**
- Observed fluctuations over three years.
- Examined variations by store type during holidays.

**Temperature Analysis:**
- Rounded temperature into ranges for better visualization.
- Analyzed its relationship with fuel prices and CPI.

**Weekly Sales Analysis:**
- Studied weekly sales trends across three years.
- Compared holiday vs non-holiday sales through hypothesis testing.
  
**Correlation Analysis:**
- Identified relationships between key variables using a heatmap.

**Store Performance:**
- Ranked stores based on total weekly sales.
- Highlighted top-performing stores.

**Visualizations:**
- Created various plots (line, bar, scatter) to explain the data.
- Saved plots with unique filenames for easy referencing.
