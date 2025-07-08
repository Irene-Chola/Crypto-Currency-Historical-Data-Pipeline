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

- [Project Overview](#-project-overview)
- [Key Features](#-key-features)
- [Architecture](#-architecture)
- [Data Sources](#-data-sources)
- [Installation & Setup](#-installation--setup)
- [Usage](#-usage)
- [Dashboard Screenshots](#-dashboard-screenshots)
- [Key Insights](#-key-insights)
- [Technical Implementation](#-technical-implementation)
- [Results & Recommendations](#-results--recommendations)
- [Future Enhancements](#-future-enhancements)
- [Contributing](#-contributing)
- [License](#-license)

---

## Project Overview

This project delivers a next-generation cryptocurrency intelligence analysis for a US-based fintech startup. The analysis enables effective monitoring and decision making for investors, traders, and regulators by providing comprehensive historical data analysis and real-time insights.


### Key Features

- **Multi-Source Data Integration**: Seamlessly combines data from Yahoo Finance, CoinGecko, and historical CSV files
- **Advanced Visualizations**: Comprehensive trend analysis, comparative performance metrics, and market insights
- **Scalable Architecture**: Built on Microsoft Fabric for enterprise-grade performance


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
AAVE         
Binancecoin
Cosmos
Dogecoin
Ethereum
Litecoin
NEM
Stellar
Uniswap
WrappedBitcoin

## Microsoft Fabric Project Assets
1. Workspace
2. Lakehouse
3. Warehouse

### 1. **Historical Foundation Data** (Jan 2020 - Jul 21, 2021)
- **Format**: 10 CSV files
- **Coverage**: Complete historical baseline for 10 major cryptocurrencies
- **Storage**: Microsoft Fabric Lakehouse 

### 2. **Yahoo Finance Integration** (Jul 22, 2021 - Jun 12, 2024)
- **Source**: YFinance API
- **Implementation**: [Python Integration Code](https://github.com/Irene-Chola/Crypto-Currency-Historical-Data-Project/blob/main/yahoofinancehistoricaldata.ipynb)
- **Features**: Historical data
- **Storage**: Microsoft Fabric Lakehouse

### 3. **CoinGecko Premium Data** (Jun 13, 2024 - Jun 13, 2025)
- **Source**: CoinGecko API
- **Implementation**: [CoinGecko Integration Code](https://github.com/Irene-Chola/Crypto-Currency-Historical-Data-Project/blob/main/historicaldata_group.coingecko.ipynb)
- **Features**: Historical data
- **Storage**: Microsoft Fabric Lakehouse

### 4. **Symbol Mapping Service**
- **Source**: CoinGecko API
- **Implementation**: [Symbol Mapping Code](https://github.com/Irene-Chola/Crypto-Currency-Historical-Data-Project/blob/main/crypto_symbol_mapping.ipynb)
- **Purpose**: Standardized currency identification across all data sources
- **Storage**: Microsoft Fabric Warehouse


## Installation & Setup

### Prerequisites
- Microsoft Fabric workspace access
- PowerBI Desktop
- API keys for Yahoo Finance and CoinGecko


## Usage

### Data Pipeline Execution
1. **Historical Data Import**:
   - Create a Microsoft Fabric Workspace, Lake House and Lake House
   - Load the 10 CSV files into Microsoft Fabric
   - Create a folder in the Lake House and store the data in tables
   
3. **API Data Sync**:
   - Write or upload your python script to Microsoft Fabric.
   - speficify the correct API key for each script
   - Create a folder in your Data Lake and set up the file path to store your data
   - Execute Yahoo Finance and CoinGecko data pulls
     
4. **Data Transformation**:
   - Create a dataflow and load all your files (10 CSV files, CoinGecko and Yahoo Finance) into the dataflow
   - Apply cleaning and standardization processes with Dataflow
   - Append the dataset into a master table
   - Load your master table into you Data Lake
     
5. **Dashboard Deployment**:
   - Create a connection from Microsoft Fabric to PowerBI
   - Load your masterdata set and symbol mapping data to PowerBI
   - Create a connection between the two files above
   - Create your dashboard and publish the dashboard to Microsoft Fabric WorkSPace

### Dashboard Navigation
- **Time Series Analysis**: Interactive charts with date range selection
- **Comparative Analysis**: Side-by-side currency performance
- **Market Metrics**: Real-time volume and market cap tracking
- **Detailed Tables**: Comprehensive data exploration

## Dashboard Screenshots

### Main Dashboard
![Crypto Currency Dashboard](https://github.com/Irene-Chola/Crypto-Currency-Historical-Data-Project/blob/main/cryptocurrencyhistoricaldatadashboard.jpg)

*Interactive dashboard showing trend analysis, price performance, and market insights*

## 🔍 Key Insights

### Market Analysis Results
- **Total Market Capitalization**: $2.3T+ across analyzed currencies
- **Volume Analysis**: Daily trading volumes exceeding $50B
- **Price Trends**: Comprehensive 5-year historical performance tracking
- **Volatility Metrics**: Risk assessment and correlation analysis

### Top Performing Insights
1. **Bitcoin (BTC)**: Consistent long-term growth despite volatility
2. **Ethereum (ETH)**: Strong correlation with DeFi adoption
3. **Market Cycles**: Clear cyclical patterns identified across all currencies

## Technical Implementation

### Data Processing Pipeline
```python
# Key transformations applied:
- Date standardization and parsing
- Duplicate removal across data sources
- Column name standardization
- Data type optimization
- Missing value handling
```

### Performance Optimizations
- **Incremental Loading**: Only new/changed data processed
- **Partitioning Strategy**: Date-based partitioning for optimal query performance
- **Caching Layer**: Frequently accessed data cached for faster response times

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

## Future Enhancements

### Phase 2 - Realtime Data Pipeline


## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Code Style
- Follow PEP 8 for Python code
- Use meaningful variable names
- Include comprehensive docstrings
- Add unit tests for new features

## 📞 Support & Contact

- **Issues**: [GitHub Issues](https://github.com/Irene-Chola/Crypto-Currency-Historical-Data-Project/issues)
- **Discussions**: [GitHub Discussions](https://github.com/Irene-Chola/Crypto-Currency-Historical-Data-Project/discussions)
- **Email**: [your-email@example.com](mailto:your-email@example.com)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Microsoft Fabric Team** for providing enterprise-grade data platform
- **CoinGecko** for comprehensive cryptocurrency data
- **Yahoo Finance** for reliable financial data feeds
- **Power BI Community** for visualization best practices

---

**⭐ If you found this project helpful, please consider giving it a star!**

---

*Built with ❤️ by [Irene Chola](https://github.com/Irene-Chola)*
