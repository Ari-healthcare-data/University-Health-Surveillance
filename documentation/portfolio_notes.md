# Portfolio Notes

---
---

# Day 1 & 2 – Building the Dataset and Dataset Analysis

## Summary

After creating the synthetic dataset, I began the analysis phase of the University Campus Health Surveillance project.

Instead of jumping straight into dashboards, I focused on understanding the data and building the core metrics that will drive the rest of the analysis.

The focus was on exploring infection trends and calculating positivity rates across diseases and demographic groups using Python.

---

## What I Worked On

I built the dataset to create realistic synthetic data:

- Created the dataset tables (patients, tests, vaccinations)


Creating this dataset was less complex compared to my previous project, so I completed the dataset build quicker than I expected. This allowed me to be able to do some of the initial analysis on the first day of this project.

I focused on building a strong analytical foundation:

- Loaded cleaned datasets into pandas  
- Explored dataset structure and distributions  
- Created a positivity indicator (`is_positive`)  
- Calculated positivity rates by disease  
- Built initial visualizations using matplotlib  
- Created age group segmentation  
- Merged patient and test datasets for demographic analysis  

---

## Key Observations

- Chlamydia has the highest positivity rate among diseases  
- Students make up the majority of the dataset  
- Most positive cases occur in ages 18–25  
- Students show slightly higher positivity rates than staff  

These patterns are influenced by how the dataset was designed, but they still help demonstrate how infection trends can be analyzed in practice.

---

## What Stood Out

One important realization is that positivity rate is more meaningful than raw case counts.

For example:
- Students have more total cases  
- But they also make up a larger share of the population  

Using positivity rate helps normalize this and gives a clearer picture of risk.

This was an important shift in how I interpret results.

---

## Challenges

- Handling NaN values when grouping by age and population  
- Understanding how pandas groupby behavior (observed=True vs False) affects results  
- Deciding whether missing combinations should be treated as 0 or left as NaN  
- Interpreting results carefully when some groups don’t exist in the data  

---

## Decisions I Made

To keep the analysis clear and interpretable, I made a few key decisions:

- Used mean of boolean (`is_positive`) to calculate positivity rate  
- Grouped ages into bins to simplify analysis  
- Merged datasets early to enable flexible analysis  
- Filled missing group combinations with 0 for clarity  

---

## Lessons Learned

- Feature engineering (like `is_positive`) simplifies analysis a lot  
- Groupby operations are powerful but require careful validation  
- Data structure matters more than visualization early on  
- Even simple datasets can produce meaningful insights  
- Separating counts from rates is critical when comparing groups of different sizes  

---

## What I Would Improve

If I were to do this project over again, I would:

- Add more demographic variables (race, risk factors, etc.)  
- Introduce comorbidities or severity levels  
- Model vaccination impact on positivity rates  

---

## Reflection

This phase felt more like real data analysis compared to dataset creation.

Instead of building the data, I’m now asking:

> What is the data actually telling me?

It also reinforced that:
- Clean structure makes analysis much easier  
- Simple metrics (like positivity rate) can be very powerful  
- Interpretation matters just as much as calculation  

This shift from building data to interpreting it was one of the most valuable parts of today’s work.

---

## Next Steps

- Expand analysis to include vaccination impact  
- Build more advanced visualizations  
- Export datasets for dashboard development  
- Potentially build a Power BI or Tableau dashboard

---
---
---

# Day 3 – Visualization Phase

## Summary

Today I focused on turning the positivity metrics from earlier analysis into visualizations that are easier to understand at a glance. The main goal was to make trends clear, improve readability, and highlight patterns across disease types, age groups, population groups, and vaccination status.

## What I Worked On

- Horizontal bar chart for disease positivity
- Bar chart for disease positivity split by population (students vs staff)
- Stacked bar chart for positivity by age group and population
- Bar chart for positivity by vaccination status
- Adjusted data labels to avoid overlap with chart boundaries
- Ensured age groups are displayed in a logical order for interpretation

## Key Observations

- Chlamydia and Gonorrhea show the highest positivity rates across diseases  
- When broken down by population, Chlamydia and Gonorrhea are also higher among students compared to staff  
- Influenza and COVID-19 (respiratory infections) and Norovirus (gastrointestinal infection) show lower positivity than initially expected  
- Most positive cases are concentrated in the 18–25 age group, which reflects the student population  
- Vaccinated individuals show slightly lower positivity, but the difference is very small  
- Adding data labels made it much easier to interpret differences between groups

## Challenges

