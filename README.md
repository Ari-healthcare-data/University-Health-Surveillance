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

## Current Progress (Day 3)

### Visualization and Chart Refinement

Today, I focused on translating the positivity metrics into clear, interpretable visualizations. The goal was to make insights from Day 1 & 2 easy to understand at a glance.

Key work done:

1. **Disease Positivity Chart**
   - Created a horizontal bar chart showing positivity rates by disease
   - Added data labels directly on the bars for readability
   - Observed that Chlamydia and Gonorrhea have the highest positivity
   - Noted unexpected patterns for respiratory diseases, likely due to broad precautionary testing

2. **Positivity by Disease and Population**
   - Created a grouped bar chart showing positivity rates by disease, separated by students and staff
   - Added data labels to each bar to make comparisons easier
   - Noticed that STI-related diseases (Chlamydia and Gonorrhea) show higher positivity among students compared to staff
   - For respiratory diseases like COVID-19 and Influenza, the difference between students and staff is much smaller
   - This suggests that infection patterns may depend more on the type of disease rather than just the population group
   - It also made me think that behavior and exposure (for example, social patterns) could play a role, especially for STIs

3. **Age Group Positivity Chart**
   - Built a stacked bar chart for positivity by age group and population (students vs staff)
   - Added labels for each segment to clearly show rates
   - Found most positive cases occur in ages 18–25 (students), while staff positivity is concentrated in older groups

4. **Vaccination Status Chart**
   - Created a bar chart for positivity by vaccination status
   - Corrected data label placement to avoid overlapping chart borders
   - Observed that vaccinated individuals show slightly lower positivity, but differences are small
   - This suggests vaccination status alone may not fully explain infection risk in this dataset

5. **Output**
   - All charts were saved to the `dashboards` folder for easy access
   - Ensured charts are clean, labeled, and ready for interactive dashboard integration

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

- How EHR-style data is organized
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
