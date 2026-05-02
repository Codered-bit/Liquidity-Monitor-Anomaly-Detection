# Liquidity-Monitor-Anomaly-Detection
A real-time liquidity monitoring system that tracks market conditions and detects anomalies in cryptocurrency trading data using statistical methods.
Overview

Liquidity is a critical component of efficient financial markets. In crypto markets, fragmented liquidity and rapid volatility make monitoring market health essential.

This project simulates how trading platforms monitor:

* Market liquidity
* Execution quality
* Abnormal trading conditions

It uses live market data to compute liquidity metrics and applies Z-score-based anomaly detection to identify statistically significant deviations.
Key Features

* Live Market Data Integration
    Fetches real-time price and order book data from exchange APIs
* Liquidity Metrics Computation
    * Bid-Ask Spread
    * Mid Price
    * Order Book Depth
* Anomaly Detection (Z-Score Based)
    Detects abnormal market conditions dynamically using rolling statistics
* Time-Series Visualization
    * Price trends
    * Spread evolution
    * Z-score anomaly signals

⸻

Methodology

Liquidity Metrics

* Mid Price = (Best Bid + Best Ask) / 2
* Spread = Best Ask − Best Bid
* Depth = Sum of order quantities

These metrics provide insight into:

* Market tightness (spread)
* Market resilience (depth)
* Pricing efficiency (mid-price)

⸻

Anomaly Detection

We use rolling Z-scores to normalize market behavior:

* Z = (X − μ) / σ

Where:

* X = current value
* μ = rolling mean
* σ = rolling standard deviation

Threshold:

* |Z| > 2 → Potential anomaly

This approach adapts to changing volatility, making it more robust than fixed thresholds.

⸻

Tech Stack

* Python
* Pandas, NumPy
* Matplotlib
* Requests (API integration)
Sample Outputs

(screenshots from Streamlit here)

* Price over time
* Spread dynamics
* Z-score anomaly detection

⸻

Key Insights

* Spread widening often correlates with increased market volatility
* Stable markets exhibit tighter spreads and lower Z-score variance
* Z-score detection effectively identifies abnormal market conditions in real time

⸻

Limitations

* Limited order book depth (top levels only)
* Short observation window
* Simple statistical model (no advanced ML yet)

⸻

Future Improvements

* Real-time deployment using dashboard frameworks
* Multi-exchange liquidity comparison
* Advanced anomaly detection (e.g., clustering, ML models)
* Liquidity quality scoring system
Live Demo

(Streamlit link)
