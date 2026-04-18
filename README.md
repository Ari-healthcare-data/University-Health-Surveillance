# University Campus Health Surveillance Project

## Overview

This project is a healthcare analytics case study focused on analyzing infection trends within a simulated university campus population.

The goal is to explore how electronic health record (EHR) style data can be used in practice to monitor disease spread, understand population risk, and support public health decision-making.

This dataset is fully synthetic and was created in Excel to simulate a university health system. It does not contain any real patient data. Please see [Dataset Generation](documentation/dataset_generation.md) for more details on how the dataset was created.

---

## Business Value

This project simulates how a university health system could monitor infectious diseases.

The analysis demonstrates how data can be used to:
- Detect emerging outbreaks
- Identify high-risk populations
- Monitor testing and positivity trends
- Support public health decision-making

---

## Project Focus

The main question guiding this project is:

> How can infection trends and risk patterns be identified using campus health data?

To answer this, I am analyzing:

- Infection positivity rates across diseases
- Differences in infection patterns by age group and population
- How demographic factors relate to infection risk

---

## Current Progress (Day 5)

### Tableau Dashboard Development

Today I moved from Python-based analysis into Tableau to build an interactive dashboard using the final dataset (`final_dataset.csv`).

This step was mainly about translating the final dataset into something more exploratory and visual.

Key work done:

1. **Dashboard Setup**
   - Loaded `final_dataset.csv` into Tableau Public
   - Verified all 21 fields were correctly imported and properly typed
   - Resolved initial issue where Tableau preview only displayed a subset of columns (View Data vs sample view discrepancy). I verified all fields were correctly imported and properly typed


2. **Dashboard Visuals**
   - KPIs (total tests, positive cases, vaccination rate, positivity rate)
   - Positivity rate by disease
   - Positivity rate over time
   - Positivity rate by age group and population 
   - Positivity rate by disease and population


3. **Interactivity**
   - Added filters for test date, disease, population, and vaccination status

4. **Data Formatting Fixes**
   - Fixed date formatting for the positivity rate over time (converted to readable month-year format)

---

### Key Insight from Dashboard Work

Moving into Tableau made the patterns easier to explore visually:

- Infection rates are consistently higher in younger age groups (18–25)
- Disease type has a stronger impact on positivity than vaccination status alone
- Monthly aggregation makes trends much easier to interpret than raw daily variation
- Some patterns that looked minor in Python became more noticeable once filters were added

---

## Next Steps

- Begin final portfolio presentation and executive summary refinement



---

## Key Early Insights

Some early patterns are already visible:

- Chlamydia shows the highest positivity rate among the diseases analyzed  
- Most positive cases occur within the 18–25 age group  
- Students account for the majority of positive cases  
- However, differences in positivity rates between students and staff are smaller than raw counts suggest  

Since the dataset is simulated, these patterns are shaped by how the data was generated. However, they still demonstrate how infection trends can be identified and interpreted using structured health data.

---

## Project Structure

Here’s the project folder structure on my local machine:

```
University-Campus-Health-Surveillance/
  - data/
  - documentation/
  - scripts/
  - dashboards/
  - README.md
```

---

## Dataset Overview

The project uses three main tables:

- **Patients:** demographic and population information
- **Tests:** diagnostic testing records (disease, result, dates)
- **Vaccinations:** vaccination records (type, dose, dates)

The dataset includes:

- ~7,000 patients
- ~25,000 test records
- ~10,000 vaccination records

---

## Dashboard

The interactive dashboard for this project is available on Tableau Public:

[View Tableau Dashboard]( https://public.tableau.com/app/profile/ari.m5621/viz/UniversityCampusHealthSurveillance-InfectiousDiseases/CampusInfectionTrendsDashboard)

The dashboard was built to explore infection trends across disease type, age group, population, and vaccination status.

### Dashboard Preview

![Tableau Dashboard Preview](dashboards/dashboard_preview.png)

---

## Tools Used

- Excel for dataset creation and simulation  
- Python (Pandas, NumPy) for data cleaning and analysis  
- Matplotlib for initial exploratory visualizations  
- Jupyter Notebook for step-by-step analysis workflow  
- GitHub for version control and project documentation  

---

## Approach

I structured this project to mirror how a real-world analytics workflow typically progresses:

1. **Data Validation & Cleaning**
   Ensure the dataset is reliable and correctly structured

2. **Exploratory Analysis**
   Understand distributions and key variables

3. **Metric Development**
   Define and calculate key metrics such as positivity rates

4. **Segmentation**
   Analyze trends across demographic groups

5. **Visualization (Next Step)**
   Build charts and dashboards to communicate insights

---

## Why I Built This

I’m transitioning into a healthcare data analytics role and wanted to build a project that reflects how real-world health data is actually structured and analyzed.

Instead of using a simple flat dataset, I created a multi-table system to better understand:

- How EHR-style data is organized
- How different datasets relate to each other
- How data quality issues impact analysis
- How infection trends can be measured and interpreted

---

## Next Steps

- Import the final dataset into Tableau  
- Begin building interactive dashboards and visualizations  
- Explore trends over time (seasonality, spikes)  
- Analyze infection risk by vaccination status, age group, and population  
- Refine visuals for stakeholder-ready dashboards

---

## Notes

All data used in this project is synthetic and created for learning and portfolio purposes only. No real patient data is used. Please see [Dataset Generation](documentation/dataset_generation.md) for more details on how the dataset was created.
