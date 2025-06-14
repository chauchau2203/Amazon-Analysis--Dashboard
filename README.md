# Amazon E-Commerece India Data Analysis

## A. Description
This project analyzes the sales performance of Amazon India's clothing segment between 2021 and 2022 by leveraging data from three key sources: Customer Sales, B2B Sales, and Inventory Level. 

### Objectives

* To evaluate **sales patterns** across different customer segments and business channels (B2C and B2B).

* To analyze **inventory distribution** and optimize stock levels based on demand and product attributes such as category, size, and color.

* To identify **top-performing** products, regions, and customer groups to inform marketing and operational strategies.

* To understand **temporal sales trends**, including seasonality and weekday effects, to improve forecasting and planning.

* To provide **recommendations** for inventory management, customer retention, and revenue growth based on comprehensive data analysis.

## B. Data Sources

### URL
The Amazon dataset is from Kaggle: **<a href="https://www.kaggle.com/datasets/thedevastator/unlock-profits-with-e-commerce-sales-data">View Dataset</a>**

### Dataset description
The dataset provides a comprehensive overview of e-commerce clothing sales data on Amazon India between 2021 and 2022 covering a variety of products. The original dataset contains 7 tables:
- File ***Amazon Sale Report.csv***: Records of clothing sales transactions in India through the Amazon platform from April 2022 to June 2022.

- File ***Cloud Warehouse Comparison Chart.csv***: Records of profits between two fulfillment methods: Shiprocket and INCREFF.

- File ***Expense IIGF.csv***: Records of financial information on expenses (received amount vs. expenses).

- File ***International sale Report.csv***: Records of clothing sale transactions to other companies (from June 2021 to May 2022).

- File ***May-2022.csv***: List of clothing products and their prices on different online platforms (including Ajio, Amazon, Flipkart, Limeroad, Myntra, Paytm, Snapdeal).

- File ***P & L March 2021.csv***: List of clothing products and their prices on different online platforms (including Ajio, Amazon, Flipkart, Limeroad, Myntra, Paytm, Snapdeal).

- File ***Sale Report.csv***: List of clothing products (including the SKU, Category, Stock level, Size, Color).

## C. Installation/Setup

