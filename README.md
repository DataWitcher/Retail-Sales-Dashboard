# Global Electronics Sales Dashboard (Excel)

## Overview
This project presents an interactive Excel-based Business Intelligence dashboard
analyzing global electronics sales from 2016 to 2021.

## Key KPIs
- Total Revenue
- Total Units Sold
- Number of Orders
- Average Order Value (AOV)

## Dashboard Features
- Monthly revenue trend analysis
- Revenue by country, category, and region
- Interactive slicers for time, geography, and brand
- Executive-style KPI cards

## Tools Used
- Microsoft Excel
- Pivot Tables
- Excel Data Model
- Slicers & Dashboard Design

## Files
- **Dashboard.pdf** – Executive dashboard view
- **Dashboard.xlsx** – Full Excel model with pivots and data

## Notes
Delivery performance analysis is planned as a future enhancement
pending standardized date handling via Power Query.

## Data Cleaning & Assumptions

### Dataset Overview
- Transactional data for a fictitious global electronics retailer
- ~62,844 records, 37 fields
- Source files: Customers, Products, Sales, Stores, Data Dictionary, Exchange Rates

### Data Quality Handling
- Some customer records contained missing ZIP codes, primarily for the United Kingdom.
  ZIP code was treated as an optional geographic attribute and excluded from KPI calculations.
- State code values were missing or inconsistent in certain records.
  These were standardized or categorized as 'Unknown' where necessary for reporting.
- Sales records with missing Order Dates were excluded from time-based analysis
  to ensure accurate monthly and yearly trends.
- Sales records with missing Delivery Dates were retained, as delivery information
  does not invalidate revenue recognition.

### Store & Channel Assumptions
- `StoreKey = 0` represents the online sales channel.
- Since online stores do not have a physical footprint, location and square meter
  attributes were treated as not applicable and retained as blank.
- Online and physical store performance were analyzed separately where relevant.

### Date & Currency Standardization
- Date fields were originally stored as text and converted to a standardized MDY
  date format for analysis.
- Currency values were standardized to USD using exchange rate data.
- Currency symbols were removed to ensure consistent numeric aggregation.

### Revenue Calculation
- A unified Revenue column was created in the Sales table using lookup logic
  to ensure consistent revenue calculations across all analyses.
- No records were deleted unless they were fully blank or analytically unusable.
---
📌 This project is part of my analytics portfolio.


