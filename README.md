### **Forecasting Cryptocurrency Volatility: Time Series Analysis of Bitcoin Monthly Closing Prices using ARIMA Models**

### **Project Overview**

This project addresses the challenge of predicting the highly volatile valuation of Bitcoin, a decentralized digital currency that deviates significantly from the price patterns of traditional financial assets. Using a dataset of monthly average closing prices spanning nearly a decade, I developed and compared several time series forecasting models, including AR, MA, ARMA, and ARIMA. The resulting models successfully identified long-term trends, though the final evaluation revealed a Root Mean Square Error (RMSE) of approximately 21,600 on the test set, highlighting the difficulty of capturing the extreme price spikes characteristic of the 2020–2021 period.

### **Business Understanding** The primary stakeholders for this project include cryptocurrency investors, financial analysts, and regulatory bodies interested in the paradigm shift toward decentralized wealth and digital payments. The core business problem is that Bitcoin's price fluctuations are far more extreme than those of gold, stock indices, or traditional commodities, making risk management exceptionally difficult. Research into blockchain-based assets suggests that while they offer revolutionary security and transparency, their market maturity is still evolving, leading to high-variance cycles. This analysis aims to provide a quantitative framework for understanding these cycles to inform better investment and regulatory decision-making.

### **Data Understanding** The analysis utilized a historical dataset of Bitcoin’s fiscal performance.

* **Data Scope:** The features included the timestamp and the monthly average closing price.
* **Timeframe:** December 2011 to March 2021.
* **Data Limitations:** Because the model relies on monthly averages, it naturally smooths out intra-month volatility, potentially masking significant daily price crashes or surges. Furthermore, the dataset does not include exogenous variables—such as global inflation rates or regulatory announcements—which are known to influence crypto markets.
* **Exploratory Insights:** Visual analysis of the data showed a relatively stable trend for several years followed by a steep, exponential incline and substantial variance in the final 12 months, signaling a regime shift in market behavior.
<img width="897" height="470" alt="Screen Shot 2026-05-12 at 19 22 41" src="https://github.com/user-attachments/assets/f964c683-0c97-4afc-a9e5-0ff9a82805ee" />

### **Modeling and Evaluation** I implemented a series of progressively complex time series models to determine the best fit for the data:

* **Models Used:** Autoregressive (AR), Moving Average (MA), ARMA, and Autoregressive Integrated Moving Average (ARIMA).
* **Evaluation Metrics:** The primary metric for success was **Root Mean Square Error (RMSE)**.
* **Results:** The RMSE for the training data was significantly lower than that of the test set. This discrepancy indicates that while the models captured historical patterns, they struggled to generalize to the unprecedented price spikes and dips seen in the latter portion of the decade. The models proved effective at following the general direction of the trend but lacked the complexity to capture high-frequency "spikes."
<img width="899" height="464" alt="Screen Shot 2026-05-12 at 19 24 09" src="https://github.com/user-attachments/assets/f9ba57ce-d75c-4b7a-94a4-9fa35a040fec" />

### **Conclusion** While the ARIMA framework provides a solid baseline for trend analysis, the high volatility of Bitcoin suggests that historical price data alone is insufficient for high-precision forecasting. I recommend that stakeholders use these models as a directional indicator of market momentum rather than a definitive predictor of specific price points.

**Future Steps:**

* **Complexity Enhancement:** I will move beyond standard ARIMA to develop more sophisticated models such as **SARIMA** and **SARIMAX** to account for potential seasonality and external market factors.
* **Feature Integration:** Future iterations will incorporate additional features, such as trading volume and "Fear and Greed" index sentiment, to build a more generalized model capable of anticipating sudden market shifts.
