# Shopify App Landscape & Review Analysis
Business Intelligence and data visualization project analyzing the Shopify App Store ecosystem using **Power BI** to evaluate developer responsiveness, community-weighted sentiment, and marketplace success factors.

---

## Project Documentation
- [View Full Report and Dashboard Walkthrough (PDF)](https://drive.google.com/file/d/1cmX9lJtplmw5v5PTRRQ2zfevBw1uRtph/view?usp=sharing)
- **Technical Stack:** Power BI Desktop, DAX, Relational Data Modeling

---

## Business Objective
Marketplace leadership requires structured visibility into the factors that drive app quality and developer engagement within the Shopify ecosystem.

This project transforms scraped marketplace data into actionable business intelligence supporting:

- **Marketplace scale and saturation analysis**
- **Community-weighted quality modeling**
- **Developer responsiveness and engagement monitoring**
- **Quality vs. Quantity performance benchmarking**
- **High-volume developer performance filtering**

The objective was to leverage advanced **DAX modeling** to move beyond raw averages and identify high-performing apps based on community-weighted helpfulness and developer activity.

---

## Dataset Overview
The analysis is based on a relational dataset of the Shopify App Store, including:

- **Apps:** Global app metadata (ID, title, developer, last modified date)
- **Reviews:** Granular user sentiment (rating, comment, helpful count)
- **Developer Replies:** Longitudinal data on developer engagement
- **Categories:** Cross-functional app classification labels

Data was integrated using a **Many-to-One (*:1)** relationship architecture between reviews and app metadata.



---

## Analytical Focus Areas
- **Weighted Helpfulness KPI** modeling
- **Developer response rate** assessment
- **High-traffic app performance isolation** (>500 reviews)
- **Rating vs. Review volume** correlation
- **Marketplace update frequency** and maturity trends

---

## Tools and Techniques
- **Power BI Desktop**
- **DAX (Data Analysis Expressions):** Engineered custom metrics for Weighted Helpfulness and binary Developer Answered flags.
- **Data Modeling:** Architecture of relational schemas between transactional reviews and app metadata.
- **Dashboard Design:** Interactive visualization of marketplace trends and developer benchmarks.
- **Business Intelligence Reporting:** Converting raw sentiment into executive-ready KPI cards and scatterplot correlations.

---

## Key Findings
- **Market Scale:** Identified **7,341 unique apps**, highlighting a highly saturated marketplace where visibility is driven by high review volume.
- **Engagement Impact:** Developers who actively engage with reviews maintain more stable and higher average ratings than non-responsive competitors.
- **Metric Normalization:** Weighted helpfulness calculations revealed that raw "Sum of Ratings" often provides a misleading view of actual app utility.
- **Responsiveness Leaders:** Filtering for high-volume apps (>500 reviews) successfully isolated top-tier developers who maintain elite responsiveness standards at scale.
