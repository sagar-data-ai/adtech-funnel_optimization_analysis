# Multi-Channel Ad Spend Efficiency & Funnel Leakage Analysis

This project analyzes advertising campaign performance across Facebook and Instagram using a large-scale Meta Ads dataset.  
The goal is to identify funnel leakage points, evaluate ad format efficiency, segment audiences, and deliver data-backed recommendations to optimize ad spend and improve conversion rates.

---

## Project Objectives

- Analyze full-funnel ad performance from impressions to purchases
- Identify where and why the conversion funnel is leaking
- Segment audiences by demographics and geography for sharper targeting
- Compare ad format performance (Video, Stories, Carousel, Image)
- Deliver actionable budget optimization and scheduling recommendations

---

## Dataset Description

The dataset consists of four relational tables representing a typical Meta advertising analytics pipeline.

### 1. Campaigns Table
Contains campaign-level strategy and budget information.

Columns include:
- campaign_id
- name
- start_date
- end_date
- duration_days
- total_budget

### 2. Ads Table
Contains ad creative metadata and targeting configuration.

Columns include:
- ad_id
- campaign_id
- ad_platform
- ad_type
- target_gender
- target_age_group
- target_interests

### 3. Users Table
Stores demographic and interest information of users interacting with ads.

Columns include:
- user_id
- user_gender
- user_age
- age_group
- country
- location
- interests

### 4. Ad Events Table
Captures every interaction event between a user and an ad.

Columns include:
- event_id
- ad_id
- user_id
- timestamp
- day_of_week
- time_of_day
- event_type

---

## Dataset Scale

- Ad Events: ~400,000 rows
- Users: ~9,800 rows
- Ads: 200 ads
- Campaigns: 50 campaigns
- Total Budget Tracked: ~$2.5M

---

## Project Workflow

```
Raw Data (4 Tables)
↓
Data Cleaning & Preprocessing
↓
Exploratory Data Analysis (EDA)
↓
Funnel Analysis & Leakage Detection
↓
Audience Segmentation
↓
Ad Format & Time-Based Analysis
↓
Dashboard & Recommendations
```

---

## Key Analysis Areas

- **Funnel Leakage Detection** — Identified 11.79% CTR but only 0.60% purchase rate, exposing a critical conversion drop-off between clicks and purchases
- **Audience Segmentation** — Segmented 9,800+ users by age, gender and geography to identify high-engagement segments
- **Ad Format Performance** — Compared CTR and CVR across Video, Stories, Carousel and Image formats
- **Time-Based Analysis** — Analyzed 400K+ events by time-of-day and day-of-week to identify peak engagement windows
- **Budget Optimization** — Recommended reallocation of ad spend toward top-performing formats and geographies

---

## Key Metrics & Findings

| Metric | Value |
|---|---|
| Total Impressions | 339,812 |
| Total Clicks | 40,079 |
| Total Purchases | 2,031 |
| CTR | 11.79% |
| Conversion Rate | 5.07% |
| Purchase Rate | 0.60% |
| Total Campaign Budget | $2.5M |

---

## Ad Format Performance

| Ad Type | CTR | CVR |
|---|---|---|
| Video | 11.90% | 5.07% |
| Stories | 11.73% | 5.34% |
| Image | 11.88% | 4.67% |
| Carousel | 11.72% | 5.13% |

---

## Tools & Technologies

- Python (Pandas, Matplotlib, Seaborn)
- SQL (MySQL)
- Excel
- Power BI

---

## Repository Structure

```
multi-channel-ad-spend-funnel-analysis
│
├── data
│   └── sample_ad_events.csv
│
├── notebooks
│   ├── 01_data_cleaning.ipynb
│   ├── 02_funnel_analysis.ipynb
│   ├── 03_audience_segmentation.ipynb
│   └── 04_ad_format_analysis.ipynb
│
├── sql
│   └── analysis_queries.sql
│
├── dashboard
│   └── ad_performance_dashboard.png
│
├── docs
│   ├── Business_Requirements_Document.md
│   ├── Domain_Knowledge_Document.md
│   └── Dashboard_Insights.md
│
├── requirements.txt
│
└── README.md
```

---

## Recommendations

1. **Fix conversion funnel** — Retarget 40K+ users who clicked but did not purchase via optimized landing pages and stronger offers
2. **Refine audience targeting** — Focus budget on 18–34 age segment which drives highest engagement
3. **Reallocate ad budget** — Shift spend toward Video (highest CTR) and Stories (highest CVR)
4. **Schedule ads smartly** — Weight budget toward afternoon and evening hours for peak engagement
5. **Segment geographic strategy** — Treat high-volume markets (India, US) and high-value markets (Germany, UK) differently

---

## Author

**Sagar Kumar**  
Data Analyst | 2+ Years Experience  
[LinkedIn](https://www.linkedin.com/in/datasagar) | [GitHub](https://github.com/sagar-data-ai)
