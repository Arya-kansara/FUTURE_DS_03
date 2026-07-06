# FUTURE_DS_03 — Marketing Funnel & Conversion Performance Analysis

## 📌 Project Overview
This project analyzes the complete marketing funnel of an e-commerce business
to identify where users are dropping off, which channels perform best, and
what actions can improve lead-to-customer conversion. Completed as **Task 3**
of the Data Science & Analytics Internship at **Future Interns**.

---

## ❓ Problem Statement
An e-commerce business running campaigns across 4 marketing channels
is converting only **10.04%** of website visitors into paying customers.
Out of 10,000 users who browsed the website, only 1,004 completed a purchase.

The business needed answers to:
- Where exactly are users dropping off in the funnel?
- Which marketing channels bring the best quality leads?
- Does device type affect conversion rates?
- Which product categories and regions perform best?
- Are current promotions actually driving conversions?
- How can conversion rates be improved without increasing traffic?

Without funnel analysis, the business had no visibility into WHERE
the 89.96% of lost customers were abandoning — making it impossible
to take targeted action.

---

## ✅ Solution Approach
A three-stage analysis was performed:

1. **Python (Pandas)** — Loaded, cleaned, and structured the raw
   event-level dataset. Calculated unique user counts at each funnel
   stage, conversion rates between stages, drop-off rates, and
   channel-level performance metrics.

2. **Funnel Analysis (Python)** — Built a complete funnel breakdown
   showing conversion and drop-off at every stage. Analyzed performance
   across channels, devices, regions, product categories, and bonus flags.
   Identified two critical leak points driving 89.96% abandonment.

3. **Power BI** — Built a 3-page interactive dashboard covering overall
   funnel performance, channel analysis, and segment breakdown.
   Written insights and recommendations delivered as a client-ready report.

---

## 🛠️ Tools Used
- **Python** (Pandas, NumPy, Matplotlib, Seaborn) — data cleaning,
  funnel metric calculation, channel analysis, visualization
- **Power BI** — interactive 3-page funnel dashboard
- **Jupyter Notebook** — step-by-step analysis documentation
- **GitHub** — version control and public portfolio submission

---

## 🧹 Data Cleaning Summary
- Dataset: 21,409 events from 10,000 unique users
- Verified 0 missing values and 0 duplicate rows
- Renamed columns (removed spaces) for Python compatibility
- Converted Event_Time to proper datetime format
- Verified Revenue = 0 for non-purchase events (no null handling needed)
- Created funnel summary CSV with pre-calculated stage metrics
- Created channel summary CSV with conversion rates and traffic volume
- Exported all cleaned files for Power BI import

Full cleaning steps available in `notebooks/funnel_analysis.ipynb`

---

## 🔍 Funnel Analysis Summary

```
Stage          Users     Conversion     Drop-off
Browse         10,000       100.00%        0.00%
Add to Cart     6,949        69.49%       30.51%
Checkout        3,456        49.73%       50.27%  🚨
Purchase        1,004        29.05%       70.95%  🚨

Overall Conversion Rate: 10.04%
Overall Drop-off Rate  : 89.96%
```

Two critical leak points identified:
- Cart → Checkout: 3,493 users lost (50.27% drop-off)
- Checkout → Purchase: 2,452 users lost (70.95% drop-off)


---

## 📊 Dashboard Preview

### Page 1 — Funnel Overview
<img width="779" height="439" alt="image" src="https://github.com/user-attachments/assets/d73ab488-c51d-4256-8c40-3bed183d3bff" />
KPI cards (Total Users, Purchases, Revenue, Conversion Rate, Drop-off Rate),
Funnel Chart showing stage-by-stage drop-off, Drop-off Rate by Stage,
Conversion Rate by Stage.

### Page 2 — Channel Performance
<img width="780" height="435" alt="image" src="https://github.com/user-attachments/assets/d8a13ba4-485e-4c45-a327-fdd228c1d8bb" />
Revenue by Channel, Conversion Rate by Channel,
Traffic Volume by Channel, Average Order Value by Channel.

### Page 3 — Segment Analysis
<img width="781" height="437" alt="image" src="https://github.com/user-attachments/assets/c920477c-5403-47dc-aebf-742876a0499c" />
Revenue by Device, Revenue by Product Category,
Revenue by Region, Conversion Rate by Device.

---

## 🔍 Key Insights (Summary)

- Overall conversion rate is only **10.04%** —
  90% of visitors leave without purchasing
- **Checkout → Purchase** is the biggest drop-off (70.95%) —
  2,452 users started checkout but never completed it
- **Google Ads** leads in total revenue ($73,862) and conversion (10.63%)
- **Email** brings fewer customers but highest average order value ($278.74) —
  email customers spend more per purchase
- **Desktop** converts best (10.6%) vs Mobile (9.5%) —
  mobile users browse but don't complete purchase
- **Electronics** is the highest revenue category ($63,000)
- **South region** generates most revenue ($77,000)
- **Bonus promotions** shown during browse stage are NOT converting
  into purchases — promotional strategy needs complete redesign


---

## 💡 Top Recommendation

> Fix the checkout experience first.
> 2,452 users started checkout but didn't complete it.
> These users were one step away from buying.
> Converting just 20% of them doubles current revenue
> without spending anything on new marketing.

