# A Deep Learning Framework for Portfolio Performance in Commodity Market



**A Deep Learning Framework for Portfolio Performance in Commodity Market**
Department of Data Science and Engineering
Indian Institute of Science Education and Research (IISER) Bhopal, 2024

The project proposes a hybrid deep learning–based portfolio optimization framework that integrates **CNN–LSTM return forecasting** with **Hierarchical Risk Parity (HRP)** and **Genetic Algorithm (GA)** optimization to construct risk-aware commodity portfolios.

The objective is to forecast short-term commodity returns and allocate portfolio weights dynamically to improve diversification and volatility-adjusted performance.

---

## Methodology

The proposed framework consists of three major stages:

### 1. Data Collection and Preprocessing

Daily historical commodity price data (2014–2023) was collected across five sectors:

* Metals
* Energy
* Softs
* Grains
* Meats

Input features include:

* Open price
* Close price
* High price
* Low price
* Technical indicators (SMA, EMA, RSI, ROC, ATR, Momentum)

Feature selection is performed using **Pearson correlation filtering** to retain informative predictors.

Data normalization is applied before training the forecasting model.

---

### 2. CNN–LSTM Return Forecasting Model

A hybrid deep learning architecture combining **Convolutional Neural Networks (CNN)** and **Long Short-Term Memory Networks (LSTM)** is used to predict short-term commodity returns.

CNN layers:

* extract local feature patterns
* capture nonlinear relationships in indicators

LSTM layers:

* model temporal dependencies
* learn sequential financial trends

This architecture enables accurate prediction of future average returns using historical time-series data.

---

### 3. Portfolio Optimization Framework

Predicted returns are used to construct an optimized portfolio using a hybrid allocation strategy.

#### Case 1: Positive Expected Returns

Portfolio weights are computed using:

* Hierarchical Risk Parity (HRP)
* Genetic Algorithm (GA)

HRP ensures balanced risk contribution across assets, while GA searches for optimal weight allocations through evolutionary optimization.

#### Case 2: Negative Expected Returns

A short-selling strategy is applied for assets with unfavorable predicted returns.

---

### 4. Volatility-Constrained Weight Refinement

Final portfolio weights are refined using a volatility minimization objective:

Minimize:

Σ wi × Volatilityi

Subject to:

Σ wi = 1
wi constrained within a small neighborhood around initial allocations

This ensures:

* diversification
* stability
* controlled exposure
* adaptability to market conditions

---




## Author

**Amish Anand**
BS Data Science and Engineering
Indian Institute of Science Education and Research (IISER) Bhopal

