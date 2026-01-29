
# Project: Impact of Market Sentiment on Cryptocurrency Trading Performance

## Overview
This project investigates the relationship between market sentiment, as captured by a Fear & Greed Index, and cryptocurrency trading performance. By analyzing historical trade data alongside sentiment data, we aim to identify how different market sentiments influence trading profitability, volume, and effective leverage.

## Data Sources
*   **`historical_data.csv`**: Contains detailed records of individual cryptocurrency trades, including profit/loss (PnL), trade size in USD, and timestamps.
*   **`fear_greed_index.csv`**: Provides daily market sentiment classifications (e.g., 'Extreme Fear', 'Fear', 'Neutral', 'Greed', 'Extreme Greed') and a corresponding numerical value.

## Methodology
1.  **Data Loading & Preprocessing**: Both datasets were loaded, cleaned, and standardized. Timestamps were converted, and a common `date` column was created.
2.  **Data Merging**: The trading data was merged with the sentiment data on the `date` column to associate each trade with the prevailing market sentiment.
3.  **Sentiment Analysis**: The merged data was grouped by sentiment classification to calculate key trading metrics:
    *   Average PnL
    *   Total PnL
    *   Average Trading Volume (absolute USD size)
    *   Average Leverage (Total PnL / Average Volume)
4.  **Visualization**: Bar plots were generated to visualize the relationship between market sentiment and Average PnL, Average Leverage, and Average Trading Volume.

## Key Findings (Summary)
*   **Profitability**: 'Greed' and 'Fear' periods showed the highest average PnL, indicating potential opportunities in these market conditions.
*   **Leverage**: Effective leverage (PnL relative to volume) was significantly higher during 'Fear' and 'Greed' sentiments.
*   **Volume**: Trading volumes tended to be highest during 'Fear' and 'Extreme Greed', suggesting increased market activity and potentially volatility.

These findings suggest a complex, non-linear relationship between market sentiment and trading outcomes, with profitable opportunities potentially arising during both 'Greed' and 'Fear' states.

## Project Structure & Outputs
The project generates the following output files:
*   `/content/outputs/pnl_vs_sentiment.png`: Bar plot showing Average PnL vs. Market Sentiment.
*   `/content/outputs/leverage_vs_sentiment.png`: Bar plot showing Average Leverage vs. Market Sentiment.
*   `/content/outputs/volume_vs_sentiment.png`: Bar plot showing Trading Volume vs. Market Sentiment.
*   `/content/csv_files/sentiment_merged.csv`: A CSV file containing the merged historical trading and fear/greed index data.
