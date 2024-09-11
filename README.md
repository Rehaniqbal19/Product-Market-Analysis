# Product Market Analysis Report



### Dashboard Link : 
https://app.powerbi.com/groups/me/reports/71d234f3-8dec-4663-8ab5-0322483d8099/ReportSection?experience=power-bi


## Overview

This dashboard is a comprehensive business intelligence tool designed to provide actionable insights into various aspects of the company's performance. It consolidates and visualizes data from multiple sources, allowing stakeholders to make data-driven decisions across different operational areas, including sales, profitability, customer orders, and product returns.


## Key Features / Pages of the Dashboard


### Executive Dashboard: 
A high-level overview of crucial metrics such as total revenue, profit, number of orders, and return rates. It provides a snapshot of the company's performance and tracks progress over time.

![image](https://github.com/user-attachments/assets/c4a7fea1-3fe7-4af4-933d-ddc7ce2fe437)



### Map view: 
It provides the management holistic view of Total Orders in different parts of the world.

![image](https://github.com/user-attachments/assets/eed24539-be60-463e-97e5-0f289afc8562)



### Product Details: 
From the Exec Dashboard page through drill-down feature, this view provide different analysis for any selected product.

![image](https://github.com/user-attachments/assets/1dcdc628-c2ec-4b96-b5e7-6d9072d831f1)



### Customer Details: 
It provides holistic view of Customers' demographics alongwith the number of orders and revenue associated with them.

![image](https://github.com/user-attachments/assets/47ad7e85-2281-4493-92ee-b1a3e58ed722)





### Data Loading, Cleaning and Setup Process

- Load data into Power BI Desktop, dataset is a csv file including Calendar Lookup, Customer Lookup, Product Lookup, Product Category Lookup, Product Subcategory Lookup, Returns Data, Sales Data 2020-22, Territory Lookup.
- Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Transformed and cleaned the tables as follows:
- - Calendar Lookup: From a single Date column, generated number of columns for Day Name, Week, Month, Quarter, Year
  -  Customer Lookup: Information related to Customers'demographics. Cleaned and standardized the data as required.
  -  Product Lookup: Different Products data that the company sells to generate revenue.
  -  Product Category Lookup: This outlines different category of the product the company sells.
  -  Product Subcategory Lookup: This outlines different subcategory of the product the company sells.
  -  Returns Data: Data for Return Product including Date and Product Key.
  -  Territory Lookup: Continents, Country and Region data.
    

- After transforming and cleaning data, in Model view, linked the tables with each other in Star Topology using Primary-Foreign Keys with 1-to-many or many-to-many cardinalities. Sales Data and Returns Data Tables are Dimensions tables and rest are fact tables.

  ![image](https://github.com/user-attachments/assets/232fe13a-471e-403d-988c-2aa4663ccab8)


- In Table view, add some columns using DAX for ease of data retrieval before moving to Report View.

![image](https://github.com/user-attachments/assets/ac5541e0-1569-49c4-ad19-4765809d53dc)



### Report View Setup

- In measure table, number of New DAX measure created including but not limited to Total Order, Total Revenue, Total Profit, Return Rate, Moving Averages etc.

![image](https://github.com/user-attachments/assets/eda944d6-8220-4edd-b82c-2184721b364b)
![image](https://github.com/user-attachments/assets/5393eaac-75b2-437a-b553-b771f757f543)


## Exec Dashboard Page Main Visuals

- In the top right, using new Card Visual, added Total Revenue, Profit, Orders and Return Rate %.
- Left pane includes Reset button (to clear all filters using Bookmark), filter, and page navigators.
- A line chart to display revenue across time (Months).
- A bar chat to display orders by category.
- Matrix table to display top 10 products. It can be used to drill-through to get details of the specific product.
- At the bottom, single cards to display stats.
- Moreover, all the visuals get update when a filter is being selected in bar plot, revenue trend, and top 10 products table. 

![image](https://github.com/user-attachments/assets/84e01a87-5eed-482f-a558-a2910e66ed02)



## Product Detail Page Main Visuals

- It displays stats for a single product. The selected product name verified from the left top name card.
- The top row displays Monthly orders, revenue, profit of profit vs its target using Gauge visual. Numerical values will turn red if values are less than the target.
- Using Product Metric Selection, line chart at bottom gets updated and display Order, profit, Revenue or returns values.
- Reports summary is being displayed as well as per the values.

![image](https://github.com/user-attachments/assets/98e1ba8e-0702-40de-81cc-3fc684174611)



## Customer Detail Page Main Visuals

- It displays unique customer and revenue per customer count in a Card visual.
- Total Customers or Revenue per Customer line chart selection is being displayed over time.
- Donut charts for Income brackets, and by top 3 occupation is being displayed.
- Top 100 Customers Matrix table is being displayed.

- From this, we can identify different patterns.
- - For example, from management occupation having income in high bracket (More than 100K and less than 150K), we can see 1126 unique customers, and Jordan Turner drove most revenue

    ![image](https://github.com/user-attachments/assets/6589f64a-eb68-461a-8308-184b1e262fa5)
