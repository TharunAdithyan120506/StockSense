# ⚙️ StockSense: Risk-Aware ML Procurement Orchestrator

**StockSense** is an advanced supply chain resilience and logistics intelligence platform designed to predict vendor performance risks and optimize procurement strategies. By leveraging machine learning, it analyzes historical vendor data and external risk signals to prescribe risk-adjusted purchase orders, ensuring a robust and reliable supply chain.

## 🚀 Overview

In modern manufacturing, vendor delays and fulfillment failures can lead to significant production bottlenecks. StockSense addresses this by:
1. **Predicting Delays**: Estimating the number of days a vendor might deviate from the promised delivery date.
2. **Assessing Fulfillment Risk**: Predicting the ratio of items received vs. ordered.
3. **Orchestrating Procurement**: Automatically generating optimized Purchase Orders (POs) by exploding Bills of Materials (BOM) and adjusting for predicted risks.

## 🛠️ Key Features

- **Multi-Model ML Architecture**:
    - **Delay Regressor**: Predicts specific delivery delays.
    - **Fulfillment Regressor**: Estimates quantity fulfillment ratios.
    - **Risk Classifier**: Categorizes orders into risk tiers (High/Low).
- **Risk-Adjusted Procurement**: Intelligent BOM explosion that recommends split-sourcing and safety stock adjustments based on vendor reliability.
- **External Signal Integration**: Incorporates port congestion, weather risks, news sentiment, and currency volatility into the risk model.
- **Visual Analytics**: Interactive heatmaps and dashboards for vendor performance and supply chain health.

## 📁 Project Structure

```text
StockSense/
├── StockSense.ipynb       # Main analysis and orchestration notebook
├── data/                  # Data directory (CSV sources)
│   ├── bom_master.csv           # Product-Component mapping & criticality
│   ├── vendor_history.csv       # 5,000+ historical order records
│   ├── external_signals.csv     # Monthly risk indices (congestion, weather, FX)
│   └── recommended_purchase_orders.csv  # Generated output
└── README.md              # Project documentation
```

## 📊 Data Descriptions

- **BOM Master**: Contains product-to-component mappings, standard lead times, and component criticality scores.
- **Vendor History**: Detailed logs of historical orders including promised vs. actual dates, quantities, and historical performance metrics.
- **External Signals**: Dynamic monthly data covering macro-environmental factors like port congestion, weather volatility, and market sentiment.

## ⚙️ Installation & Usage

### Prerequisites
- Python 3.8+
- Jupyter Notebook or JupyterLab

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/StockSense.git
   cd StockSense
   ```
2. Install required libraries:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn
   ```

### Running the Orchestrator
1. Open the Jupyter notebook:
   ```bash
   jupyter notebook StockSense.ipynb
   ```
2. Run the cells sequentially to execute the full pipeline from Data Ingestion to Procurement Recommendations.

## 🏷️ Version
- **StockSense v1.0**
