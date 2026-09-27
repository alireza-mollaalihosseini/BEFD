# Interest Rates and Exchange Rates – Time-Series Modelling

Course project for *Business, Economic and Financial Data* (M.Sc. Physics of Data, University of Padova,
2021/22).

**Question:** how well does the 1-year US Treasury rate explain the 3-year rate, and how do US interest
rates relate to the Chinese yuan and Mexican peso exchange rates?

## Data

Daily US Treasury constant-maturity rates (1-year and 3-year, January 1962 – December 2021) from FRED
(Federal Reserve Bank of St. Louis), and the CNY/USD and MXN/USD exchange rates. The CSV files are not
included.

## Models

* Linear regression of the 3-year rate on the 1-year rate and a trend, followed by ARIMA models of the
  regression residuals.
* ARIMA models of the 3-year rate itself.
* Generalized additive models (GAM) with smooth terms.
* The same linear + ARIMA approach for the yuan and peso exchange rates.
* Gradient boosting regression with PyCaret in Python (`BEFD_GB.ipynb`).

The statistical models were fitted in R and are documented, with diagnostics and plots, in the slides.

## Files

| File | Contents |
|---|---|
| `BEFD_Project_Alireza_MollaAliHosseini.pdf` | Presentation (38 slides): background, models, diagnostics, conclusions |
| `BEFD_GB.ipynb` | Gradient boosting models for the interest-rate, yuan and peso datasets |
