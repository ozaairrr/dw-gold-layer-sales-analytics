# Sales and Customer Analytics Project (EDA + Data Analysis)

## Overview
This project performs comprehensive Exploratory Data Analysis (EDA) and advanced Data Analysis (DA) on retail sales, customer, and product data. The analysis leverages **gold layer views** created in a separate data warehouse project, which serve as clean, business-friendly datasets derived from raw data.

The goal is to extract valuable business insights such as sales trends, customer segmentation, product performance, and cumulative analytics to support data-driven decision-making.

## Project Structure
### 📊 Exploratory Data Analysis (EDA)
Initial data profiling and discovery queries that explore:
- **Dataset Characteristics:** First/last order dates, customer age ranges, total business metrics
- **Geographic Distribution:** Customer locations and sales by country
- **Product Catalog Analysis:** Categories, subcategories, and product variety
- **Business Scale Metrics:** Total sales, customers, orders, and product counts
- **Ranking & Performance:** Top/bottom performing products and customers

### 📈 Data Analysis (DA) 
Advanced analytical queries focusing on:
- **Time Series Analysis:** Monthly/yearly trends with running totals and averages
- **Customer Segmentation:** VIP, Regular, and New customer classification based on spending and loyalty
- **Product Performance Analytics:** Year-over-year comparisons and performance benchmarking
- **Revenue Attribution:** Category contribution analysis and product cost segmentation
- **KPI Reporting:** Comprehensive customer and product report views with key metrics
```
Data Warehouse (Separate Repo) → Gold Layer Views → This Analytics Project
     ↓                              ↓                    ↓
Bronze/Silver Layers          Curated Business Views   EDA + Advanced Analysis
```

## Key Features
- Analyze sales trends over months and years with running totals and averages
- Segment customers by spending behavior and loyalty (VIP, Regular, New)
- Track product performance compared to average sales and previous years
- Compute category contributions to overall sales revenue
- Generate detailed customer and product KPI reports as SQL views
- Utilize window functions such as RANK(), LAG(), ROW_NUMBER(), and AVG() OVER()
- Comprehensive use of SQL Common Table Expressions (CTEs) for cleaner queries

```
## Business Metrics & KPIs

| Metric Category       | Key Metrics                                               |
|----------------------|-----------------------------------------------------------|
| **Sales Analytics**    | Monthly sales trends, cumulative revenue, average order value |
| **Customer Insights**  | Customer segments (VIP/Regular/New), lifetime value, recency    |
| **Product Performance**| Category contributions, year-over-year growth, cost analysis |
| **Operational KPIs**   | Order patterns, quantity trends, price analysis          |
```  

## Dependencies
- This project expects a data warehouse with the **gold layer views** available, specifically:
  - `gold_dim_customers`
  - `gold_dim_products`
  - `gold_fact_sales`

These are sourced from the data warehouse project repository: [Data Warehouse Project Repo](https://github.com/ozaairrr/sql-datawarehouse-project/tree/main)

- MySQL (or compatible SQL engine) capable of running advanced SQL features (window functions, CTEs)

## Usage
1. Clone this repository.
2. Connect to your database where the gold layer views are present.
3. Run the SQL scripts in the following sequence:
   - EDA queries folder: for initial data discovery and profiling.
   - Data Analysis queries folder: for business insights and report generation.
4. Use the queries or views for dashboarding, reporting, or further analysis.

## Business Impact
- Helps marketing teams identify high-value customers and tailor loyalty programs.
- Assists product managers in spotting rising or declining products and prioritizing inventory.
- Enables finance to track sales momentum and forecast revenue.
- Provides stakeholders with actionable segmentation and performance reports.

## Future Enhancements
- Integration with visualization tools such as Tableau or Power BI for dynamic reporting.
- Automation of query execution and results delivery via ETL orchestration tools.
- Expansion into customer cohort analysis and churn prediction.
- Improved documentation and parameterization for different environments.

## Contact
For questions or collaboration, contact Ozair at: [Your Email or LinkedIn]

