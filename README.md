# 📊 Maven Electronics Sales Performance Analysis

## Project Overview

This project analyzes historical sales performance for **Maven Electronics**, a multinational consumer electronics retailer, using **Microsoft Power BI**. The objective is to identify the factors contributing to declining revenue after 2020 while evaluating customer behavior, product performance, regional sales, and store operations.

The final solution combines data preparation, data modeling, DAX calculations, and interactive dashboards to provide executives with actionable insights that support strategic business decisions.

---

## Introduction

Maven Electronics is a multinational consumer electronics retailer offering products such as computers, mobile phones, televisions, cameras, home appliances, gaming devices, audio equipment, and digital media. The company operates through both physical retail stores and an online sales platform, serving customers across multiple countries and regions.

### Disclaimer

> **Note:** This project was completed for learning and portfolio purposes using a sample dataset provided by Maven Analytics. It does not represent the operations or performance of any real organization.

---

## Business Understanding

### Business Problem

Maven Electronics has consistently maintained healthy profit margins of approximately **58–60%**, yet management observed a significant decline in overall revenue beginning in **2020**. Without an integrated reporting system, it became difficult to determine whether the decline was driven by customer behavior, product performance, pricing strategies, store operations, or broader market trends.

The organization lacked a centralized analytics solution capable of bringing together sales, customer, product, and store data into a single source of truth. As a result, executives had limited visibility into the factors affecting business performance and were unable to make timely, data-driven decisions.



### Key Business Challenges

- Revenue declined significantly after 2020 despite maintaining strong profit margins.
- Management lacked visibility into the underlying drivers of declining revenue.
- It was unclear whether the decline resulted from customer churn, reduced customer acquisition, weaker product demand, or underperforming stores.
- Sales, customer, product, and store information existed in separate datasets without an integrated reporting solution.
- Decision-makers required an interactive dashboard capable of monitoring business performance and identifying growth opportunities.


### Business Questions

This analysis was designed to answer the following business questions:

- Why did revenue decline after 2020 despite stable profit margins?
- Which products, categories, brands, and regions generate the highest revenue?
- Has customer acquisition or customer retention changed over time?
- Which customer demographics contribute the most revenue?
- Do store characteristics such as size or age influence profitability?
- Is the decline in revenue seasonal or part of a long-term business trend?
- What strategic actions can management take to restore sustainable growth?



### Business Objectives

The primary objective of this project is to transform transactional sales data into meaningful business intelligence that supports data-driven decision-making across sales, customer management, product strategy, and store operations.

Specifically, this project aims to:

- Monitor overall business performance using key financial and operational KPIs.
- Identify the primary drivers behind the post-2020 decline in revenue.
- Evaluate the impact of pricing, profitability, and customer activity on business performance.
- Assess customer acquisition, retention, and purchasing behavior to understand changes in customer engagement.
- Evaluate product, category, brand, regional, and store performance to identify key revenue contributors.
- Determine whether store characteristics such as size and age influence profitability.
- Examine historical sales trends and seasonal patterns to distinguish temporary fluctuations from long-term structural changes.
- Provide actionable recommendations that support revenue recovery, customer growth, and long-term profitability.
By achieving these objectives, the project delivers a comprehensive analytical framework that enables management to monitor business performance, diagnose operational challenges, and make informed strategic decisions.

---

## Project Objectives

This project demonstrates the complete end-to-end **Business Intelligence workflow** using **Microsoft Power BI**, from raw data preparation to executive reporting and strategic recommendation development.


### Data Preparation

- Imported and consolidated multiple datasets into Power BI.
- Cleaned, validated, and transformed raw data using Power Query.
- Standardized data types and resolved data quality issues.
- Created additional analytical features, including:
  - Customer Age
  - Customer Tenure
  - Store Age
  - Store Size Categories



### Data Modeling

- Designed a scalable **Star Schema** consisting of one fact table and multiple dimension tables.
- Established one-to-many relationships to support efficient reporting.
- Developed a custom Date Dimension to enable accurate time intelligence analysis.

### Data Analysis

- Performed exploratory data analysis (EDA) to identify trends and anomalies.
- Evaluated sales performance across products, customers, stores, and geographic regions.
- Conducted customer acquisition and cohort retention analysis to understand customer lifecycle behavior.
- Investigated historical revenue trends to identify structural shifts in business performance.



### Dashboard Development

- Built interactive executive dashboards focused on sales, customers, products, and store performance.
- Created reusable DAX measures for financial and operational KPIs.
- Implemented field parameters, slicers, drill-downs, and interactive filtering to improve user experience.
- Presented key metrics through clear and executive-friendly visualizations.

### Business Intelligence

- Translated analytical findings into actionable business insights.
- Identified the key drivers behind declining business performance.
- Developed data-driven recommendations to improve customer acquisition, retention, and revenue growth.
- Delivered an executive reporting solution that supports informed decision-making across multiple business functions.

