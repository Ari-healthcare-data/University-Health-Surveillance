# Dataset Formulas Reference

## Overview

This document provides a technical reference for how the campus health surveillance dataset was generated in Excel.

The goal was to create a dataset that behaves like a real university health system by simulating infection testing and vaccination patterns using controlled randomness and clear logic. 
This approach allowed me to practice structuring complex data while keeping it analyzable and realistic.

---

## How to Read This Document

- Each table includes the logic behind each column, along with its purpose
- Emphasis is on *why* I structured the data this way
- Randomization is controlled to simulate realistic epidemiological patterns
- The Tests table is the main analytical table and drives most metrics

---

## What Makes This Dataset Realistic

- COVID-19 only appears after 2020 to reflect real-world emergence in the USA
- Respiratory illnesses increase in winter months, reflecting seasonal patterns
- STI positivity rates are higher in younger populations, as expected in campus settings
- Students and staff follow distinct age distributions
- Vaccination schedules mimic real-world constraints and timing

---

# **PATIENTS Table**

**patient_id**
Formula: `=ROW()-1`
Purpose: Unique identifier for each patient.

**age**
Formula: Based on student/staff status
Purpose: Students (18–25) and staff (26–65). I set these ranges to reflect realistic campus demographics and to allow meaningful age-based analysis later.

**gender**
Formula: Weighted random distribution
Purpose: Simulates population demographics.

**staff_or_student_status**
Formula: 75% Student, 25% Staff
Purpose: Reflects typical university population.

**residence_type**
Formula: Conditional on student/staff
Purpose: Students more likely on-campus.

---

# **TESTS Table**

**test_id**
Formula: `=ROW()-1`
Purpose: Unique test identifier.

**patient_id**
Formula: Random patient assignment
Purpose: Links tests to patients.

**disease**
Logic:
- Pre-2020: no COVID-19
- Post-2020: includes COVID-19
Purpose: Simulates disease emergence.

**test_date**
Formula: Random date (2019–2024)
Purpose: Enables time-based analysis.

**test_result**
Method: Probabilistic model considering:
- Disease type
- Age
- Year
- Seasonality

Purpose: I designed test results this way to simulate realistic positivity rates and trends. This ensures downstream analysis, such as calculating positivity rates by age or population, reflecting patterns that might be seen in real public health data.

**report_date**
Formula: test_date + 1–2 days
Purpose: Simulates lab delay.

**lab_source**
Formula: Random selection
Purpose: Mimics multiple testing sources.

---

# **VACCINATIONS Table**

**vaccination_id**
Formula: `=ROW()-1`
Purpose: Unique identifier.

**patient_id**
Formula: Random assignment
Purpose: Links to patients.

**vaccine_type**
Formula: COVID-19 or Influenza
Purpose: Enables comparison.

**dose_number**
Logic:
- Influenza: Max 1 per year
- COVID-19: Multiple doses

Purpose: I set these limits to mirror real-world vaccination schedules. This allows trend analysis over time and ensures metrics like “vaccination coverage” are realistic.

**vaccination_date**
Formula: Random date (2020–2024)
Purpose: Supports trend analysis.

**vaccination_year**
Formula: YEAR(date)
Purpose: Enables aggregation.

---

## Notes

- Randomness is guided rather than purely random, to simulate realistic variation
- Logical constraints prevent impossible or inconsistent scenarios
- Time-based rules create trends that mimic real-world seasonality
- The dataset prioritizes analyzability and meaningful insights over perfect realism

---

## My Goal

I designed this dataset as a simplified public health surveillance system. My goal was to create something that allows meaningful exploration of infection trends, demographic risk, and testing outcomes, while practicing real-world data structuring and analysis principles.
