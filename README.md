# Bitcoin Market Sentiment vs Trader Performance Analysis

## Overview

This project analyzes the relationship between **Bitcoin market
sentiment (Fear & Greed Index)** and **trader performance** using
historical trading data from Hyperliquid.

The goal is to discover patterns between trader profitability and
overall market sentiment, and extract insights that could help build
smarter trading strategies.

------------------------------------------------------------------------

## Datasets Used

### 1. Bitcoin Fear & Greed Index

Columns: - Date - Classification (Extreme Fear, Fear, Neutral, Greed,
Extreme Greed)

### 2. Hyperliquid Historical Trader Data

Columns include: - account - symbol - execution price - size - side -
time - start position - event - closedPnL - leverage

------------------------------------------------------------------------

## Methodology

1.  **Data Cleaning**
    -   Converted timestamps to datetime format
    -   Extracted trading dates
    -   Cleaned missing values
2.  **Data Merging**
    -   Merged trader data with sentiment dataset using date
3.  **Feature Engineering**
    -   Created `is_profit` column based on closedPnL
    -   Grouped trades by sentiment classification
4.  **Analysis**
    -   Profitability analysis across sentiment categories
    -   Visualization of trader performance trends

------------------------------------------------------------------------

## Key Insights

Average trader profitability by market sentiment:

  Sentiment       Profitability (%)
  --------------- -------------------
  Extreme Fear    40.49
  Fear            44.50
  Neutral         47.91
  Greed           41.13
  Extreme Greed   53.69

### Observations

-   Traders performed **best during Extreme Greed markets**.
-   **Neutral sentiment** showed relatively stable profitability.
-   **Extreme Fear markets** had the lowest profitability, indicating
    higher uncertainty.
-   Sentiment clearly influences trader success patterns.

------------------------------------------------------------------------

## Technologies Used

-   Python
-   Pandas
-   NumPy
-   Matplotlib
-   Jupyter Notebook

------------------------------------------------------------------------

## Project Structure

    bitcoin-trader-sentiment-analysis
    │
    ├── notebook.ipynb          # Main analysis notebook
    ├── fear_greed_index.csv    # Sentiment dataset
    ├── README.md               # Project documentation
    └── insights.md             # Key findings and explanations

------------------------------------------------------------------------

## Future Improvements

-   Apply machine learning models to predict trader profitability
-   Perform leverage-risk analysis
-   Analyze trader behavior patterns
-   Build an interactive dashboard for sentiment vs trading metrics

------------------------------------------------------------------------

## Author

Srihitha Chayanam
