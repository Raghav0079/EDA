# Exploratory Data Analysis (EDA) Project

## Overview
This repository contains Jupyter notebooks that perform exploratory data analysis (EDA) on financial market data. The analysis focuses on understanding the structure of the dataset, identifying patterns, and deriving insights from stock market data. The notebooks include detailed steps for data preprocessing, visualization, and statistical analysis.

## Dataset Structure
The dataset used in this project contains the following columns:
- **Date**: The date of the record (object type).
- **Open**: Opening price of the stock (float64).
- **High**: Highest price of the stock during the day (float64).
- **Low**: Lowest price of the stock during the day (float64).
- **Close**: Closing price of the stock (float64).
- **Adj Close**: Adjusted closing price of the stock (float64).
- **Volume**: Number of shares traded (int64).

The dataset consists of 2,956 entries, providing a comprehensive view of stock market trends over time.

## Project Files
- **`Data analysis.ipynb`**: The main Jupyter notebook that performs the EDA. It includes:
  - Data loading and inspection.
  - Handling missing values and data cleaning.
  - Statistical summaries of the dataset.
  - Data visualization using libraries like Matplotlib and Seaborn.
  - Insights derived from the analysis.
- **`data analysis 2.ipynb`**: A supplementary notebook that explores additional aspects of the dataset, such as:
  - Advanced visualizations.
  - Correlation analysis.
  - Feature engineering for predictive modeling.

## Key Steps in the Analysis

### 1. **Data Loading**
   - The dataset is loaded into a Pandas DataFrame for analysis.
   - File I/O operations are demonstrated, including reading CSV files and handling compressed files (e.g., `.zip`).
   - The structure of the dataset is inspected using methods like `.head()`, `.info()`, and `.describe()` to understand the data types, column names, and basic statistics.

### 2. **Data Cleaning**
   - Missing values are identified using `.isnull()` and `.sum()` to determine the extent of missing data in each column.
   - Strategies for handling missing data are applied, such as:
     - Dropping rows or columns with excessive missing values.
     - Imputing missing values using statistical measures like mean, median, or mode.
   - Data types are analyzed and optimized to reduce memory usage, especially for large datasets. For example, converting `object` types to `datetime` or categorical types where applicable.

### 3. **Exploratory Analysis**
   - **Statistical Summaries**:
     - Key statistics such as mean, median, standard deviation, and percentiles are computed for numerical columns to understand the distribution and variability of the data.
   - **Time-Series Analysis**:
     - Stock price trends over time are analyzed using line plots to identify patterns such as seasonality, trends, or anomalies.
   - **Correlation Analysis**:
     - A correlation matrix is generated to identify relationships between numerical features (e.g., how `Volume` correlates with `Close` prices).
     - Insights from correlation analysis are used to determine which features might be useful for predictive modeling.

### 4. **Visualization**
   - **Line Plots**:
     - Used to visualize stock price trends (`Open`, `Close`, `High`, `Low`) over time.
   - **Histograms**:
     - Provide insights into the distribution of numerical features, such as stock prices and trading volumes.
   - **Box Plots**:
     - Highlight the spread and presence of outliers in features like `Volume` and `Close`.
   - **Heatmaps**:
     - Visualize the correlation matrix to easily identify strong positive or negative correlations between features.
   - **Scatter Plots**:
     - Explore relationships between two variables, such as `Volume` and `Close`, to identify potential dependencies.

### 5. **Insights**
   - Patterns in stock prices, such as upward or downward trends, are identified.
   - Trading volume spikes are analyzed to understand their impact on stock prices.
   - Recommendations for further analysis are provided, such as:
     - Investigating external factors (e.g., news, economic indicators) that may influence stock prices.
     - Building predictive models using features derived from the dataset.

## Requirements
To run the notebooks, ensure you have the following installed:
- Python 3.x
- Required libraries:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - zipfile
  - io

Install the required libraries using:
```sh
pip install pandas numpy matplotlib seaborn
