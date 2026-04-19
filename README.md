# University Campus Health Surveillance Project


## Table of Contents

- [Overview]( https://github.com/Ari-healthcare-data/University-Health-Surveillance/tree/main#overview)

  - [Business Value](https://github.com/Ari-healthcare-data/University-Health-Surveillance/tree/main#business-value)

  - [Project Structure](https://github.com/Ari-healthcare-data/University-Health-Surveillance/tree/main#project-structure)

  - [Dashboard Preview]( https://github.com/Ari-healthcare-data/University-Health-Surveillance/tree/main#dashboard)

  - [Why I Built This]( https://github.com/Ari-healthcare-data/University-Health-Surveillance/tree/main#why-i-built-this)

- [Dataset Generation]( https://github.com/Ari-healthcare-data/University-Health-Surveillance/blob/main/documentation/dataset_generation.md#dataset-generation)

- [Dataset Formulas Reference]( https://github.com/Ari-healthcare-data/University-Health-Surveillance/blob/main/documentation/dataset_formulas_reference.md#dataset-formulas-reference)

- [Methodology]( https://github.com/Ari-healthcare-data/University-Health-Surveillance/blob/main/documentation/methodology.md#methodology)

- [Portfolio Notes]( https://github.com/Ari-healthcare-data/University-Health-Surveillance/blob/main/documentation/portfolio_notes.md#portfolio-notes)

- [Executive Summary]( https://github.com/Ari-healthcare-data/University-Health-Surveillance/blob/main/documentation/executive_summary_campus_infectious_disease_trends.md#executive-summary-campus-infectious-disease-trends-dashboard)


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

## End-to-End Workflow

This project follows a full analytics lifecycle:

1. Dataset design (synthetic EHR-style data)
2. Data cleaning and validation (Python)
3. Feature engineering and metric development
4. Exploratory analysis and visualization
5. Interactive dashboard development (Tableau)
6. Executive summary for stakeholder communication

My goal for this project was to mirror how real-world analytics projects are done.

---

## Notes

All data used in this project is synthetic and created for learning and portfolio purposes only. No real patient data is used. Please see [Dataset Generation](documentation/dataset_generation.md) for more details on how the dataset was created.
