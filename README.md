# Car-Sales-Analytics-Dashboard
📌 Project Overview
This Power BI dashboard provides comprehensive analytics for a car dealership, tracking key performance metrics across sales categories, vehicle models, and time periods. The interactive visualization enables data-driven decision making for inventory management, sales strategy, and budget planning.

📊 Key Features
🔢 Core Metrics
Annual Sales Performance: Track total sales against yearly budgets

Growth Analysis: Monitor YOY growth percentages

Pre-Sales Metrics: Measure pre-sales conversions

AOV (Average Order Value): Calculate per-vehicle revenue

📈 Visualization Components
Donut Charts:

Sales type distribution (New, Used, Certified Pre-Owned)

Market segment breakdown

Bar Charts:

Horizontal: Service vs Replacement vs Other sales categories

Vertical: Monthly sales across 3 vehicle models:

SUV

Sports

Retro

Comparative Analysis:

Monthly sales trends

Budget vs actual performance

Model-wise profitability

🛠️ Technical Implementation
Data Model
Star schema design with fact tables for sales transactions

Dimension tables for:

Vehicles (Model, Type, Year)

Time (Date hierarchy)

Customers (Segment, Region)

Sales Team

**DAX Measures**
Sales Growth YoY = 
VAR CurrentYearSales = [Total Sales]
VAR PreviousYearSales = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date]))
RETURN DIVIDE(CurrentYearSales - PreviousYearSales, PreviousYearSales, 0)

Budget Variance = 
[Total Sales] - [Budgeted Sales]
Interactive Features
Cross-filtering across all visuals

Drill-down capability from annual → quarterly → monthly

Tooltip details on hover

Mobile-responsive layout