- Initial data label placement caused labels to extend outside chart borders, which I fixed by using alignment and small offset adjustments  
- Ensuring stacked bar chart segments remained readable while still showing exact values  
- Making sure age groups displayed in a logical order instead of a random sorting order  
- Interpreting small differences in vaccination trends without over-interpreting the results  

## Decisions Made

- Added data labels inside bars where possible to improve readability  
- Reordered age group categories so they follow a natural progression (younger to older)  
- Used consistent color schemes across charts to make comparisons easier  
- Saved all visualizations in the `dashboards` folder for future use in Tableau  

## Lessons Learned

- Even small formatting changes (labels, spacing, ordering) can significantly improve how easy a chart is to understand  
- Visualizations reveal patterns more clearly than raw tables, especially for comparing groups  
- Breaking data down by both disease and population adds an extra layer of insight that would otherwise be missed  
- It’s important not to over-interpret small differences, especially in simulated datasets  

---
---
---

# Day 4 – Dataset Preparation for Tableau

## Summary

I focused on preparing a merged, feature-rich dataset ready for Tableau dashboard analysis. This step ensures that all metrics are accurate and visualizations can be built without additional transformations.

## What I Worked On

- Loaded cleaned patient and test datasets into Python (pandas)  
- Converted test dates to proper datetime format  
- Created derived fields: `is_positive`, `age_group`, `vaccinated`  
- Merged datasets into a single file for Tableau  
- Printed sample rows and inspected distributions to validate correctness  
- Saved final dataset as `final_dataset.csv`  

## Key Observations

- Merged dataset contains 25,103 rows and 16 columns  
- Most positive cases are in the 18–25 age group  
- Age bins and vaccination flags applied consistently across the dataset  
- Dataset is ready for direct use in Tableau dashboards  

## Challenges

- Ensuring derived fields (`age_group`, `vaccinated`) are correctly aligned with test records  
- Maintaining reproducibility: all steps performed in a notebook with print statements for validation  

## Decisions Made

- Verified row counts and categorical distributions before saving final dataset  
- Printed sample rows and value counts to confirm data integrity  
- Chose to merge datasets early to simplify downstream Tableau workflow  

## Lessons Learned

- Early validation prevents downstream errors in dashboards  
- Feature engineering in Python makes future visualizations easier and more reliable  
- Printing sample rows and distributions is an effective sanity check

---
---
---

# Day 5 – Tableau Dashboard Development

## Summary

Today I moved from Python-based analysis into Tableau to build an interactive dashboard using the final dataset.

This was the first time I could actually explore the data dynamically instead of looking at static outputs, and it changed how I interpreted some of the earlier results.

---

## What I Worked On

- Loaded the final dataset into Tableau Public
   - Verified all 21 fields were correctly imported and properly typed
   - Resolved initial issue where Tableau preview only displayed a subset of columns (View Data vs sample view discrepancy). I verified all fields were correctly imported and properly typed.

- Dashboard Visuals
   - KPIs (total tests, positive cases, vaccination rate, positivity rate)
   - Positivity rate by disease
   - Positivity rate over time
   - Positivity rate by age group and population 
   - Positivity rate by disease and population

-Fixed an initial issue where Tableau preview didn’t show all columns (this was just a preview limitation, not a data issue)
- Added filters for disease, population, and vaccination status
- Improved date formatting for time-based charts

---

## Key Observations

- The interactive dashboard made it easier to see how strongly age group affects infection patterns
- Vaccination status shows a difference, but it is not as strong as demographic effects
- Monthly aggregation makes trends easier to understand
- Filtering the dashboard changes how patterns appear quite significantly

---

## Challenges 

- Tableau initially displayed fewer columns in the sample view, even though the full dataset was correctly loaded. Tableau preview initially looked like columns were missing, which was confusing at first.
- I needed to understand the difference between sample preview vs full data load behavior in Tableau
- Ensuring `year_month` sorted correctly in chronological order required adjusting date formatting
- Filters initially only applied to individual sheets, required configuration to apply across all dashboard sheets

---

## Decisions Made

- Kept the dashboard simple instead of adding too many visuals
- Used monthly aggregation instead of quarterly trends for clarity
- Prioritized simplicity over dense dashboards
- Kept color consistent across all visualizations for readability
- Focused on interactive filtering rather than adding too many charts

---

## Reflection

This stage made the project feel more realistic.

Python helped me understand what was happening in the data, but Tableau made it easier to see how someone else might explore it.

The biggest takeaway for me is that:
> The same dataset can lead to different interpretations depending on how it is explored interactively.