---

## Dataset Information

The analysis was conducted using the **Global Electronics Retail Dataset** provided by **Maven Analytics**, which simulates the operations of a multinational consumer electronics retailer. The dataset captures sales transactions, customer information, product details, store operations, and exchange rates over a five-year period, enabling comprehensive analysis of business performance across multiple dimensions.

The data was integrated into a relational model consisting of one fact table and multiple dimension tables, allowing for efficient analysis of sales performance, customer behavior, product profitability, and store operations.

| Attribute | Details |
|------------|---------|
| **Dataset Source** | Maven Analytics |
| **Industry** | Consumer Electronics Retail |
| **Time Period** | January 2016 – February 2021 |
| **File Format** | CSV |
| **Data Model** | Star Schema |
| **Fact Table** | Sales |
| **Dimension Tables** | Customers, Products, Stores, Exchange Rates, Date |
| **Primary Currency** | USD |

### Dataset Overview

The project integrates information from the following business entities:

| Table | Description |
|--------|-------------|
| **Sales** | Transactional sales records containing order details, quantities sold, customers, products, and stores. |
| **Customers** | Customer demographic and geographic information. |
| **Products** | Product attributes including brand, category, subcategory, cost, and selling price. |
| **Stores** | Store location, opening date, and physical store size. |
| **Exchange Rates** | Daily exchange rates used for currency normalization. |
| **Date** | Custom calendar table created to support time intelligence and trend analysis. |

---

## Data Dictionary

The following data dictionary summarizes the key fields used throughout the analysis. These fields served as the foundation for data modeling, KPI development, customer segmentation, and business reporting.

### Sales Table

| Field | Description |
|---------|------------|
| Order Number | Unique identifier for each customer order. |
| Line Item | Identifies individual products purchased within an order. |
| Order Date | Date the customer placed the order. |
| Delivery Date | Date the order was delivered to the customer. |
| CustomerKey | Foreign key linking each transaction to a customer. |
| StoreKey | Foreign key linking each transaction to a store. |
| ProductKey | Foreign key linking each transaction to a product. |
| Quantity | Number of units purchased. |
| Currency Code | Currency used for the transaction. |

### Customer Table

| Field | Description |
|---------|------------|
| CustomerKey | Unique customer identifier. |
| Name | Customer full name. |
| Gender | Customer gender. |
| Birthday | Customer date of birth. |
| City | Customer city. |
| State | Customer state or province. |
| Country | Customer country. |
| Continent | Customer continent. |
| Zip Code | Customer postal code. |

### Product Table

| Field | Description |
|---------|------------|
| ProductKey | Unique product identifier. |
| Product Name | Product description. |
| Brand | Product manufacturer. |
| Category | High-level product category. |
| Subcategory | Product subcategory. |
| Color | Product color. |
| Unit Cost USD | Cost of the product. |
| Unit Price USD | Selling price of the product. |

### Store Table

| Field | Description |
|---------|------------|
| StoreKey | Unique store identifier. |
| Country | Store country. |
| State | Store state or province. |
| Square Meters | Physical size of the store. |
| Open Date | Date the store began operations. |

### Exchange Rate Table

| Field | Description |
|---------|------------|
| Date | Exchange rate date. |
| Currency | Currency code. |
| Exchange | Exchange rate relative to USD. |

### Engineered Features

To support deeper business analysis, several calculated columns were created during the data preparation stage.

| Feature | Purpose |
|----------|---------|
| Customer Age | Calculate each customer's age for demographic analysis. |
| Age Group | Segment customers into standardized age categories. |
| First Purchase Date | Identify when each customer first purchased from the business. |
| Customer Tenure | Measure how long customers have remained active. |
| Customer Type | Classify customers as New or Returning. |
| Store Age | Calculate the operational age of each store. |
| Store Size Category | Classify stores into Small, Medium, Large, and Extra Large based on floor area. |
| Date Dimension | Support Year-over-Year, Month-over-Month, and other time-intelligence analyses. |

---
## Technology Stack

- Power BI
- Power Query
- DAX
--- 
## Skills Demonstrated

This project demonstrates the complete Business Intelligence workflow, from data preparation and modeling to interactive dashboard development and strategic business recommendations. Throughout the project, both technical and analytical skills were applied to transform raw transactional data into actionable business insights.

### Data Preparation & Transformation


### Data Modeling


### Data Analysis
- Exploratory Data Analysis (EDA)
- Trend Analysis
- Customer Segmentation
- Customer Cohort Analysis
- Customer Acquisition Analysis
- Customer Retention Analysis
- Product Performance Analysis
- Regional Performance Analysis
- Time-Series Analysis


### Power BI Development

- Interactive Dashboard Design
- DAX Measure Development
- Time Intelligence Functions
- Dynamic Field Parameters
- KPI Development
- Drill-through & Cross-filtering
- Slicer Implementation
- Performance Optimization

