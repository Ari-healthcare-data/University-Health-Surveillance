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

## Current Progress (Day 4)

### Dataset Preparation for Tableau

Today, I focused on preparing a clean, merged dataset for Tableau dashboard analysis. This involved combining patient demographics with test data and creating key features such as positivity, age groups, and vaccination status.

Key work done:

1. **Dataset Merging**
   - Combined `patients` and `tests` tables using `patient_id` as the join key
   - Verified that all rows merged correctly and handled any missing patient IDs

2. **Feature Engineering**
   - Created `is_positive` flag for infection results
   - Generated age groups (`18–20`, `21–25`, `26–35`, `36–50`, `51–65`)
   - Created `vaccinated` flag for immunization status

3. **Data Validation**
   - Printed sample rows (`df.head()`) to inspect merged dataset
   - Checked distribution of age groups and positivity flags
   - Confirmed final dataset shape: 25,103 rows × 16 columns

4. **Output**
   - Saved merged dataset as `final_dataset.csv` for Tableau dashboard use


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
