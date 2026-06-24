# YRBS 2007 Final Individual Project

## Student Information
Name: 黃立帆  
Student ID: 112370206

## Project Repository
https://github.com/t112370206/final_project_cycle/upload
## Presentation Video


## Research Question
Among U.S. high school students in the YRBS 2007 dataset, is BMI percentile associated with physical activity days after adjusting for computer use, sleep, sex, and age?

## Variables
- Outcome variable: `bmi_percentile` from `BMIPCT`.
- Main predictor: `physical_activity_days`, recoded from `PhysicalActivity5OrMoreDays`.
- Control variables: `computer_use_hours`, `sleep_hours`, `female`, and `age_years_approx`.

## Statistical Method
This project uses multiple linear regression because the outcome variable, BMI percentile, is numeric and the goal is to examine how several predictors are associated with it.

Model:

`BMI percentile = b0 + b1(activity days) + b2(computer use hours) + b3(sleep hours) + b4(female) + b5(age) + error`

## Key Results
- Sample size after cleaning: 11,287 students.
- R-squared: 0.008.
- Physical activity coefficient: -0.267 BMI percentile points per additional active day.
- p-value for physical activity: 0.0097.

## Interpretation
After adjusting for computer use, sleep, sex, and age, each additional physically active day was associated with about 0.27 lower BMI percentile points. The association was statistically significant in the unweighted OLS model, but the effect size was very small and the model explained little variation in BMI percentile.

## Repository Structure
```text
data/raw/YRBS_2007.csv
data/processed/yrbs_2007_cleaned_regression.csv
notebooks/yrbs_final_project.ipynb
outputs/figures/
outputs/tables/
summary/one_page_infographic_summary.png
report/final_project_report.docx
report/video_script_english.md
references/
```

## How to Run
1. Open `notebooks/yrbs_final_project.ipynb` in Jupyter Notebook.
2. Run all cells from top to bottom.
3. The notebook will reproduce the cleaned data, tables, figures, regression results, and one-page summary.

## Important Limitation
The YRBS dataset is a survey dataset. This project uses a simple regression workflow for course requirements and should be interpreted as association, not causation.
