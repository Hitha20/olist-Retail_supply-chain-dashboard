# olist-Retail_supply-chain-dashboard
Power BI dashboard analyzing delivery performance and customer satisfaction on real Olist e-commerce data
# Brazilian E-Commerce Supply Chain Dashboard (Olist)

An interactive Power BI dashboard analyzing ~100,000 real e-commerce orders from the Olist Brazilian marketplace to measure delivery performance, identify regional logistics gaps, and quantify how delivery reliability affects customer satisfaction.

## Overview

This project analyzes the full order lifecycle of a real Brazilian e-commerce marketplace to answer a core supply chain question: **where is delivery performance breaking down, and how does it affect customers?**

The dashboard tracks delivery KPIs, breaks performance down by geographic region, and uses Power BI's built-in AI to surface what drives customer satisfaction.

## Dataset

**Source:** Brazilian E-Commerce Public Dataset by Olist (Kaggle)

Real anonymized commercial data covering ~100,000 orders placed between 2016 and 2018. The dataset includes the complete order lifecycle: purchase timestamp, estimated delivery date, actual delivery date, seller and customer location, freight values, and customer review scores.

Key tables used:
- `olist_orders_dataset` — order and delivery timestamps
- `olist_order_reviews_dataset` — customer satisfaction scores (1-5)
- `olist_customers_dataset` — customer location (state)
- `olist_order_items_dataset` — pricing and freight

## Key Performance Indicators

Built as DAX measures that recalculate dynamically with filters:

- **On-Time Delivery Rate: 94.96%** — orders delivered by the estimated date
- **Total Delivered Orders: ~96K** — completed deliveries
- **Average Delivery Time: 12.5 days** — from purchase to delivery
- **Average Review Score: 4.09 / 5** — customer satisfaction

## Key Findings

**1. Geography drives delivery performance.**
Remote northern states (such as Amapá and Roraima) showed both the lowest on-time rates and the longest average delivery times, pointing to distance and carrier coverage as the core logistics challenge rather than random variation.

**2. Delivery completion is the strongest driver of satisfaction.**
Using Power BI's Key Influencers AI visual, the analysis found that successful delivery increases the average review score by 2.42 points — quantifying how directly delivery reliability affects the customer relationship.

**3. On-time rate is strong but estimates carry buffer.**
The ~95% on-time rate is high partly because estimated delivery dates are padded. A real operational opportunity is tightening delivery promises to be more competitive while maintaining reliability.

## Tools & Techniques

- **Power BI Desktop** — data modeling, interactive dashboard
- **Power Query** — data loading, type validation, transformation (ETL)
- **DAX** — calculated measures for all KPIs
- **Data modeling** — relationships across four linked tables
- **Key Influencers (AI visual)** — automated driver analysis of customer satisfaction

## Dashboard Features

- Four headline KPI cards
- On-time delivery rate by state
- Average delivery time by state
- Order volume trend over time
- Customer review score distribution
- AI-powered Key Influencers analysis
- Interactive state slicer for drill-down

## Business Application

This analysis framework applies directly to institutional and enterprise procurement. The same KPIs and breakdowns translate to tracking purchase order performance across vendors and locations — identifying which suppliers miss delivery windows, which sites face logistics delays, and how delivery reliability affects operational outcomes. Connected to a live ERP system, the dashboard would refresh automatically and support proactive alerting when performance drops below threshold.

## Future Enhancements

- Live connection to an ERP system for automatic data refresh
- Automated alerts when on-time rate falls below a defined threshold
- Predictive delivery-time forecasting by region and vendor
- Data validation layer to maintain input quality
