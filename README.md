   # Olist E-Commerce Delivery Analysis (Power BI)

Power BI analysis of delivery performance and customer satisfaction using the Olist Brazilian E-Commerce dataset — 96,000+ orders analyzed end-to-end.

## Key Finding
Late deliveries don't just delay a package — they cost nearly 2 stars in customer rating.
- On-time orders average **4.29★**
- Late orders drop to **2.57★**

## Other Findings
- 🚚 Shipping/transit time (not payment or warehouse delays) accounts for ~75% of total delivery time
- 📍 North/Northeast Brazil states see delivery times 3-4x the national average, driven by distance from logistics hubs
- 📈 A holiday order surge (Nov-Dec 2017) temporarily overwhelmed capacity, pushing delivery times to 16.5 days by Feb 2018 — recovery took ~3 months
- ✅ Overall delivery time improved from 13 days (2017) to 7 days (2018)

## Approach
The dataset came as 9 separate CSV files (orders, items, payments, reviews, products, customers, sellers, etc.) requiring a proper relational data model rather than a single flat table.

**Power Query:**
- Cleaned and merged tables, resolving duplicate keys and row-count mismatches
- Broke total delivery time into stages (payment approval → warehouse processing → carrier transit) via calculated columns

**DAX:**
- Built measures comparing performance across delivery status, time period, and region

**Investigation approach:**
Rather than stopping at "delivery is sometimes late," I tested multiple hypotheses (order volume shifts, regional mix, payment type) to isolate the actual drivers of delay.

## Report Pages
1. **Executive Summary** — high-level KPIs and key findings
2. **Delivery Performance** — trend, on-time/late split, stage breakdown
3. **Why Deliveries Slow Down** — root-cause investigation (seasonal + geographic)
4. **Customer Satisfaction & Reviews** — delivery's impact on ratings

## Demo
[Watch the interactive report demo](Screen Recording 2026-09-14 180845.mp)

## Tools Used
Power BI (Power Query, DAX) | Dataset: [Olist Brazilian E-Commerce](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

## Note
This was my first end-to-end multi-table Power BI project. Feedback welcome!
 
