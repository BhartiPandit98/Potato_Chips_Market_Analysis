# Potato Chips Market Analysis: Project Overview
- Created a tool to help the sellers better understand the types of customers who purchase Chips and their purchasing behaviour.
- Scaped over 2 lakhs customer behaviour and transaction data from the forage
- Engineered features from each product name to get the packet size, brands and taste associated
- Used KMeans for better segmentation of the chips and drivers of their sales.

# Code and Resources Used
- Python Version: 3.7
- Packages: pandas, numpy, sklearn, matplotlib, plotly
- Scraper Data:
    - https://github.com/BhartiPandit98/Potato_chips_market_analysis/blob/main/QVI_transaction_data.xlsx
    - https://github.com/BhartiPandit98/Potato_chips_market_analysis/blob/main/QVI_purchase_behaviour.csv
    
# Dataset Description
Purchase Behaviour data:
  - Loyalty Card Number
  - Lifestage
  - Premium Customer
  
Transaction data:
  - Date
  - Store Number
  - Loyalty Card Number
  - Transaction Id
  - Product Number
  - Product Name
  - Product Quantity
  - Total sales
  
# Data Cleaning
After scraping the data, I needed to clean it up so that it was usable for our model. I made the following changes and created the following variables:
- Combined the datasets
- Parsed packet size out of the product name
- Parsed Brand name out of the product name
- Made columns for if different flavours were present in the product name:
    - Salt
    - Cream
    - Cheese
- Removed the outliers

# EDA
I looked at the distributions of the data and the value counts for the various categorical variables. Below are a few highlights from the pivot tables.

![alt](https://github.com/BhartiPandit98/Potato_chips_market_analysis/blob/main/Packet%20size%20distribution.JPG)

![alt](https://github.com/BhartiPandit98/Potato_chips_market_analysis/blob/main/Correlation.JPG)

![alt](https://github.com/BhartiPandit98/Potato_chips_market_analysis/blob/main/Brand%20distribution.JPG)

# Model Building
First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 20%.

I applied KMeans Clustering and plotted graph using plotly to visualize the characteristics of the clusters. The model gave diverse clusters and showed the characteristics of different clusters.
