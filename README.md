# AI Job Displacement Intelligence Dashboard
### Workforce Automation & AI Disruption Analysis 2020-2026

---

## Project Overview

This project analyzes the impact of Artificial Intelligence and automation on the global workforce using a dataset of **15,000 job records** spanning **8 industries**, **9 countries**, and **10 job roles** from **2020 to 2026**.

An interactive **4-page Power BI dashboard** was built to visualize automation risk, salary impact, reskilling urgency, skill gap analysis, and AI adoption levels across industries, countries, and roles.

---

## Project Structure

```
AI-Job-Displacement-Analysis/
│
├── dataset/
│   └── ai_job_replacement_2020_2026_v2.csv   # Raw dataset (15,000 records, 20 columns)
│
├── powerbi/
│   └── Copy_AI_Job_Replacement_Insights.pbix  # Power BI Dashboard file
│
├── reports/
│   ├── project_summary.pdf                    # Full project summary report
│   └── industry_level_report.pdf              # Detailed industry-by-industry analysis
│
└── README.md                                  # This file
```

---

## Dataset Details

| Property | Value |
|---|---|
| File | `ai_job_replacement_2020_2026_v2.csv` |
| Total Records | 15,000 |
| Time Period | 2020 – 2026 |
| Industries | 8 |
| Countries | 9 |
| Job Roles | 10 |
| Total Features | 20 columns |

### Columns

| Column | Type | Description |
|---|---|---|
| `job_id` | Integer | Unique record identifier |
| `job_role` | Text | Job title (10 distinct roles) |
| `industry` | Text | Industry sector (8 categories) |
| `country` | Text | Country (9 countries) |
| `year` | Integer | Year 2020-2026 |
| `automation_risk_percent` | Decimal | Automation probability 0-100% |
| `ai_replacement_score` | Decimal | AI replacement capability score |
| `skill_gap_index` | Decimal | Skills gap measure 0-100 |
| `salary_before_usd` | Decimal | Salary before AI adoption (USD) |
| `salary_after_usd` | Decimal | Salary after AI adoption (USD) |
| `salary_change_percent` | Decimal | Salary change % (-38% to +37%) |
| `skill_demand_growth_percent` | Decimal | Growth in skill demand |
| `remote_feasibility_score` | Decimal | Remote work potential |
| `ai_adoption_level` | Decimal | AI adoption level in role |
| `education_requirement_level` | Integer | Education level required (1-5) |
| `automation_risk_category` | Text | High / Medium / Low |
| `skill_transition_pressure` | Decimal | Pressure to change skills |
| `wage_volatility_index` | Decimal | Wage volatility due to AI |
| `reskilling_urgency_score` | Decimal | Urgency to reskill (0-80) |
| `ai_disruption_intensity` | Decimal | Overall disruption score |

---

## Key Statistics

| Metric | Value |
|---|---|
| Total Records | 15,000 |
| Avg Automation Risk | 46.2% |
| Avg AI Replacement Score | 46.2 |
| Avg Salary Before AI | $89,771 |
| Avg Salary After AI | $89,871 |
| Net Salary Change | +$100 (+0.11%) |
| Max Salary Gain | +36.92% |
| Max Salary Loss | -38.37% |
| Avg Reskilling Urgency | 35.9 |
| Avg Skill Gap Index | 50.0 |
| High Risk Jobs | 4,496 (30.0%) |
| Medium Risk Jobs | 6,464 (43.1%) |
| Low Risk Jobs | 4,040 (26.9%) |

---

## Power BI Dashboard

The dashboard (`Copy_AI_Job_Replacement_Insights.pbix`) consists of **4 interactive pages**:

### Page 1 — Executive Overview
- 6 KPI Cards (Total Records, Avg Risk, AI Score, Salary Change, Reskilling, High Risk %)
- Trend Line Chart: Automation Risk & AI Score 2020-2026
- Donut Chart: Risk Category Distribution
- Bar Charts: Industry AI Scores & Role Reskilling Rankings
- Slicers: Year, Industry, Country, Role, Risk Level

### Page 2 — Industry & Role Deep-Dive
- Clustered Bar Chart: AI Score by Industry × Risk Level
- Scatter Plot: Skill Gap vs AI Adoption (bubble = disruption intensity)
- Column Chart: Skill Demand Growth % by Role

### Page 3 — Country & Time Analysis
- Heatmap Matrix: Country × Year automation risk (color-coded)
- Area Chart: Risk trends for top 5 countries
- Map Visual: Global risk bubbles by country

### Page 4 — Salary & Skill Intelligence
- Waterfall Chart: Salary change by risk category
- Gauge Chart: Reskilling urgency score vs target
- Smart Narrative: AI-generated insight text
- Data Table: Full filterable/sortable record explorer

