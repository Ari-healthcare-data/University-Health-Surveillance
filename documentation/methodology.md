# Methodology

## Overview

This project follows a structured analytical workflow, moving from raw synthetic data to exploratory analysis and insight generation using Python.

The focus of this project is infection positivity analysis, with an emphasis on understanding how disease patterns vary across populations and over time.

Rather than trying to model everything, I focused on building a clear and reliable approach to measuring and interpreting positivity rates.

---

## Approach

Rather than starting with visualization, on Day 1 and 2 I focused on:

- Understanding the dataset
- Validating structure and distributions
- Creating derived metrics (positivity rates)
- Analyzing patterns across demographics

This mirrors how I would approach a real-world healthcare analytics problem, where understanding the data comes before building dashboards or visualizations.

---

## Step 1: Data Loading

I loaded cleaned datasets into Python using pandas:

- patients_cleaned.csv
- tests_cleaned.csv
- vaccinations_cleaned.csv

Initial checks included:
- Row counts
- Column structure
- Data types

---

## Step 2: Data Understanding

Before calculating metrics, I explored:

- Test distribution by disease
- Population composition (students vs staff)
- Vaccination distribution

I used this step to sanity check whether the data looked reasonable before moving into calculations.

---

## Step 3: Feature Engineering

### Key Derived Fields

- **is_positive** 
  Boolean flag derived from `test_result`

- **age_group**
  Created using bins to group patients:
  - 18–20
  - 21–25
  - 26–35
  - 36–50
  - 51–65

These features enable demographic analysis.

---

## Step 4: Data Integration

Test data was merged with patient data:

- Join key: `patient_id`
- Result: combined dataset with demographic + test data

This enables:
- Population-level analysis
- Age-based trends
- Student vs staff comparisons

This was a key step, since most of the analysis depends on combining clinical data with demographic context.

---

## Step 5: Positivity Rate Calculations

Positivity rate is defined as:

> Positive Tests / Total Tests

I used `groupby` operations in pandas to calculate this across different segments:

- By disease
- By population (student vs staff)
- By age group
- By combined age and population

Since this is a simulated dataset, the exact rates are influenced by how the data was generated. That said, the process still reflects how this type of analysis would be done in a real-world setting.

Positivity rate is an important metric in public health because it accounts for how much testing is being done, not just how many positive cases there are.

It’s commonly used to:

- Spot potential outbreaks
- Track how diseases are spreading
- Understand whether enough testing is being done

---

## Step 6: Visualization

Used matplotlib to create:

- Positivity rate by disease (bar chart)
- Positivity rate by population group

Focus:
- Clear labeling
- Simple, readable visuals
- Direct comparison across categories


---

## Step 7: Validation

Validation checks included:

- Ensuring positivity rates fall within expected ranges
- Verifying groupby outputs match raw counts
- Checking for missing or invalid combinations
- Handling NaN values in grouped data

Before finalizing results, I performed several validation checks to make sure the calculations were correct.

---

## Design Philosophy

- Keep analysis simple and interpretable
- Focus on meaningful metrics (positivity rate)
- Build from raw data → features → metrics → insights
- Avoid overcomplicating early-stage analysis

---

## Challenges Encountered

- Handling missing group combinations (NaN values) when grouping by age and population
- Deciding whether to use `observed=True` vs `False` in pandas groupby operations
- Interpreting results carefully given the uneven population distribution (more students than staff)
- Avoiding over-interpreting patterns in a simulated dataset

---

## Summary

This methodology focuses on building a clear, step-by-step analytical workflow:

- Data → Features → Metrics → Insights

Overall, this approach helped me move from raw data to interpretable insights in a structured and transparent way.

The goal was not just to compute metrics, but to understand what they mean and how they would be used in a real-world setting.
