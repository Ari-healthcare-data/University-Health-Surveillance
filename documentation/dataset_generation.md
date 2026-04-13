# Dataset Generation

## Overview

I created this dataset to simulate a university campus health surveillance system.

The goal was to model how infectious disease testing and vaccination data might be collected and analyzed in a real-world campus environment. Rather than building a single flat dataset, I structured the data into multiple related tables to reflect how public health and clinical data are typically organized.

This dataset is fully synthetic and designed for learning and portfolio purposes only.

---

## Why I Designed It This Way

I intentionally designed this dataset to balance realism with simplicity.

The goal was not to perfectly replicate real-world epidemiology, but to create a dataset that:
- supports meaningful analysis
- demonstrates core data analyst skills
- reflects how healthcare data is structured in systems like EHRs

This approach allowed me to focus on data cleaning, validation, and analysis workflows that are directly relevant to healthcare analytics roles.

---

## Tables Included

- Patients
- Tests
- Vaccinations

Each table represents a different aspect of a campus health system:
- **Patients:** Demographic and population structure
- **Tests:** Diagnostic testing events and outcomes
- **Vaccinations:** Immunization records over time

---

## How the Tables Connect

The dataset follows a simple relational structure:

- Patients are the central entity
- Tests link to patients via `patient_id`
- Vaccinations link to patients via `patient_id`

This structure allows for:
- Demographic analysis of infection patterns
- Positivity rate calculations across populations
- Longitudinal tracking of vaccination and testing behavior

---

## Data Generation Approach

The dataset was generated in Excel using a combination of:

- Randomization (`RAND`, `RANDBETWEEN`)
- Conditional logic (`IF`, `SWITCH`)
- Lookup functions (`XLOOKUP`)
- Time-based logic (YEAR, MONTH)

Rather than using purely random values, I applied **controlled randomness** to simulate realistic epidemiological patterns.

Examples:

- Students are primarily aged 18–25, while staff are older
- COVID-19 only appears in data from 2020 onward
- Respiratory illnesses (Influenza, COVID-19, Norovirus) show higher rates in winter
- STI positivity rates are higher in younger populations
- Vaccination schedules reflect real-world constraints (e.g., one flu shot per year)

---

## Key Design Decisions

### 1. Patients as the Anchor Table
All analysis flows through the patient population, allowing demographic segmentation.

### 2. Time-Aware Disease Logic
Disease assignment and positivity rates depend on:
- Year (pre/post COVID-19)
- Seasonality (winter spikes)
- Age group

### 3. Probabilistic Test Results
Test outcomes are not random. They are based on:
- Disease-specific positivity rates
- Seasonal adjustments
- Age-based risk

This allows realistic calculation of positivity rates.

### 4. Vaccination Constraints
- **Influenza:** Max 1 dose per year
- **COVID-19:** Multiple doses allowed
- **Vaccination Dates:** Spans multiple years for trend analysis

---

## Things That Were Tricky

- Designing realistic positivity rates across diseases
- Balancing randomness with believable epidemiological patterns
- Preventing impossible scenarios (e.g., COVID-19 before 2020 in the USA) 
- Maintaining relationships across multiple tables
- Ensuring distributions looked realistic after generation

---

## Limitations

The structure and dataset I made will make it possible for me to run analyses that are commonly done in healthcare settings. However, there are a few limitations, including:

- Positivity rates are approximations and not based on real epidemiological data
- I did not model comorbidities or disease severity
- Vaccination effectiveness is not explicitly incorporated
- Behavioral factors (e.g., exposure risk) are simplified

These tradeoffs allowed me to focus more on data structure, cleaning, and analysis rather than complex modeling.

---

## Why This Matters

Designing the dataset this way allows for meaningful analysis such as:

- Positivity rate comparison by disease
- Demographic risk analysis
- Population-level infection trends
- Basic public health insights

---

## Data Quality Note

This dataset intentionally reflects some real-world characteristics:

- Uneven population distribution (more students than staff)
- Seasonal variation in disease patterns
- Missing combinations (e.g., no staff in younger age groups)

These are not errors, they reflect a simplified realistic population structure.

---

## Reflection

Building this dataset helped me better understand how healthcare data is structured and the importance of designing data in a way that supports reliable analysis.

---
---
---

## Day 3 - Progress

The cleaned datasets created in Day 1 & 2 have been successfully used to generate visualizations that communicate key insights clearly:

- Positivity rates by disease, age group, and vaccination status can now be visualized directly
- Dataset structure proved sufficient for stacked, labeled, and comparative charts
- I made small adjustments to the order of categories and cleaned up labels to make the charts easier to read and understand. These changes were done in Python using pandas and matplotlib inside the Jupyter notebook.
---
---
---

## Day 4 – Final Dataset for Dashboard

I have now merged the cleaned datasets to create a single, analysis-ready file for Tableau:

- Patient demographics and test records are fully combined  
- Key fields added: `is_positive`, `age_group`, `vaccinated`  
- Dataset structure supports Tableau dashboards with minimal further transformation  
- Validated row counts, distributions, and sample data to confirm accuracy

---
---
---
## Notes

All data is synthetic and created for learning purposes only. No real patient data is used.

For a more detailed breakdown of the column-level logic, formulas, and design decisions used to generate this dataset, see the [Dataset Formulas Reference](dataset_formulas_reference.md).
