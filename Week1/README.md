# Advanced Data Science — First Class Project README

## Project Title

**Ames Housing Dataset — Reproducible Foundations for Advanced Data Science**

---

## Project Description (Background, Motivation, Objectives)

This project marks the first session of an Advanced Data Science course using the Ames Housing dataset as the main case study. The course establishes three core principles:

* Every claim must be reproducible.
* Every missing value must be explained, not simply imputed.

The Ames dataset is widely used for predictive modeling because it contains detailed information about residential property sales. It provides an excellent opportunity to practice reproducible workflows, structured reporting, and rigorous exploratory data analysis.

### Objectives

* Establish a reproducible project structure.
* Document dataset provenance and unit of analysis.
* Define target variables for future modeling:

  * Numeric target: **SalePrice** (house sale price).
  * Derived categorical target: **Price Tier** (quantile-based classification for later supervised learning).
* Perform initial exploratory checks to understand data quality and structure.

---

## Installation Instructions

### 1. Create a project environment

```bash
pip install -r requirements.txt
```
The file requirements.txt is included in the project repository and lists all necessary libraries.

---

## Data Source and Data Structure

### Data Source

The Ames Housing dataset originates from property sales recorded in Ames, Iowa (USA). It is commonly distributed via:

* Kaggle housing price competitions([link](https://www.kaggle.com/datasets/marcopale/housing))
* Academic machine learning repositories
* Course-provided datasets

Dataset provenance must always be explicitly documented to ensure reproducibility.

### Unit of Analysis

Each row represents a single residential property sale.

### Data Structure Overview

* Format: CSV
* Observations: 2930
* Features: 82 explanatory

---

## Initial Check of the Data

Initial exploration should focus on understanding the dataset before any modeling:

### Typical checks include:

* Data types of each variable
* Missing value counts and patterns
* Summary statistics (mean, median, spread)
* Distribution plots of SalePrice and key predictors

Key guiding principle: missing values should be interpreted, not blindly filled.

Example exploratory steps:

* Inspect SalePrice distribution (skewness is expected).
* Identify variables with substantial missingness (e.g., Alley, PoolQC).
* Verify consistency between related variables (e.g., garage attributes).

---

## Summary Table

Below is a summary table of all variables in the dataset, including counts, missing value percentages, unique value counts for categorical variables, means for numerical variables, and data types. This table serves as a reference for understanding the dataset's structure and guiding subsequent analysis.

**Table 1 — Summary of Ames Housing Dataset Variables**

| Variable | Num of Values | % of Missing Values | Unique Values (Categorical) | Mean (Numerical) | Python Type | float | int | str |
|----------|--------------|---------------------|-----------------------------|------------------|-------------|-------|-----|-----|
| 1st Flr SF | 2930 | 0.000000 | NaN | 1159.557679 | int64 | NaN | 100.0 | NaN |
| 2nd Flr SF | 2930 | 0.000000 | NaN | 335.455973 | int64 | NaN | 100.0 | NaN |
| 3Ssn Porch | 2930 | 0.000000 | NaN | 2.592491 | int64 | NaN | 100.0 | NaN |
| Alley | 198 | 93.242321 | 2.0 | NaN | str | 93.242321 | NaN | 6.757679 |
| Bedroom AbvGr | 2930 | 0.000000 | NaN | 2.854266 | int64 | NaN | 100.0 | NaN |
| Bldg Type | 2930 | 0.000000 | 5.0 | NaN | str | NaN | NaN | 100.000000 |
| Bsmt Cond | 2850 | 2.730375 | 5.0 | NaN | str | 2.730375 | NaN | 97.269625 |
| Bsmt Exposure | 2847 | 2.832765 | 4.0 | NaN | str | 2.832765 | NaN | 97.167235 |
| Bsmt Full Bath | 2928 | 0.068259 | NaN | 0.431352 | float64 | 100.000000 | NaN | NaN |
| Bsmt Half Bath | 2928 | 0.068259 | NaN | 0.061134 | float64 | 100.000000 | NaN | NaN |
| Bsmt Qual | 2850 | 2.730375 | 5.0 | NaN | str | 2.730375 | NaN | 97.269625 |
| Bsmt Unf SF | 2929 | 0.034130 | NaN | 559.262547 | float64 | 100.000000 | NaN | NaN |
| BsmtFin SF 1 | 2929 | 0.034130 | NaN | 442.629566 | float64 | 100.000000 | NaN | NaN |
| BsmtFin SF 2 | 2929 | 0.034130 | NaN | 49.722431 | float64 | 100.000000 | NaN | NaN |
| BsmtFin Type 1 | 2850 | 2.730375 | 6.0 | NaN | str | 2.730375 | NaN | 97.269625 |
| BsmtFin Type 2 | 2849 | 2.764505 | 6.0 | NaN | str | 2.764505 | NaN | 97.235495 |
| Central Air | 2930 | 0.000000 | 2.0 | NaN | str | NaN | NaN | 100.000000 |
| Condition 1 | 2930 | 0.000000 | 9.0 | NaN | str | NaN | NaN | 100.000000 |
| Condition 2 | 2930 | 0.000000 | 8.0 | NaN | str | NaN | NaN | 100.000000 |
| Electrical | 2929 | 0.034130 | 5.0 | NaN | str | 0.034130 | NaN | 99.965870 |
| Enclosed Porch | 2930 | 0.000000 | NaN | 23.011604 | int64 | NaN | 100.0 | NaN |
| Exter Cond | 2930 | 0.000000 | 5.0 | NaN | str | NaN | NaN | 100.000000 |
| Exter Qual | 2930 | 0.000000 | 4.0 | NaN | str | NaN | NaN | 100.000000 |
| Exterior 1st | 2930 | 0.000000 | 16.0 | NaN | str | NaN | NaN | 100.000000 |
| Exterior 2nd | 2930 | 0.000000 | 17.0 | NaN | str | NaN | NaN | 100.000000 |
| Fence | 572 | 80.477816 | 4.0 | NaN | str | 80.477816 | NaN | 19.522184 |
| Fireplace Qu | 1508 | 48.532423 | 5.0 | NaN | str | 48.532423 | NaN | 51.467577 |
| Fireplaces | 2930 | 0.000000 | NaN | 0.599317 | int64 | NaN | 100.0 | NaN |
| Foundation | 2930 | 0.000000 | 6.0 | NaN | str | NaN | NaN | 100.000000 |
| Full Bath | 2930 | 0.000000 | NaN | 1.566553 | int64 | NaN | 100.0 | NaN |
| Functional | 2930 | 0.000000 | 8.0 | NaN | str | NaN | NaN | 100.000000 |
| Garage Area | 2929 | 0.034130 | NaN | 472.819734 | float64 | 100.000000 | NaN | NaN |
| Garage Cars | 2929 | 0.034130 | NaN | 1.766815 | float64 | 100.000000 | NaN | NaN |
| Garage Cond | 2771 | 5.426621 | 5.0 | NaN | str | 5.426621 | NaN | 94.573379 |
| Garage Finish | 2771 | 5.426621 | 3.0 | NaN | str | 5.426621 | NaN | 94.573379 |
| Garage Qual | 2771 | 5.426621 | 5.0 | NaN | str | 5.426621 | NaN | 94.573379 |
| Garage Type | 2773 | 5.358362 | 6.0 | NaN | str | 5.358362 | NaN | 94.641638 |
| Garage Yr Blt | 2771 | 5.426621 | NaN | 1978.132443 | float64 | 100.000000 | NaN | NaN |
| Gr Liv Area | 2930 | 0.000000 | NaN | 1499.690444 | int64 | NaN | 100.0 | NaN |
| Half Bath | 2930 | 0.000000 | NaN | 0.379522 | int64 | NaN | 100.0 | NaN |
| Heating | 2930 | 0.000000 | 6.0 | NaN | str | NaN | NaN | 100.0 |
| Heating QC | 2930 | 0.000000 | 5.0 | NaN | str | NaN | NaN | 100.0 |
| House Style | 2930 | 0.000000 | 8.0 | NaN | str | NaN | NaN | 100.0 |
| Kitchen AbvGr | 2930 | 0.000000 | NaN | 1.044369 | int64 | NaN | 100.0 | NaN |
| Kitchen Qual | 2930 | 0.000000 | 5.0 | NaN | str | NaN | NaN | 100.0 |
| Land Contour | 2930 | 0.000000 | 4.0 | NaN | str | NaN | NaN | 100.0 |
| Land Slope | 2930 | 0.000000 | 3.0 | NaN | str | NaN | NaN | 100.0 |
| Lot Area | 2930 | 0.000000 | NaN | 10147.921843 | int64 | NaN | 100.0 | NaN |
| Lot Config | 2930 | 0.000000 | 5.0 | NaN | str | NaN | NaN | 100.0 |
| Lot Frontage | 2440 | 16.723549 | NaN | 69.224590 | float64 | 100.0 | NaN | NaN |
| Lot Shape | 2930 | 0.000000 | 4.0 | NaN | str | NaN | NaN | 100.000000 |
| Low Qual Fin SF | 2930 | 0.000000 | NaN | 4.676792 | int64 | NaN | 100.0 | NaN |
| MS SubClass | 2930 | 0.000000 | NaN | 57.387372 | int64 | NaN | 100.0 | NaN |
| MS Zoning | 2930 | 0.000000 | 7.0 | NaN | str | NaN | NaN | 100.000000 |
| Mas Vnr Area | 2907 | 0.784983 | NaN | 101.896801 | float64 | 100.000000 | NaN | NaN |
| Mas Vnr Type | 1155 | 60.580205 | 4.0 | NaN | str | 60.580205 | NaN | 39.419795 |
| Misc Feature | 106 | 96.382253 | 5.0 | NaN | str | 96.382253 | NaN | 3.617747 |
| Misc Val | 2930 | 0.000000 | NaN | 50.635154 | int64 | NaN | 100.0 | NaN |
| Mo Sold | 2930 | 0.000000 | NaN | 6.216041 | int64 | NaN | 100.0 | NaN |
| Neighborhood | 2930 | 0.000000 | 28.0 | NaN | str | NaN | NaN | 100.000000 |
| Open Porch SF | 2930 | 0.000000 | NaN | 47.53345 | int64 | NaN | 100.0 | NaN |
| Order | 2930 | 0.000000 | NaN | 1465.500 | int64 | NaN | 100.0 | NaN |
| Overall Cond | 2930 | 0.000000 | NaN | 5.563140 | int64 | NaN | 100.0 | NaN |
| Overall Qual | 2930 | 0.000000 | NaN | 6.094881 | int64 | NaN | 100.0 | NaN |
| PID | 2930 | 0.000000 | NaN | 7.144645e+08 | int64 | NaN | 100.0 | NaN |
| Paved Drive | 2930 | 0.000000 | 3.0 | NaN | str | NaN | NaN | 100.000000 |
| Pool Area | 2930 | 0.000000 | NaN | 2.243345 | int64 | NaN | 100.0 | NaN |
| Pool QC | 13 | 99.556314 | 4.0 | NaN | str | 99.556314 | NaN | 0.443686 |
| Roof Matl | 2930 | 0.000000 | 8.0 | NaN | str | NaN | NaN | 100.000000 |
| Roof Style | 2930 | 0.000000 | 6.0 | NaN | str | NaN | NaN | 100.000000 |
| Sale Condition | 2930 | 0.00000 | 6.0 | NaN | str | NaN | NaN | 100.0 |
| Sale Type | 2930 | 0.00000 | 10.0 | NaN | str | NaN | NaN | 100.0 |
| SalePrice | 2930 | 0.00000 | NaN | 180796.060068 | int64 | NaN | 100.0 | NaN |
| Screen Porch | 2930 | 0.00000 | NaN | 16.002048 | int64 | NaN | 100.0 | NaN |
| Street | 2930 | 0.00000 | 2.0 | NaN | str | NaN | NaN | 100.0 |
| TotRms AbvGrd | 2930 | 0.00000 | NaN | 6.443003 | int64 | NaN | 100.0 | NaN |
| Total Bsmt SF | 2929 | 0.03413 | NaN | 1051.614544 | float64 | 100.0 | NaN | NaN |
| Utilities | 2930 | 0.00000 | 3.0 | NaN | str | NaN | NaN | 100.0 |
| Wood Deck SF | 2930 | 0.00000 | NaN | 93.751877 | int64 | NaN | 100.0 | NaN |
| Year Built | 2930 | 0.00000 | NaN | 1971.356314 | int64 | NaN | 100.0 | NaN |
| Year Remod/Add | 2930 | 0.0 | NaN | 1984.266553 | int64 | NaN | 100.0 | NaN |
| Yr Sold | 2930 | 0.0 | NaN | 2007.790444 | int64 | NaN | 100.0 | NaN |

### Caption
Explaining all columns in table 1:
- **Variable**: Name of the feature or target variable.
- **Num of Values**: Total count of non-missing entries for the variable.
- **% of Missing Values**: Percentage of entries that are missing for the variable.
- **Unique Values (Categorical)**: Number of unique categories for categorical variables.
- **Mean (Numerical)**: Average value for numerical variables.
- **Python Type**: Data type of the variable in Python (e.g., int64, float64, str).
- **float**: Percentage of entries that are of type float.
- **int**: Percentage of entries that are of type int.
- **str**: Percentage of entries that are of type string.

The code to generate this table is included in [notebook](https://github.com/zuilpirola/AdvandedDS/tree/main/Week1/notebooks) and is designed to be reproducible, following the course's principles.

---

## Initial Analysis

Several preliminary insights can be drawn:

1. Order vs PID identifiers
Both Order and PID act as unique identifiers for properties, but they may serve different purposes. Order likely represents a sequential index, while PID may be a more complex property identifier containing additional information such as location or classification. Dataset documentation is needed for confirmation.

2. Lot Frontage meaning
Lot Frontage represents the linear feet of street connected to the property. It is a numerical variable describing how much street exposure a property has.

3. Lot Area interpretation
Lot Area measures the total lot size in square feet. This numerical feature reflects property land size and can influence valuation.

4. Street access types
The Street variable indicates the type of road access to a property. The dataset typically includes Grvl (gravel road access) and Pave (paved road access).

5. Alley access categories
Similar to street access, Alley describes alley access type. Values like Grvl and Pave indicate gravel or paved alleys, while missing values often represent no alley access.

6. Difference between Street and Alley
Street refers to the primary road access to the property, whereas Alley describes secondary rear or side access. While street access usually has fewer categories, alley access may include an explicit absence (NA).

8. Missing value patterns
Several variables exhibit significant missingness (e.g., Alley, Pool QC, Fence). Understanding the reasons for missing values is crucial. For instance, missing Pool QC likely indicates no pool, while missing Alley may indicate no alley access. These patterns must be documented and interpreted rather than simply imputed.

...

---

## Next Steps

* Complete exploratory data analysis with reproducible notebooks.
* Document missing-value mechanisms.
* Validate assumptions visually and statistically.
* Begin feature engineering and baseline modeling.

---

This README represents the first stage of a reproducible advanced data science workflow using the Ames Housing dataset.
