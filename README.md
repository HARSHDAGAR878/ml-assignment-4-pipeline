ML Assignment 4 — End-to-End Data Pipeline
**NYC Airbnb Open Data — AB_NYC_2019.csv**

* Rows: 48,895
* Columns: 16
* Source: [NYC Airbnb Open Data](https://raw.githubusercontent.com/MainakRepositor/Datasets/master/AB_NYC_2019.csv)

The dataset contains numerical, categorical, text, and date-related data with genuine missing values.

Assignment

This project performs an end-to-end data preparation pipeline:
Raw Data → Cleaning → Feature Engineering → Preprocessing → Model-Ready Matrix

No machine learning model is trained in this assignment.

Features Added
1. `availability_rate` — converts annual availability into a proportion.
2. `minimum_stay_cost` — estimates the minimum total booking cost.
3. `reviews_per_year` — converts monthly reviews into yearly reviews.
4. `host_listing_ratio` — relates host listing count to review activity.

Before vs After

| Stage |                Rows |             Columns | Missing Values | Duplicates |
| ----- | ------------------: | ------------------: | -------------: | ---------: |
| Raw   |              48,895 |                  16 |         20,141 |          0 |
| Final | See notebook output | See notebook output |              0 |          0 |

Data Quality
The raw dataset contained:

* 20,141 missing values
* 0 duplicate rows
* 0 negative prices
* 0 invalid minimum-night values
* 0 invalid availability values
* 0 invalid category labels

Missing numerical and categorical values were handled using appropriate imputation methods. Categorical variables were one-hot encoded and numerical variables were standardized.

Files
* `assignment4_endtoend.ipynb` — Complete notebook
* `cleaned_data.csv` — Cleaned dataset
* `pipeline.joblib` — Fitted preprocessing pipeline
* `README.md` — Project information

Limitations
Some issues still remain, such as extreme prices and very high minimum-stay values. Missing review dates also cannot be recovered accurately. These limitations could not be fixed without making assumptions about the original data.
