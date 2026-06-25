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
| 4 | Funnel Metrics | Done |
| 5 | Segmentation Analysis | In Progress |
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

### Funnel Stage Metrics
| Stage | Count | Conversion % |
|-------|-------|--------------|
| 1. Total Contacts | 41,188 | 100% |
| 2. Previously Contacted | 5,625 | 13.66% |
| 3. Engaged (duration > 0) | 41,184 | 99.99% |
| 4. Converted | 4,640 | 11.27% |

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

#### By Previous Campaign Outcome
| Outcome | Conversion Rate |
|---------|----------------|
| Success | **65.11%** |
| Failure | 14.23% |
| No previous contact | 8.83% |

#### Best Performing Segments
| Segment | Best Group | Conversion Rate |
|---------|-----------|----------------|
| Job | Student | **31.43%** |
| Age Group | 65+ | **46.85%** |
| Month | March | **50.55%** |
| Day | Thursday | 12.12% |
| Prev. Outcome | Success | **65.11%** |

> Customers with a previous successful campaign are **7.4x more likely** to convert than new contacts

### Visualizations Produced
| # | Chart | Type |
|---|-------|------|
| 1 | Overall Funnel Drop-off | Plotly Funnel |
| 2 | Conversion by Channel | Plotly Bar |
| 3 | Conversion by Job Type | Plotly Horizontal Bar |
| 4 | Conversion by Age Group | Plotly Bar |
| 5 | Conversion by Month | Plotly Line |
| 6 | Campaign Intensity Impact | Plotly Bar |
| 7 | Previous Outcome Impact | Plotly Bar |
| 8 | Job × Channel Heatmap | Seaborn Heatmap |

## Author
- **Name:** Meklit Tensae
- **Internship:** Future Interns: Data Science & Analytics Track (2026)
- **LinkedIn:** 
