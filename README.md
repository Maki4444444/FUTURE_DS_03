# Marketing Funnel & Conversion Performance Analysis

## Project Overview
This project analyzes a real-world bank marketing campaign dataset to understand
how leads move through a marketing funnel and where drop-offs occur.
Built as part of the **Future Interns Data Science & Analytics Internship (2026)**.


## Objective
- Identify drop-off points in the marketing funnel
- Analyze conversion rates at each funnel stage
- Compare performance across channels, age groups, and job types
- Provide actionable recommendations to improve conversions


## Dataset
- **Source:** UCI Machine Learning Repository: Bank Marketing Dataset
- **File used:** `bank-additional-full.csv`
- **Size:** 41,188 rows × 20 columns
- **Target column:** `y` (yes = subscribed, no = did not subscribe)


## Tools & Libraries
- Python 3
- Pandas, NumPy
- Matplotlib, Seaborn, Plotly
- Jupyter Notebook


## Project Structure

marketing-funnel-analysis/

│

├── data/                          # Raw dataset (not pushed to GitHub)

├── notebooks/

│   ├── 01_data_loading.ipynb      # Data loading & first look (Completed)

│   ├── 02_cleaning.ipynb          # Data cleaning (in progress)

│   ├── 03_funnel_metrics.ipynb    # Funnel stage metrics

│   ├── 04_segmentation.ipynb      # Segmentation analysis

│   ├── 05_visualizations.ipynb    # Charts & dashboards

│   └── 06_insights.ipynb          # Final insights & recommendations

├── outputs/

│   ├── 01_funnel_chart.png

│   ├── 02_channel_conversion.png

│   ├── 03_job_conversion.png

│   ├── 04_age_conversion.png

│   ├── 05_month_conversion.png

│   ├── 06_campaign_intensity.png

│   ├── 07_previous_outcome.png

│   ├── 08_heatmap_job_channel.png

│   ├── funnel_summary.csv

│   ├── channel_conversion.csv

│   ├── segment_job.csv

│   ├── segment_education.csv

│   ├── segment_age.csv

│   ├── segment_month.csv

│   ├── segment_day.csv

│   ├── segment_poutcome.csv

│   └── recommendations_summary.csv

├── requirements.txt               # Python dependencies

└── README.md                      # Project documentation                      # Saved charts and reports



## Progress

| Step | Notebook | Status |
|------|----------|--------|
| 1 | Project Setup | Done |
| 2 | Data Loading & First Look | Done |
| 3 | Data Cleaning | Done |
| 4 | Funnel Metrics | Done |
| 5 | Segmentation Analysis | Done |
| 6 | Visualizations | Done |
| 7 | Insights & Recommendations | Done |


## Key Findings

### Data Overview
- Total contacts: **41,188**
- Converted (yes): **4,640**
- Not converted (no): **36,548**
- Overall conversion rate: **11.27%**

### After Cleaning
- Dropped `default` column (too many unknowns)
- Encoded target column `y` → `y_binary` (0/1)
- Created `age_group` column → largest segment is **26-35 (14,847 people)**
- Created `campaign_bucket` for contact intensity analysis
- Final shape: **41,188 rows × 23 columns**
- Nulls remaining: **0**

### Funnel Stage Metrics
| Stage | Count | Conversion % | Drop-off % |
|-------|-------|--------------|------------|
| 1. Total Contacts | 41,188 | 100% | — |
| 2. Previously Contacted | 5,625 | 13.66% | 86.34% |
| 3. Engaged (duration > 0) | 41,184 | 99.99% | 0.01% |
| 4. Converted | 4,640 | 11.27% | 88.73% |

### Funnel Waste Analysis
- Cold contacts (no prior history): **35,563**
- Cold contacts wasted: **32,422**
- Cold contact waste rate: **91.2%**
- If only warm leads contacted: conversion jumps to **65.1%**

> **32,422 contacts were essentially wasted on cold outreach**
> the single biggest opportunity for improvement

### Conversion by Channel
| Channel | Converted | Total | Conversion Rate |
|---------|-----------|-------|-----------------|
| Cellular | 3,853 | 26,144 | **14.74%** |
| Telephone | 787 | 15,044 | 5.23% |

> Cellular is **2.8x more effective** than telephone outreach

### Conversion by Campaign Intensity
| Contacts Made | Conversion Rate |
|---------------|-----------------|
| 1 contact | **13.04%** |
| 2-3 contacts | 11.22% |
| 4-5 contacts | 8.68% |
| 6+ contacts | 5.49% |

> More calls = lower conversion. Quality over quantity wins.

### Segmentation Analysis

#### By Job Type
| Job | Conversion Rate |
|-----|----------------|
| Student | **31.43%** |
| Retired | **25.23%** |
| Unemployed | 14.20% |
| Admin | 12.97% |
| Blue-collar | 6.89% (lowest) |

#### By Age Group
| Age Group | Conversion Rate |
|-----------|----------------|
| 65+ | **46.85%** |
| 17-25 | 22.99% |
| 56-65 | 20.25% |
| 26-35 | 8.91% (lowest) |

#### By Previous Campaign Outcome
| Outcome | Conversion Rate |
|---------|----------------|
| Success | **65.11%** |
| Failure | 14.23% |
| No previous contact | 8.83% |

> Customers with a previous successful campaign are **7.4x more likely** to convert

#### Best Performing Segments
| Segment | Best Group | Conversion Rate |
|---------|-----------|----------------|
| Job | Student | **31.43%** |
| Age Group | 65+ | **46.85%** |
| Month | March | **50.55%** |
| Day | Thursday | 12.12% |
| Prev. Outcome | Success | **65.11%** |


## Actionable Recommendations

| # | Recommendation | Current Rate | Target Rate | Priority |
|---|---------------|-------------|-------------|----------|
| 1 | Prioritize warm leads over cold outreach | 8.83% | 65.11% | High |
| 2 | Switch budget from telephone to cellular | 5.23% | 14.74% | High |
| 3 | Cap contacts at 3 per lead | 5.49% | 13.04% | Medium |
| 4 | Target 65+ and student segments | 6.89% | 46.85% | Medium |
| 5 | Time campaigns to March/Sep/Oct | Low in May | 50.55% | Quick Win |



## Visualizations

| # | Chart | File |
|---|-------|------|
| 1 | Overall Funnel Drop-off | 01_funnel_chart.png |
| 2 | Conversion by Channel | 02_channel_conversion.png |
| 3 | Conversion by Job Type | 03_job_conversion.png |
| 4 | Conversion by Age Group | 04_age_conversion.png |
| 5 | Conversion by Month | 05_month_conversion.png |
| 6 | Campaign Intensity Impact | 06_campaign_intensity.png |
| 7 | Previous Outcome Impact | 07_previous_outcome.png |
| 8 | Job × Channel Heatmap | 08_heatmap_job_channel.png |


## Author
- **Name:** Your Name
- **Internship:** Future Interns: Data Science & Analytics Track (2026)

