# Inflation-Hedging-in-NYC-Real-Estate-Quantitative-Research-Project
This paper asks whether New York metropolitan single family housing returns hedge expected and unexpected inflation in the sense of Fama and Schwert (1977), and whether that hedging relationship changed during the 2021–2022 inflation surge. 
## Overview
This repository contains a quantitative econometric analysis testing the Fama-Schwert hypothesis on the New York metropolitan area housing market. The project investigates whether single-family homes act as a reliable hedge against expected and unexpected inflation shocks over a 38-year period.

## Data Sources
Data was programmatically extracted using the `pandas-datareader` library via the **Federal Reserve Economic Data (FRED)** API. 
* **Housing Data:** [Insert specific FRED series name, e.g., NY Metro Case-Shiller Index]
* **Macroeconomic Indicators:** [Insert inflation metrics used, e.g., CPI]
* **Timeframe:** 1988 – 2026 (38 Years)

## Methodology
The analysis employs several advanced time-series techniques to isolate inflation shocks and model housing market responses:
* **Autoregressive (AR) Models:** Utilized to forecast expected inflation.
* **Ordinary Least Squares (OLS) Regression:** Applied to test the Fama-Schwert hypothesis.
* **Newey-West Standard Errors:** Implemented via `statsmodels` to correct for autocorrelation and heteroskedasticity in the time-series data.

## Key Findings
* [Insert your primary finding about housing as an inflation hedge here].
* **Structural Break:** Visualized and identified a statistically significant structural break in the market dynamics during the 2021 COVID-19 pandemic. 

## Technologies Used
* **Language:** Python
* **Libraries:** `pandas`, `pandas-datareader`, `NumPy`, `statsmodels`, `Matplotlib`

## How to Run This Project
1. Clone the repository: `git clone https://github.com/YourUsername/NY-Housing-Inflation.git`
2. Install the required dependencies: `pip install -r requirements.txt`
3. Run the Jupyter Notebook or main Python script to reproduce the extraction and regression models.