### DAX Measures
```dax
Total Records = COUNTROWS(ai_job_replacement_2020_2026_v2)
Avg Automation Risk = AVERAGE([automation_risk_percent])
Avg AI Score = AVERAGE([ai_replacement_score])
Avg Salary Before = AVERAGE([salary_before_usd])
Avg Salary After = AVERAGE([salary_after_usd])
Avg Salary Change % = AVERAGE([salary_change_percent])
High Risk Count = CALCULATE(COUNTROWS(...), [automation_risk_category] = "High")
High Risk % = DIVIDE([High Risk Count], [Total Records], 0) * 100
Avg Reskilling Urgency = AVERAGE([reskilling_urgency_score])
```

---

## Key Findings

### By Job Role
| Role | Avg Risk | Status |
|---|---|---|
| Truck Driver | 60.74% | 🔴 Highest risk |
| Customer Support Rep | 59.85% | 🔴 Very high risk |
| Marketing Specialist | 45.44% | 🟡 Medium risk |
| Mechanical Engineer | 45.40% | 🟡 Medium risk |
| Teacher | 45.14% | 🟡 Medium risk |
| HR Manager | 45.09% | 🟡 Medium risk |
| Accountant | 44.98% | 🟡 Medium risk |
| Financial Analyst | 44.70% | 🟡 Medium risk |
| Data Analyst | 35.46% | 🟢 Low risk |
| Software Engineer | 34.85% | 🟢 Lowest risk |

### By Industry
| Industry | Avg Risk | Salary Change |
|---|---|---|
| Energy | 47.02% | -0.02% |
| Manufacturing | 46.88% | +0.04% |
| Finance | 46.41% | +0.18% |
| Retail | 46.13% | +0.36% ✅ Best |
| Transportation | 45.87% | +0.30% |
| Technology | 45.75% | +0.12% |
| Healthcare | 45.76% | +0.04% |
| Education | 45.60% | -0.11% |

### By Country
| Country | Avg Risk | Salary Change |
|---|---|---|
| Australia | 46.57% | +0.08% |
| Singapore | 46.53% | +0.13% |
| UK | 46.48% | -0.11% |
| Japan | 46.33% | +0.10% |
| USA | 46.09% | -0.05% |
| Canada | 46.09% | +0.01% |
| India | 46.08% | +0.38% |
| Germany | 45.76% | +0.58% ✅ Best |
| Brazil | 45.61% | -0.06% |

---

## Yearly Trend

| Year | Avg Risk | Signal |
|---|---|---|
| 2020 | 46.50% | Baseline |
| 2021 | 46.10% | Slight dip |
| 2022 | 46.31% | Recovering |
| 2023 | 46.51% | Mid-peak |
| 2024 | 45.36% | Lowest risk year |
| 2025 | 45.56% | Rising again |
| 2026 | 46.87% | **Peak disruption year** |

---

## Reports

### `project_summary.pdf`
Complete project summary covering:
- Executive Summary with KPIs
- Dataset structure and column descriptions
- Statistical summary (min, max, avg for all metrics)
- Year, Role, Industry, Country analysis
- Power BI dashboard structure and DAX measures
- Conclusions and strategic recommendations

### `industry_level_report.pdf`
Detailed industry-by-industry report covering each of the 8 industries with:
- Sector overview and AI disruption summary
- Risk breakdown (High / Medium / Low counts)
- Key automation drivers
- Roles at highest risk
- Salary impact analysis
- Strategic recommendation per sector

---

## Tools Used

| Tool | Purpose |
|---|---|
| Microsoft Power BI Desktop | Dashboard creation, DAX measures, visualization |
| CSV (Python analysis) | Data exploration and statistics |
| ReportLab (Python) | PDF report generation |

---

## How to Open the Dashboard

1. Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
2. Open `Copy_AI_Job_Replacement_Insights.pbix`
3. If prompted, re-link the data source to `ai_job_replacement_2020_2026_v2.csv`
4. Use slicers to filter by Year, Industry, Country, Role, or Risk Level
5. Click bookmark buttons for pre-configured views (High Risk View, Technology, 2024-2026)

---

## How to Share the Dashboard

| Method | Steps |
|---|---|
| Share via link | Publish to Power BI Service → Share → Copy link |
| Embed in website | File → Embed report → Publish to web → Copy iframe code |
| Email report | Export → PDF → Send as attachment |
| Mobile view | Share Power BI Service link → Open in Power BI mobile app |

---

## Conclusions

1. **AI disruption is global** — no industry or country is immune; risk variance is minimal across all sectors and geographies.
2. **Truck Drivers and Customer Support Reps** face immediate, high-priority automation risk requiring urgent reskilling investment.
3. **Software Engineers and Data Analysts** are best positioned — AI augments rather than replaces technical knowledge workers.
4. **Salary impact is near-neutral overall** (+0.11%) but masks extreme individual variance (-38% to +37%).
5. **2026 is the projected peak disruption year** — organisations must prepare workforce strategies now.
6. **Germany and India** show the strongest salary adaptation post-AI, indicating effective reskilling ecosystems.

---

*AI Job Displacement Intelligence Project | Power BI Dashboard | Data Analysis 2020-2026*
