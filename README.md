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

├── outputs/                       # Saved charts and reports

├── requirements.txt               # Python dependencies

└── README.md                      # Project documentation



## Progress

| Step | Notebook | Status |
|------|----------|--------|
| 1 | Project Setup | Done |
| 2 | Data Loading & First Look | Done |
| 3 | Data Cleaning | Done |
| 4 | Funnel Metrics | In Progress |
| 5 | Segmentation Analysis | Pending |
| 6 | Visualizations | Pending |
| 7 | Insights & Recommendations | Pending |


## Key Findings So Far
- Total contacts: **41,188**
- Converted (yes): **4,640**
- Not converted (no): **36,548**
- Overall conversion rate: **11.27%**

### After Cleaning:
- Dropped `default` column (too many unknowns)
- Encoded target column `y` → `y_binary` (0/1)
- Created `age_group` column → largest segment is **26-35 (14,847 people)**
- Created `campaign_bucket` for contact intensity analysis
- Final shape: **41,188 rows × 23 columns**
- Nulls remaining: **0**

## Author
- **Name:** Meklit Tensae
- **Internship:** Future Interns: Data Science & Analytics Track (2026)
- **LinkedIn:** 
