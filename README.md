# Inflation Hedging in NYC Real Estate: Quantitative Research Project

This paper asks whether New York metropolitan single-family housing returns hedge expected and unexpected inflation in the sense of Fama and Schwert (1977), and whether that hedging relationship changed during the 2021–2022 inflation surge.

## Overview
This repository contains a quantitative econometric analysis testing the Fama-Schwert hypothesis on the New York metropolitan area housing market. The project investigates whether single-family homes act as a reliable hedge against expected and unexpected inflation shocks over a 38-year period, and how the COVID-19 pandemic structurally altered that relationship.

## Data Sources
Data was programmatically extracted using the `pandas-datareader` library via the Federal Reserve Economic Data (FRED) API.

* **Housing Data:** S&P/CoreLogic Case-Shiller NY-Newark-Jersey City Home Price Index (FRED Series: `NYXRNSA`)
* **Macroeconomic Indicators:** Consumer Price Index for All Urban Consumers: All Items Less Shelter in New York-Newark-Jersey City (FRED Series: `CUURA101SA0L2`). Robustness checks utilized national CPI less shelter (`CUSR0000SA0L2`) and NY-Metro all-items CPI (`CUURA101SA0`).
* **Timeframe:** February 1987 – December 2025 (38 Years, 466 monthly observations)

## Methodology
The analysis employs several advanced time-series techniques to isolate inflation shocks and model housing market responses:
* **Autoregressive (AR) Models:** Utilized an optimal AR(1) model with seasonal dummy variables to forecast expected inflation and isolate unexpected inflation shocks (residuals).
* **Ordinary Least Squares (OLS) Regression:** Applied to test the Fama-Schwert hypothesis, evaluating if housing returns move 1-to-1 with inflation components.
* **Newey-West Standard Errors:** Implemented via `statsmodels` (with 6 lags) to correct for autocorrelation and heteroskedasticity inherent in the Case-Shiller moving-average construction.

## Key Findings
* **Baseline Failure to Hedge:** Contrary to popular belief, between 1987 and 2021, NYC single-family homes completely failed to act as a 1-to-1 hedge against either expected or unexpected inflation. 
* **The Pandemic Paradigm Shift (Structural Break):** The COVID-19 inflation shock fundamentally rewired the market. Following a statistically significant structural break identified in March 2021, the NYC housing market aggressively repriced risk, waking up to act as a nearly perfect 1-to-1 hedge against expected inflation.

## Technologies Used
* **Language:** Python
* **Libraries:** `pandas`, `pandas-datareader`, `NumPy`, `statsmodels`, `Matplotlib`

## How to Run This Project
1. Clone the repository: `git clone https://github.com/vpena987/Inflation-Hedging-in-NYC-Real-Estate-Quantitative-Research-Project.git`
2. Install the required dependencies: `pip install -r requirements.txt`
3. Run the Jupyter Notebook to reproduce the extraction, structural break tests, and regression models.
