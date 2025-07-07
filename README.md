# **Crypto Currency Analysis**
## An Analysis of the historical data of 10 Crypto Currencies
## **Table of Contents**
- [Project Overview](project-overview)
- [Project Objectives](project-objectives)
- [Key-Deliverables](key-deliverables)
- [Tools Used](tools-used)
- [Data Sources](data-sources)
- [Data Description](data-description)
- [Data Cleaning](data-cleaning)

---
## Project Overview
US-based fintech startup requires a next-generation cryptocurrency intelligence and reporting platform

---

## Project Objective
To create a next-generation crypto currency intelligence and reporting platform to enable effective monitoring by  investors, traders and regulators.

---

## Key Deliverables
- Ingest historical data from multiple sources
- Clean and transform data
- Visualize insights using PowerBi and Real-Time Dashboards

---

### Tools Used
- Microsoft Fabric
- PowerBI
  
---  

### Data Sources
Here are the 4 datasets ingested from various sources. Each of this datasets was stored in a seperate folder in the Lake House.

  **1. Data from January 2020 - 21-07-2021** 
  
10 CSV files were provided containing historical data for the 10 crytpo currencies. 
  
Here is the complete dataset provided in the CSV Files - [ten_crypto_currencies]()  

  
  **2. Data from 22-07-2021 - 12-06-2024 - Yahoo Finance Data**

An API Key was used to ingest data from YFinance for the specified dates. 
   
The following python code was used to ingest this data - [YFinance Data Python Code](https://github.com/Irene-Chola/Crypto-Currency-Historical-Data-Project/blob/main/yahoofinancehistoricaldata.ipynb)
  
  **3. Data from 13-06-2024 - 13-06-2025 - CoinGecko Data** 

An API key was used to ingest data from CoinGecko for the specified dates. 
   
The following python code was used to ingest this data from CoinGecko - [CoinGecko Python Code](https://github.com/Irene-Chola/Crypto-Currency-Historical-Data-Project/blob/main/historicaldata_group.coingecko.ipynb)
  
  **4. Symbol mapping data - CoinGecko** 
  
The following python code was used to perform symbol mapping from CoinGecko - [Symbol Mapping Python Code](https://github.com/Irene-Chola/Crypto-Currency-Historical-Data-Project/blob/main/crypto_symbol_mapping.ipynb)

  ---

### Data Description
Historical data was ingested from various sources a specified above. The goal of this exercise is to have a complete set of date from January 2020 - 13-06-2025 (The time this project was conducted). 

**Crypyo Currencies data contained:** 

Crypto symbol, Date, (High, Low, Open, Close) refers to the crypto price, Volume and Marketcap

**Symbol Mapping data contained:** 

Actual names of each crypto currency mapped using the crypto symbols.

---

### Data Cleaning 
- Microsoft Fabric Data Lake - Data ingested and loaded to Microsoft Fabric Data Lake
- Dataflows - Used to transform the data and join it into one master dataset
    Key Transformations:
    - Filtered data from 2020 onwards
    - Date parsing and type conversions
    - Appending CoinGecko data without duplicates
    - Appending YFinance data without duplicates
    - Standardizing column names across sources
      
---

### EDA(Exploratory Data Analysis)
- What is the total market capitalization?
- What is the total market Volume?
- What is the trend of each currency over time?
- What is the price of each Crypto Currency?
  
---
### Data Analysis
This historical data dashboard is created in PowerBI.
Key Insights Shared:
Trend analysis for each crypto coin
Comparative price performance
Volume and market capitalization analysis
Detailed data table with metrics
Interactive filters by year and coin

---
### Power BI Dashboard
Here is a link to the PowerBI dashboard:

[Crypto Currency Historical Data Dashboard](https://github.com/Irene-Chola/Crypto-Currency-Historical-Data-Project/blob/main/cryptocurrencyhistoricaldatadashboard.jpg)

---
### Results

----

### Recommendations
----
### Limitations

### References 
