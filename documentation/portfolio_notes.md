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