### Prerequisites
- **Python 3.10.16** or higher. Download [here](https://www.python.org/).
    - Install **statsmodels** package:
    - Install **Jupyter** package.
```
pip install jupyter
pip install statsmodels
```

- **Visual Studio Code (VS Code)**. Download [here](https://code.visualstudio.com/).

- **VS Code Extensions**:
    - Python extension by Microsoft.
    - Jupyter extension by Microsoft.


- (Optional but recommended) Use a **virtual environment or Anaconda environment** to manage dependencies and avoid conflicts.

- **Power BI** version used is 2.131.1203.0 32-bit (July 2024) or higher. Download [here](https://www.microsoft.com/en-us/power-platform/products/power-bi/downloads).

### Environment Setup
- Open VSCode

- Select Python 3.10.16 interpreter using the Command Palette (Ctrl+Shift+P) → Python: Select Interpreter.

- Python libraries imported:
    - **pandas** - for Data Manipulation
    - **numpy** - for Numerical Computation
    - **matplotlib.pylot** - for Data Visualisation
    - **adfuller** - for ADF Test (ARIMA Modelling)
    - **plot_acf, plot_pacf** - for Plotting ACF, PACF plots

## D. Project Structure

### 1. Data Preparation
- **<a href="https://github.com/chauchau2203/Amazon-Analysis--Dashboard/blob/main/Amazon%20Preparing%20Data.ipynb">Amazon Preparing Data.ipynb</a>**: Contains data cleaning, transformation, and preprocessing steps for the raw datasets (all 7 files).

### 2. Exploratory Data Analysis (EDA)
- **<a href="https://github.com/chauchau2203/Amazon-Analysis--Dashboard/blob/main/Amazon%20EDA.ipynb">Amazon EDA.ipynb</a>**: Performs exploratory data analysis (EDA) to uncover key patterns, trends, and insights in sales and inventory data. Includes visualizations, summary statistics, and initial findings that guide further analysis. 

- After performing EDA, only 3 files were kept for further analysis and visualisation: ***[amazon_sales.csv](https://github.com/chauchau2203/Amazon-Analysis--Dashboard/blob/main/amazon_sales.zip) (Customer Sales table)***, ***[international_sales.csv](https://github.com/chauchau2203/Amazon-Analysis--Dashboard/blob/main/international_sales.zip) (B2B Sales table)***, ***[inventory_level.csv](https://github.com/chauchau2203/Amazon-Analysis--Dashboard/blob/main/inventory_level.zip) (Inventory Level table)***. The remaining files provide some data including expenses, profits from two fulfillment methods, and cross-platform pricing but each only has a few rows, thus uneccessary.

### 3. Revenue Forecast
- **<a href="https://github.com/chauchau2203/Amazon-Analysis--Dashboard/blob/main/Amazon%20Forecasting%20Revenue.ipynb">Amazon Forecasting Revenue.ipynb</a>**: Contains the revenue forecasting models and time series analysis ARIMA. This notebook predicts future sales based on historical data and seasonal trends.

### 4. Dashboard for visualisation
- **<a href="https://github.com/chauchau2203/Amazon-Analysis--Dashboard/blob/main/Amazon%20Dashboard.pbix">Amazon Dashboard.pbix</a>**: Develops interactive visualizations and dashboards to present insights dynamically. This dashboard integrates key metrics and charts for stakeholder reporting and decision-making.
    - **Customer Sales Dashboard**:
![3cacd3a1-506c-4aff-b21d-d60ef6fd7b3e](https://github.com/user-attachments/assets/a7e1be7d-cea9-48cd-a242-0a08ae418251)
    - **B2B Sales Dashboard**:
![af431184-8d95-41d4-af4b-2b8475f68a0e](https://github.com/user-attachments/assets/47060d11-8657-4e38-a623-564bd6f8630b)
    - **Inventory Level Dashboard**:
 ![fa7d38d6-c496-4da1-8adb-e65c7441badd](https://github.com/user-attachments/assets/5c33f26f-ffbf-48d4-9aaf-fcaa467d587a)
 
### 5. Sales Report
- **[Amazon Sales Report.pdf](https://github.com/chauchau2203/Amazon-Analysis--Dashboard/blob/main/Amazon%20Sales%20Report-compressed.pdf)**: A comprehensive report summarizing the key findings, insights, and recommendations derived from the data analysis and dashboard.

## E. Methodology

The project follows a structured, end-to-end data analytics workflow to derive actionable insights from Amazon India’s clothing sales data across Customer Sales, B2B Sales, and Inventory Level datasets.

### 1. Data Collection and Preparation 
   Raw datasets were imported and consolidated using Python (pandas). Data cleaning included handling missing values, correcting erroneous entries, converting currencies, standardizing formats (e.g., dates, categories), and removing duplicates to ensure data quality and consistency.

### 2. Exploratory Data Analysis (EDA)
   Comprehensive EDA was performed to uncover sales patterns, customer behavior, and inventory distribution. Key statistical summaries and visualizations were generated to identify seasonality, regional performance, and product preferences.

### 3. Revenue Forecasting 
   Time series forecasting model ARIMA (autoregressive integrated moving average) was developed using historical sales data to predict future revenue trends. Techniques included moving averages and seasonality adjustments, enabling better inventory and sales planning aligned with demand cycles.

### 4. Dashboard Development
   Cleaned data and key metrics were imported into Power BI to build an interactive dashboard. Dynamic slicers and DAX measures were implemented to allow stakeholders to explore sales by time, region, product category, and customer segment.

### 5. Insights and Recommendations
   Analytical findings were synthesized into a comprehensive report highlighting sales drivers, inventory optimization opportunities, and customer retention strategies. Recommendations were tailored to support data-driven decision-making for business growth.

## F. Analysis & Results: Key Findings and Visuals

### Customer Sales

- **Sales Trends & Seasonality:**  
  - **April 2022** recorded the **highest sales**, driven by major Indian festivals and post-pandemic demand recovery.
  - A consistent **decline in both order volume and revenue** was observed in **May and June**, correlating with reduced festive activity and rising inflation.

- **Regional Performance:**  
  - **Maharashtra and Karnataka** led in total revenue, reflecting their economic strength and higher e-commerce adoption.
  - **ignificant revenue concentration** in **western and southern states**, with underrepresentation in eastern and central regions.

- **Customer Behavior:**  
  - **Peak order and revenue** activity occurred on **weekends**, especially Sundays.
  - Average order value remained stable, indicating consistent purchasing patterns.

### B2B Sales

- **Customer Segmentation:**  
  - Revenue is **highly concentrated among a few key business customers**, with the top 5 accounting for a significant share.
  - The majority of customers are small or mid-sized businesses, each contributing modest revenue but representing future growth potential.

- **Sales Cycles & Seasonality:**  
  - Notable **revenue peaks in October 2021** (festival season) and **March 2022** (spring/summer collection launches).
  - **Sharp drop in May 2022** is attributed to only partial data for the month.

- **Order Patterns:**  
  - **Thursday** is the **highest revenue weekday** for B2B sales, while **Sunday** activity is **minimal**, reflecting standard business procurement cycles.


### Inventory Level

- **Category Distribution:**  
  - Inventory is heavily **concentrated in ethnic wear**, with Kurtas and Kurta Sets comprising over 70% of total stock.
  - **Bottom wear and western categories** are **underrepresente***, suggesting potential missed opportunities.

- **Color and Size Distribution:**  
  - Core colors (Black, Blue, Pink) and standard sizes (S, M, L, XL, XXL) dominate inventory allocation.
  - Extended sizes (3XL–6XL) and specialty colors have minimal stock, indicating limited focus on plus-size and niche segments.

- **Inventory Optimization Opportunities:**  
  - **Imbalances between sales trends and stock levels** highlight areas for rebalancing, particularly increasing investment in fast-moving sizes and colors, and reducing overstock in slow-moving categories.


**For visual references, see the included Power BI dashboard and the Amazon Sales Report PDF.**

## G. Recommendations

### Inventory Optimisation
- **Reduce Overstock in Ethnic Wear**: Kurtas (48% of stock) and Kurta Sets (21%) are overrepresented. Rebalance inventory to allocate 15–20% of stock to bottoms (pants, leggings) and western categories (dresses, jumpsuits) to meet growing urban demand.
  
- **Introduce Plus-Size Collections**: Expand 4XL–6XL stock from <3% to 10–15% of inventory. Partner with influencers/designers to tap into India’s underserved $10B plus-size apparel market.
  
- **Liquidate Low-Demand Colors**: Clear stagnant stock in niche colors (Coral Pink, Aqua Green) via flash sales. Redirect capital to high-demand colors: Black (22K units sold), Blue (19K), and Pink (21K).

### Demand Forecasting and Procurement
- **Align Procurement with Festive Peaks**: Pre-stock ethnic wear 8–10 weeks before Diwali (Oct–Nov) and Holi (March) to avoid stockouts, leveraging Amazon’s FBA demand forecasting tools.
  
- **Mitigate May–June Slump**: Launch monsoon-themed promotions (raincoats, quick-dry fabrics) and bundle ethnic wear with accessories to offset seasonal dips.

### Data-driven Pricing
- **Dynamic Pricing for Peak Months**: Increase margins by 10–15% on ethnic wear during festivals (Oct/Nov, March) using AI tools like Revionics.
  
- **Discount Aging Stock Automatically**: Set rules to auto-apply 20% discounts on items unsold for 60+ days (e.g., Shararas, Lehenga Cholis).

### Operational Efficiency
- **Adopt ABC Analysis**:
A (20% SKUs, 70% revenue): Kurta sets, M/L/XL sizes (restock weekly).
B (30% SKUs, 20% revenue): Dresses, S/XXL sizes (restock biweekly).
C (50% SKUs, 10% revenue): Niche colors/sizes (JIT restocking).

- **Implement Real-Time Tracking**: Use Amazon’s IPI dashboard + third-party tools (Unicommerce) to sync inventory across channels and avoid stockouts/overstock penalties.
- **Target High-Potential Regions**: Allocate 25% of marketing budget to underpenetrated eastern states (West Bengal, Odisha) where e-commerce adoption is rising but revenue contribution is low (<$53K).

## H. Future Work: Extensions and Improvements

- **Expand Data Coverage:** The current analysis is limited by the short duration of the Customer Sales data (only 3 months) and the relatively small volume of B2B sales data. Extending the data timeline and increasing the sample size would improve the robustness and reliability of insights.

- **Incorporate Additional Datasets:** Other available datasets such as expenses and fulfillment profitability were not included due to insufficient data rows. Future work should integrate these datasets once more comprehensive data is available to provide a holistic view of business performance.

- **Enhance Data Granularity:** Collecting more granular data, such as daily sales for B2B or detailed customer demographics, would enable deeper segmentation and more precise forecasting.

- **Improve Forecasting Models:** Current forecasting could be enhanced by incorporating advanced machine learning techniques and external factors like market trends, economic indicators, and competitor analysis.

- **Expand Customer Segmentation:** Utilize more sophisticated segmentation methods, including behavioral and psychographic data, to better tailor marketing and retention strategies.

- **Broaden Geographic Analysis:** Include more detailed regional and city-level analysis to identify micro-market opportunities and optimize logistics.

- **Evaluate Impact of Marketing Campaigns:** Incorporate marketing spend and campaign data to assess their effectiveness on sales and customer acquisition.


**Important:**  
- The dataset used in this project is sourced from Kaggle and is subject to its own licensing terms. Please refer to the [original dataset page](https://www.kaggle.com/datasets/thedevastator/unlock-profits-with-e-commerce-sales-data) for specific usage rights and restrictions.  

- This project is intended for educational and research purposes only. Commercial use of the dataset or derived insights should comply with the dataset provider’s terms and applicable laws.



