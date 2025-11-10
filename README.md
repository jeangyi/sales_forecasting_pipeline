# Sales Forecasting with CatBoost 
A time-series forecasting pipeline for daily sales prediction using **CatBoost** with **lag-based temporal features** and **recursive multi-step prediction**.

The notebook contains the complete pipeline up to the **daily and monthly forecast generation** stages.

## Limitations
Due to the Upgini free-tier API row limit (1000 rows), the enrichment stage was omitted in the forecasting pipeline and the forecasts were therefore generated locally on a downsampled dataset (600 train, 400 test). Consequently, the forecasts are likely to be inaccurate and overestimated due to limited training context with the model being trained on a smaller sample size and is lacking external enrichment in this section. 

In a full-scale implementation—with all ~19k rows and enriched external features—the same pipeline would yield smoother, more calibrated forecasts that more accurately and realistically captures seasonal patterns and sales magnitude.
