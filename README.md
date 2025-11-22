# Clickstream-Ecommerce-Funnel-Analysis
A Power BI dashboard analyzing user clickstream data to understand drop-offs in the e-commerce conversion funnel.

Week 1: Data Understanding & Cleaning
1. Objective
Understand the clickstream dataset and prepare it for funnel analysis by cleaning, fixing inconsistencies, and preparing usable fields for Power BI.

2. Tasks Completed
Imported raw clickstream dataset (sessions.csv, products.csv, reviews.csv, orders.csv)
Performed detailed data cleaning, including:
Removal of duplicates
Handling missing values
Standardizing date & time formats
Cleaning text fields (lowercasing, trimming, removing special characters)
Correcting outliers and invalid values
Fixing inconsistent product names
Unifying session identifiers
Merged all datasets into a structured format suitable for funnel modeling.

3. Tools Used
Python (Pandas, NumPy)
Power BI
Excel / CSV data exploration

4. Key Learnings
How clickstream events behave in real e-commerce flows
How session-level data requires careful cleaning
Importance of consistent identifiers across datasets
Converting raw data into funnel stages

5. Next Steps (Week 2 Preview)
Build the Power BI funnel model
Create DAX measures for:
Sessions
Product views
Add-to-cart rate
Checkout conversions
Design dashboards and interactive visuals

Week 2 – Data Modelling & Basic Funnel Visualization

Objective
Design the star schema, create base DAX measures, and build the initial funnel dashboard.

Tasks Completed
1️. Built Star Schema
Created and validated table relationships:
fEvents → dSessions
fOrders → dCustomers
fOrderItems → dProducts
fOrders → fOrderItems
fOrders → dDate

Ensured correct cardinality and filter directions.

2️. Created Base DAX Measures
Sessions = DISTINCTCOUNT(fEvents[SessionID])
Orders = DISTINCTCOUNT(fOrders[OrderID])
Conversion Rate % = DIVIDE([Orders], [Sessions], 0)

These measures power funnel KPIs.

3️. Built Funnel Visualization
Tracked journey stages:
Homepage visits
Product page visits
Add-to-cart
Checkout
Purchase

Used Funnel visual for drop-off visualization.

4️. Added KPI Cards
Total Sessions
Total Orders

Conversion Rate %

5️. Added Interactive Slicers
Device Type
Traffic Source
Date

Output
A fully working basic dashboard that visualizes user behavior flow and drop-offs.
