# Walmart Business Analysis


<img width="768" height="185" alt="Walmart_logo svg" src="https://github.com/user-attachments/assets/a9010160-33e4-4263-a3f5-ff818a93e091" />


# About 

This project analyzes Walmart’s historical sales data across multiple U.S. stores from year 2010 to 2012 to identify the sales trends and few high-performing stroes. Besides that another objective of this project is to uncover business insights from total weekly sales figures, CPI rate, fuel prices, unemployment, and holidays to help understand patterns and trends that impact performance.


# Dataset Overview

The dataset consists of two main tables:

1. Walmart sales
                               
- Store_ID     :             Unique ID for each store 
- Date         :		         Date of the recorded weekly sales
- Weekly_Sales :             Weekly sales figures in USD 
- Holiday_Flag :             1 if the week includes a holiday,verse versa   
- Temperature  :             Recorded temperature on that date    
- Fuel_Price   :             Fuel price in USD
- CPI          :             Consumer Price Index 
- Unemployment :             Unemployment rate

                  
2. Date  
Enriched calendar table used for better time-based reporting.

- Date         :            Full date (converted)  
- Year         :            Extracted year  
- Month_Name   :            Full month name  
- Month_Number :            Numerical month  
- Year_Month   :            Concatenated year+month


# **Data Source:**  
> This dataset was obtained from Kaggle: [Walmart Store Sales Forecasting](https://www.kaggle.com/datasets/yasserh/walmart-dataset)  
> Credit to the original contributor.

## Approach Used

**Data Wrangling**
- Checked for missing or NULL values
- Trim whitespace using excel (as not a big data)

**Feature Engineering**
New table were created to help extract more insights in Power Bi Desktop with DAX:
- `Date`: Full date
- `month_name`: Extract month name from date
- `month_number`: Extract month number from date
- `year` : Extract year from date
- `year_month` : Extract year_month from date

**Exploratory Data Analysis (EDA)**
Performed EDA to answer project questions, support visualizations, and summarize key trends.


# Business Questions Answered

1.**Monthly Sales Trend by Year**

*What is the monthly sales trend by year?*

- MySQL: [Total Sales by Months and Years.sql] 
- Power BI: Line chart to visualize seasonal patterns
- Insight: Trend analysis. Significant drop in sales on 2012. YOY pecentage drop about 18.23% between 2012 to 2011.


2.**Top 5 Stores by Sales Performance**

  *Which stores performed best over 3 years?*

- MySQL : [Top 5 Stores by Sales Over 3 Years.sql]  
- Power BI : Bar Chart with breakdown by year and store id
- Insight:Correlation analysis. The sales of the top 5 stores has seen a slight drop on year 2012, Strong negative correlation (r ≈ -0.7), indicating sales decrease as inflation rises.



3.**Average CPI & Unemployment by Year**
  
  *Is there any correlation between CPI rate and unemployment rate?*

- MySQL:[ Avg CPI Rate and Avg Unemployment Rate by Year.sql] 
- Power BI:  Combo Chart for macroeconomic overview
-  Insight: Hypotheses and Correlation analysis. The combo chart shows The higher the average unemployemnt rate the lower the average cpi rate. Vice versa.



 4. **Fuel Price vs Holiday on Sales Performance**

   *Do holidays and fuel prices influence sales performance?*

- MySQL: [Avg Weekly Sales and Avg Fuel Price by Holiday Flag.sql]
- Power BI: scattered plot chart to visualize sales performance over the two variables
- Insight :  Regression analysis.The higher the average fuel price the higher the sales performance on holiday weeks compare to non holiday week.

#  Power BI Dashboard
<img width="626" height="540" alt="Walmart analysis dashboard power bi service" src="https://github.com/user-attachments/assets/81515d9d-1dc9-407e-81aa-3164a347dc0a" />

The dashboard provides:
- Total Sales Over The Years(Card),Avg Sales Per Week (Card),Avg CPI Rate Over The Years(Card),Avg Fuel Price Over The Years (Card)
- Monthly sales trend by year
- Top 5 performing stores
- Average CPI & Unemployment Rate by Year
- Sales performance by fuel price and holiday week



# Tools Used

- **Power BI** – Interactive data visualization and dashboard design  
- **MySQL** – Data manupulation and analysis  
- **Excel** – Data preparation and formatting  


# License

[![License: CC0 1.0 Universal](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

This project is dedicated to the public domain under the [Creative Commons CC0 1.0 Universal License](https://creativecommons.org/publicdomain/zero/1.0/).  
You can copy, modify, and distribute this work without any restrictions.



# Contact

For questions or collaboration, feel free to connect:  
**[Feliz-7]
**GitHub: [@Feliz-7](https://github.com/Feliz-7)
