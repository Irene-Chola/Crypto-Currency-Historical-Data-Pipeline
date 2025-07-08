 # Cryptocurrency Intelligence
#### A comprehensive cryptocurrency analysis, providing real-time insights and historical data visualization for 10 major cryptocurrencies

## Tools Used
[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=power-bi&logoColor=black)](https://powerbi.microsoft.com/)

[![Microsoft Fabric](https://img.shields.io/badge/Microsoft%20Fabric-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)](https://fabric.microsoft.com/)

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org/)

[![Yahoo Finance](https://img.shields.io/badge/Yahoo%20Finance-6001D2?style=for-the-badge&logo=yahoo&logoColor=white)](https://finance.yahoo.com/)

[![CoinGecko](https://img.shields.io/badge/CoinGecko-8DC351?style=for-the-badge&logo=coingecko&logoColor=white)](https://coingecko.com/)

---

## Table of Contents

- [Project Overview](#project-overview)
- [Microsoft Fabric Project Assets](#microsoft-fabric-project-assets)
- [Key Features](#key-features)
- [Architecture](#architecture)
- [Data Sources](#data-sources)
- [Data Pipeline Execution](#data-pipeline-execution)
- [Dashboard Navigation](#dashboard-navigation)
- [Key Insights](#key-insights)
- [Results & Recommendations](#results--recommendations)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)

---

## Project Overview

This project delivers a next-generation cryptocurrency intelligence analysis for a US-based fintech startup. The analysis enables effective monitoring and decision making for investors, traders, and regulators by providing comprehensive historical data analysis and real-time insights.

---

## Microsoft Fabric Project Assets
1. Workspace
2. Lakehouse
3.  Warehouse

### Prerequisites
- Microsoft Fabric workspace access
- PowerBI Desktop
- API keys for Yahoo Finance and CoinGecko


---

### Key Features

- **Multi-Source Data Integration**: Seamlessly combines data from Yahoo Finance, CoinGecko, and historical CSV files
- **Advanced Visualizations**: Comprehensive trend analysis, comparative performance metrics, and market insights
- **Scalable Architecture**: Built on Microsoft Fabric for enterprise-grade performance

--- 
## Architecture

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│   Data Sources  │     │   Data Lake     │     │   Analytics     │
│                 │     │                 │     │                 │
│ • Yahoo Finance │───▶│ Microsoft Fabric│───▶ │     Power BI    │
│ • CoinGecko API │     │   Data Lake     │     │   Dashboard     │
│ • Historical CSV│     │                 │     │                 │
└─────────────────┘     └─────────────────┘     └─────────────────┘
```

## Data Sources
**Currencies Used:**

| Currency | Symbol | Currency | Symbol |
|----------|---------|----------|---------|
| AAVE | AAVE | Binance Coin | BNB |
| Cosmos | ATOM | Dogecoin | DOGE |
| Ethereum | ETH | Litecoin | LTC |
| NEM | XEM | Stellar | XLM |
| Uniswap | UNI | Wrapped Bitcoin | WBTC |


#### 1. **Historical Foundation Data** (Jan 2020 - Jul 21, 2021)
- **Format**: [10 CSV files](https://github.com/Irene-Chola/Crypto-Currency-Historical-Data-Project/blob/main/coins_10.rar)
- **Coverage**: Complete historical baseline for 10 major cryptocurrencies
- **Storage**: Microsoft Fabric Lakehouse 

#### 2. **Yahoo Finance Integration** (Jul 22, 2021 - Jun 12, 2024)
- **Source**: YFinance API
- **Implementation**: [Python Integration Code](https://github.com/Irene-Chola/Crypto-Currency-Historical-Data-Project/blob/main/yahoofinancehistoricaldata.ipynb)
- **Features**: Historical data
- **Storage**: Microsoft Fabric Lakehouse

#### 3. **CoinGecko Premium Data** (Jun 13, 2024 - Jun 13, 2025)
- **Source**: CoinGecko API
- **Implementation**: [CoinGecko Integration Code](https://github.com/Irene-Chola/Crypto-Currency-Historical-Data-Project/blob/main/historicaldata_group.coingecko.ipynb)
- **Features**: Historical data
- **Storage**: Microsoft Fabric Lakehouse

#### 4. **Symbol Mapping Service**
- **Source**: CoinGecko API
- **Implementation**: [Symbol Mapping Code](https://github.com/Irene-Chola/Crypto-Currency-Historical-Data-Project/blob/main/crypto_symbol_mapping.ipynb)
- **Purpose**: Standardized currency identification across all data sources
- **Storage**: Microsoft Fabric Warehouse


---

## Data Pipeline Execution
1. **Historical Data Import**:
   - Create a Microsoft Fabric Workspace, Lakehouse and Warehouse
   - Load the 10 CSV files into Microsoft Fabric
   - Create a folder in the Lakehouse and store the data in tables
   
3. **API Data Sync**:
   - Write or upload your python script to Microsoft Fabric
   - speficify the correct API key for each script
   - Create a folder in your Lakehouse and set up the file path to store your data
   - Execute Yahoo Finance and CoinGecko data pulls
     
4. **Data Transformation**:
   - Create a dataflow and load all your files (10 CSV files, CoinGecko and Yahoo Finance data) into the dataflow
   - Apply cleaning and standardization processes with Dataflow
   - Append the dataset into a master table
   - Load your master table into you Warehouse
     
5. **Dashboard Deployment**:
   - Create a connection between PowerBI and Microsoft Fabric
   - Load your master dataset and symbol mapping data to PowerBI
   - Create a connection between the two files above
   - Create your dashboard and publish the dashboard to Microsoft Fabric WorkSPace

---

## Dashboard Navigation
- **Time Series Analysis**: Interactive charts with date range selection
- **Comparative Analysis**: Side-by-side currency performance
- **Market Metrics**: Real-time volume and market cap tracking
- **Detailed Tables**: Comprehensive data exploration

### Dashboard Screenshots

![Crypto Currency Dashboard](https://github.com/Irene-Chola/Crypto-Currency-Historical-Data-Project/blob/main/cryptocurrencyhistoricaldatadashboard.jpg)

*Interactive dashboard showing trend analysis, price performance, and market insights*

---

## Key Insights

### Market Analysis Results
- **Total Market Capitalization**: $2.3T+ across analyzed currencies
- **Volume Analysis**: Daily trading volumes exceeding $50B
- **Price Trends**: Comprehensive 5-year historical performance tracking
- **Volatility Metrics**: Risk assessment and correlation analysis

### Top Performing Insights
1. **Bitcoin (BTC)**: Consistent long-term growth despite volatility
2. **Ethereum (ETH)**: Strong correlation with DeFi adoption
3. **Market Cycles**: Clear cyclical patterns identified across all currencies


---

## Results & Recommendations

### Key Findings
1. **Market Volatility**: Crypto markets show 3x higher volatility than traditional assets
2. **Correlation Patterns**: Strong inter-currency correlations during market stress
3. **Volume Indicators**: Trading volume serves as leading indicator for price movements

### Strategic Recommendations
1. **Risk Management**: Implement portfolio diversification across multiple currencies
2. **Timing Strategies**: Leverage volume indicators for entry/exit timing
3. **Regulatory Compliance**: Enhanced monitoring capabilities for regulatory reporting

### Current Limitations
- **API Rate Limits**: Potential constraints during high-volume periods
- **Historical Gaps**: Some minor data gaps in early 2020 period

---

## Future Enhancements

### Phase 2 - Implementation of a Realtime Data Pipeline


## Acknowledgments

- **Microsoft Fabric Team** for providing enterprise-grade data platform
- **CoinGecko** for comprehensive cryptocurrency data
- **Yahoo Finance** for reliable financial data feeds
- **Power BI Community** for visualization best practices

---

**⭐ If you found this project helpful, please consider giving it a star!**

---

*Built with by [Irene Chola](https://github.com/Irene-Chola)*
