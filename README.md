# Enterprise Data Analytics Platform

**Project Author:** Vedang Mishra

## Project Overview

AtliQ Hardware is a rapidly growing company operating across multiple markets and selling computers and computer accessories through Retail, Direct, and Distributor channels.

The company faced challenges in making data-driven decisions because business analysis was largely dependent on surveys, intuition, and Excel-based analysis. This project focuses on building an **Enterprise Data Analytics Platform using Power BI** to bring business data together and provide actionable insights across **Finance, Sales, Marketing, and Supply Chain**.

The main objective is to help stakeholders understand business performance, identify trends and problem areas, and answer important business questions using interactive dashboards.

[Live Report Link](https://app.powerbi.com/view?r=eyJrIjoiMTQwNWVlNmUtZWY5ZC00Mjc4LWJhMzMtZWZkMzA3OTM0YTY3IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9&pageName=ReportSection0e765c0061580b067c73)

## Tech Stack

- SQL
- MySQL
- Power BI Desktop
- Power Query / M Language
- DAX
- Excel
- DAX Studio
- Project Charter / Business Requirements

## Power BI Skills & Techniques

During this project, I worked on the complete analytics workflow, from understanding business requirements and data to building and publishing the final report.

- Understanding business requirements and identifying the right questions before analysis
- Creating calculated columns and DAX measures
- Building and maintaining a structured data model
- Creating a date table using Power Query / M Language
- Using DAX functions such as `DIVIDE` to handle zero-division scenarios
- Creating dynamic titles based on applied filters
- Implementing KPI indicators for quick performance tracking
- Applying conditional formatting using icons and background colors
- Using bookmarks to switch between different visual views
- Implementing page navigation using buttons
- Applying data validation techniques
- Optimizing reports using DAX Studio
- Publishing reports to Power BI Service
- Setting up a personal gateway for scheduled data refresh
- Creating and managing a Power BI App
- Working with workspaces, collaboration, and access permissions in Power BI Service

## Business Concepts Covered

The project also helped in understanding important business and financial metrics used in the organization:

- Gross Price
- Pre-Invoice Deductions
- Post-Invoice Deductions
- Net Invoice Sales
- Gross Margin
- Net Sales
- Net Profit
- COGS - Cost of Goods Sold
- YTD - Year to Date
- YTG - Year to Go
- Retailer
- Direct
- Distributor
- Consumer

## Company Background

AtliQ Hardware has expanded its business across multiple countries and sells computers and computer accessories through three primary channels:

- Retailers
- Direct
- Distributors

The company experienced a significant business loss after opening a store in America based mainly on surveys, intuition, and Excel-based analysis. At the same time, competitors were using dedicated analytics teams to support data-driven decision-making.

This created a need for a centralized analytics solution that could provide reliable insights and help business teams make better decisions based on actual data.

## Dataset Understanding

Before starting the analysis, it was important to understand the available data, the purpose of each table, and the relationships between them.

### Dimension Tables

Dimension tables contain descriptive and relatively static information such as customer, market, and product details.

### Fact Tables

Fact tables contain transactional information such as sales and forecast quantities.

### Database: `gdb041`

#### `dim_customer`

- 27 distinct markets, including India, USA, and Spain
- 75 distinct customers across the markets
- 2 platform types:
  - Brick & Mortar - Physical / Offline Store
  - E-commerce - Online Store
- 3 sales channels:
  - Retailer
  - Direct
  - Distributor

#### `dim_market`

- 27 distinct markets
- 7 sub-zones
- 4 regions:
  - APAC
  - EU
  - LATAM
  - Other / Unclassified

#### `dim_product`

Products are organized into multiple divisions and categories.

- **P & A**
  - Peripherals
  - Accessories
- **PC**
  - Notebook
  - Desktop
- **N & S**
  - Networking
  - Storage
- 14 product categories
- Multiple variants available for the same product

#### `fact_forecast_monthly`

This table contains monthly forecast quantities for customers. Forecasting helps the business plan inventory in advance, which can support:

- Better customer satisfaction
- Improved inventory planning
- Reduced warehouse storage costs

The table is denormalized for analytical use. Monthly dates are represented using the start date of each month, and the final measure contains the forecast quantity.

#### `fact_sales_monthly`

This table follows a structure similar to `fact_forecast_monthly`, but the final measure represents the actual quantity sold.

### Database: `gdb056`

#### `freight_cost`

Contains freight and related travel costs for each market and fiscal year.

#### `gross_price`

Contains gross pricing information by product code.

#### `manufacturing_cost`

Contains manufacturing costs by product code and year.

#### `Pre_invoice_deductions`

Contains pre-invoice deduction percentages for each customer and year.

#### `Post_invoice_deductions`

Contains post-invoice deductions and other deduction-related information.

## Importing Data into Power BI

The project data is stored in a MySQL database. The datasets were connected to Power BI by providing the required database credentials and importing the required tables for analysis.

## Data Model

Data modeling is a critical part of the project because all calculations and visualizations depend on the underlying model.

A well-structured data model improves:

- Report performance
- Calculation accuracy
- Data consistency
- Ease of analysis
- Maintainability of the report

For this project, a **Snowflake data modeling approach** was followed.

<img src="Resources/Data_model.png" class="center">

## Dashboard Design

The dashboard was designed based on the business requirements and mock-ups. Each section focuses on a specific business function and uses appropriate KPIs, measures, filters, and visualizations to make the analysis easy to understand.

The report provides multiple views so that stakeholders can quickly navigate to the area they are interested in.

## Home View

The Home page acts as the central navigation screen of the report. Users can move to different sections using navigation buttons.

Available sections include:

- Info
- Finance
- Sales
- Marketing
- Supply Chain
- Executive
- Products
- Support

## Overall Report

<img src="Resources/Home.png" class="center">

## Finance View

The Finance view focuses on financial performance and key metrics such as sales, margins, deductions, and profitability.

<img src="Resources/Finance View.png" class="center">

## Sales View

The Sales view helps analyze sales performance across different markets, customers, products, and channels.

<img src="Resources/Sales View.png" class="center">

## Marketing View

The Marketing view provides insights that help understand business performance from a market and customer perspective.

<img src="Resources/Marketing View.png" class="center">

## Supply Chain View

The Supply Chain view focuses on demand, forecast, and sales-related information to support inventory and supply chain decision-making.

<img src="Resources/Supply Chain View.png" class="center">

## Project Outcome

The final Power BI solution provides stakeholders with a centralized and interactive platform for exploring business performance.

The project demonstrates how raw business data can be transformed into meaningful insights using **SQL, Power BI, Power Query, DAX, data modeling, and dashboard design**.

The report enables stakeholders to:

- Monitor important business KPIs
- Analyze Finance, Sales, Marketing, and Supply Chain performance
- Identify trends and areas requiring attention
- Drill down into business performance using filters and interactive visuals
- Support data-driven decision-making
- Investigate the reasons behind changes in business performance

## Full Report

You can explore the complete Power BI report here:

[View Full Power BI Report](https://app.powerbi.com/view?r=eyJrIjoiMTQwNWVlNmUtZWY5ZC00Mjc4LWJhMzMtZWZkMzA3OTM0YTY3IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9&pageName=ReportSection0e765c0061580b067c73)
