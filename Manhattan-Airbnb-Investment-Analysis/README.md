# Manhattan Airbnb Market Analysis — Real Estate Investment Intelligence

Business Intelligence project analyzing the Manhattan vacation rental market to identify high-yield investment opportunities and optimal property configurations using Google Sheets.

---

## Project Documentation

- [View Full Performance Report (PDF)](https://drive.google.com/file/d/1L5lRGKThufTeF4L0DDfqUg5B0q1imPsy/view?usp=sharing)

---

## Business Objective

This analysis evaluates market demand and revenue potential to provide a data-driven framework for property acquisition.

Key questions addressed:

- Which neighborhoods demonstrate the highest consistent rental demand?
- What property size (bedroom count) serves as the optimal asset class for ROI?
- How much annual revenue do top-performing listings generate?
- How do traveler preferences shift across specific Manhattan micro-markets?

---

## Dataset Overview

Multi-dimensional Airbnb activity logs including:

- **id / listing_id**: Unique property identifiers.
- **neighborhood**: Localized market segments.
- **bedrooms**: Property size configurations.
- **number_of_reviews_ltm**: Behavioral demand proxy (reviews in last 12 months).
- **available**: Occupancy status ('t' or 'f').
- **adjusted_price**: Dynamic nightly rates.

---

## Analytical Framework

### Demand Segmentation (Market Attractiveness)

- Utilized **Reviews in the Last 12 Months (LTM)** as a proxy for rental frequency.
- Built neighborhood-level Pivot Tables to rank the top 10 demand hubs.
- Calculated unique listing counts per neighborhood to assess saturation vs. demand.
- Identified **Lower East Side**, **Hell’s Kitchen**, and **Harlem** as primary targets.

### Property Size Optimization

- Normalized bedroom data to categorize Studio vs. multi-room assets.
- Analyzed review distribution across bedroom counts (0, 1, 2, 3+).
- Validated the **1-Bedroom Strategy** as the most stable investment class.
- Identified **Midtown** as a unique outlier where **Studios** outperform 1-bedroom units.

### Revenue Modeling & Benchmarking

- Engineered a 30-day revenue model by linking `listings` and `calendar` datasets.
- Calculated realized income: `IF(available="f", adjusted_price, 0)`.
- Integrated total revenue back to master listings using **SUMIF** logic.
- Applied predictive annualization (30-day revenue × 12) to estimate yearly ROI.

---

## Tools and Techniques

- **Google Sheets / Excel**
- **Pivot Tables** (Multi-dimensional market analysis)
- **PROPER / TRIM** (Data normalization & cleaning)
- **IF / ISBLANK** (Feature engineering for Studio categorization)
- **SUMIF** (Relational data integration across sheets)
- **Predictive Modeling** (Revenue scaling and annualization)

---

## Key Findings

- **Strategic Hubs:** Investment should be concentrated in high-demand neighborhoods with **5,000+ annual reviews**.
- **Asset Leader:** 1-bedroom units are the market leader, accounting for **1,265 active listings** in high-performance clusters.
- **Micro-Market Nuance:** Midtown requires a specialized Studio-focused acquisition strategy to match unique local demand.
- **Revenue Ceiling:** Top-tier listings in optimized neighborhoods generate an estimated **$359,280** in annual revenue.

---

## Business Recommendations

1. **Prioritize 1-Bedroom Assets:** Focus acquisition on 1-bedroom units in the Lower East Side and Hell's Kitchen for maximum stability.
2. **Execute Midtown Studio Pivot:** Deploy a specialized strategy for Midtown, prioritizing Studios to capture unique local traveler preferences.
3. **Target High-Review Clusters:** Avoid "The Popularity Trap" by investing only in properties with proven high-frequency review activity (LTM).
4. **Scale Revenue Modeling:** Implement the created revenue model as a diagnostic tool for vetting new property acquisitions before capital allocation.

