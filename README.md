# AnalystLAB-Internship
# Airbnb Market Intelligence Case Study

## Project Overview

This project explores Airbnb market data to investigate how advertised listing prices vary across different cities, room types and property characteristics.

The analysis also examines host characteristics, listing ratings and review activity to identify patterns that may support market intelligence and data-driven decision-making.

The project was completed as part of the **Data Science AnalystLAB Internship**, using Python and Databricks.

## Research Problem

How do advertised Airbnb listing prices vary across different cities, room types and accommodation characteristics, and what factors are associated with these price differences?

## Project Objectives

- Analyse Airbnb listing distributions across different cities.
- Investigate advertised prices across cities, room types and property types.
- Explore relationships between accommodation capacity and listing prices.
- Examine host characteristics and performance indicators.
- Investigate listing ratings and review activity.
- Apply statistical hypothesis testing.
- Develop a machine learning model to estimate advertised listing prices.
- Create an interactive Airbnb Market Intelligence Dashboard.

## Datasets

Two datasets were used:

**1. Listings Dataset**

Contains information about:
- Listing and host identifiers.
- Host response and acceptance rates.
- City and neighbourhood.
- Property and room types.
- Accommodation capacity.
- Advertised prices.
- Minimum and maximum nights.
- Listing review scores.

**2. Reviews Dataset**

Contains:
- `listing_id`
- `review_id`
- `date`
- `reviewer_id`

The Reviews dataset contained 10,000 records and was used to investigate review activity and review frequency.

## Tools and Technologies

- Python
- Pandas
- Matplotlib
- SciPy
- Scikit-learn
- Databricks
- Databricks AI/BI Dashboards

## Methodology

The project followed these analytical stages:

### 1. Data Cleaning and Preparation
- Inspected dataset structures and data types.
- Handled missing and inconsistent values.
- Converted price and numerical fields into appropriate formats.
- Converted review dates into datetime format.
- Checked duplicate records and review identifiers.
- Prepared both datasets for analysis.

### 2. Exploratory Data Analysis (EDA)
- Analysed listing distributions across ten cities.
- Compared advertised prices across cities.
- Examined room type and property type distributions.
- Investigated accommodation capacity and prices.
- Explored host characteristics and listing ratings.
- Analysed review frequency and date distributions.

### 3. Statistical Analysis and Hypothesis Testing

Three hypotheses were investigated:

1. Whether advertised prices differ across room types.
2. Whether accommodation capacity is associated with advertised prices.
3. Whether listing ratings differ across room types.

Methods included:
- Kruskal-Wallis H-test.
- Mann-Whitney U-test.
- Holm correction.
- Spearman rank correlation.
- Effect size analysis.

### 4. Predictive Modelling

A Random Forest Regression model was developed to estimate advertised listing prices using listing characteristics.

**Model performance:**

| Metric | Result |
|---|---:|
| MAE | 166.56 |
| RMSE | 362.88 |
| R² | 0.4647 |

The model explained approximately 46.47% of the variation in advertised listing prices on the test dataset.

### 5. Reviews Analysis and Dataset Integration

The Reviews dataset was analysed to identify:
- Review frequency per listing.
- Most-reviewed listings.
- Review date distributions.
- Unique listing and review identifiers.

Both datasets were linked using `listing_id`.

A total of 42 listing IDs matched between the two datasets, and all matched listings were from Paris.

### 6. Dashboard Development

An Airbnb Market Intelligence Dashboard was developed using Databricks AI/BI Dashboards.

The dashboard presents:
- Listing distribution by city.
- Average and median advertised prices.
- Listing distribution by room type.
- Property type analysis.
- Top 10 most-reviewed listings.
- Price prediction model performance.

## Key Findings

- Listing distribution varied considerably across the ten cities.
- Advertised prices differed across room types in Cape Town, with a statistically significant Kruskal-Wallis result.
- Accommodation capacity had a weak positive association with advertised prices in Cape Town (Spearman correlation: 0.1685).
- Listing ratings differed overall across room types, although pairwise comparisons were not significant after correction.
- Review activity was unevenly distributed, with most listings having only one recorded review in the available sample.
- The Random Forest model demonstrated moderate explanatory performance, with an R² of 0.4647.

## Project Limitations

- Currency information was not confirmed, limiting direct price comparisons across cities.
- The number of listings varied significantly between cities.
- Only 42 listing IDs matched between Listings and Reviews, all from Paris.
- Some listing attributes contained missing values.
- Extreme advertised prices could influence average price calculations.
- Review activity does not represent actual bookings, occupancy or revenue.
- The predictive model's performance indicates that additional features and model improvements may be required.

## Project Deliverables

- Cleaned Listings dataset.
- Cleaned Reviews dataset.
- Listings analysis notebook.
- Reviews analysis notebook.
- Exploratory data analysis and visualisations.
- Statistical hypothesis testing.
- Random Forest regression model.
- Airbnb Market Intelligence Dashboard.
- Analytical report and data dictionaries.

## Conclusion

This case study demonstrates the application of data science techniques to an Airbnb market intelligence problem.

Through data cleaning, exploratory analysis, statistical testing, predictive modelling and dashboard development, the project transformed raw listing and review data into structured analytical insights.

The project also highlighted the importance of data quality, careful interpretation of statistical results and transparent communication of analytical limitations.

---

**Project:** Airbnb Market Intelligence Case Study  
**Programme:** Data Science AnalystLAB Internship  
