# University Campus Health Surveillance Project

## Overview

This project is a healthcare analytics case study focused on analyzing infection trends within a simulated university campus population.

The goal is to explore how electronic medical record (EMR) style data can be used in practice to monitor disease spread, understand population risk, and support public health decision-making.

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

## Current Progress (Day 1 & 2)

So far, I’ve focused on building a clean and reliable foundation before moving into deeper analysis.

### 1. Data Cleaning & Validation

- Loaded and validated all datasets
- Converted Excel date formats into proper datetime fields
- Verified relationships between tables
- Checked for missing values, duplicates, and invalid records
- Removed mismatched patient records

### 2. Positivity Rate Analysis

- Created a positivity indicator from test results
- Calculated positivity rates by disease
- Compared infection patterns across population groups (students vs staff)
- Grouped patients into age categories for demographic analysis
- Merged datasets to analyze infection trends across demographics

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
  - images/
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

- How EMR-style data is organized
- How different datasets relate to each other
- How data quality issues impact analysis
- How infection trends can be measured and interpreted

---

## Next Steps

The next phase of this project will focus on turning these analyses into more interpretable insights:

- Build more detailed visualizations of infection trends
- Analyze trends over time (seasonality, spikes)
- Explore relationships between vaccination status and infection rates
- Develop a dashboard to present findings more clearly

---

## Notes

All data used in this project is synthetic and created for learning and portfolio purposes only. No real patient data is used. Please see [Dataset Generation](documentation/dataset_generation.md) for more details on how the dataset was created.
