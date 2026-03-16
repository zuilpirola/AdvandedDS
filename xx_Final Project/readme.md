# Final Project — Exploratory Data Analysis, Regression and PCA

## Overview

In this project you will conduct a **complete exploratory data analysis (EDA)** of a dataset, design and evaluate a **regression approach**, and assess the **viability and consequences of applying Principal Component Analysis (PCA)**.

The objective is not simply to build a predictive model, but to demonstrate **analytical discipline**:

- every claim must be **reproducible**
- every plot must answer a **question**
- every missing value must be **explained**, not blindly imputed
- modelling decisions must be **justified**

The final deliverable is a **structured analytical report**, similar to the early chapters of a thesis or a professional data science report.

---

# Dataset Selection

Students must select a dataset from one of the following repositories:

- https://huggingface.co/datasets  
- https://www.kaggle.com/datasets  

### Dataset Requirements

The dataset must:

- contain **at least one numeric variable suitable as a regression target**
- contain **multiple predictor variables**
- include **both numeric and categorical variables**
- have **non-trivial structure** (with missing values, correlations, heterogeneous variables, etc.)

Avoid datasets that are:

- extremely small (<500 rows)
- extremely large (>10,000 rows)
- already heavily preprocessed
- purely image/text datasets without structured tabular features

---

# Reproducibility Requirements

Your project must be **fully reproducible**.

Minimum repository structure:
```
# ames-project/
# │
# ├── data/
# │   ├── raw/
# │   └── processed/
# │
# ├── notebooks/
# ├── src/
# ├── reports/
# │   └── figures/
# │
# ├── README.md
# ├── requirements.txt
# └── .gitignore
```


The repository must allow someone to reproduce the analysis starting from the raw dataset.

---

# Report Structure

Your report should follow the structure below.

The goal is **clarity of reasoning**, not volume.

---

# 1. Dataset Description

Explain the dataset as a **case**, not as a file.

Include:

- dataset source
- dataset purpose or origin
- unit of analysis
- number of observations
- number of variables
- description of the **target variable**

Discuss:

- what kinds of claims the dataset allows
- known limitations of the data
- potential biases or sampling issues

---

# 2. Variable Dictionary and Measurement Types

Construct a **variable table** that classifies each variable.

Example format:

| Variable | Data Type | Measurement Level | Description |
|--------|--------|--------|--------|
| Age | numeric | ratio | age of individual |
| Education | categorical | ordinal | education level |

Discuss:

- nominal vs ordinal vs continuous variables
- variables with ambiguous interpretation
- variables that may require transformation or recoding

Explain why **variable type is an analytical decision**, not simply metadata.

---

# 3. Missing Data Analysis

Quantify and analyse missingness.

Include:

- percentage of missing values per variable
- missingness patterns
- possible interpretations of missing data

Discuss:

- possible mechanisms (**MCAR**, **MAR**, **MNAR**) as **hypotheses**
- variables where missingness may have **semantic meaning**

Define a **missing data strategy**:

- imputation
- indicator variables
- removal
- domain-based interpretation

All decisions must be **explicitly justified**.

---

# 4. Univariate Analysis

Analyse the distribution of each variable.

For numeric variables include:

- distribution plots
- skewness and outliers
- robust statistics (median, IQR)

For categorical variables include:

- cardinality
- frequency distributions
- rare levels

Discuss:

- potential transformations
- variables with problematic distributions

---

# 5. Association and Dependence

Explore relationships between variables.

Use appropriate methods depending on variable type:

- numeric → numeric (correlation)
- categorical → numeric
- categorical → categorical

Discuss:

- meaningful associations with the target
- potential **multicollinearity**
- interpretation limits of correlation

---

# 6. Regression Modelling Strategy

Define a **regression task** using the selected target variable.

Describe:

- modelling objective
- train/validation/test split strategy
- evaluation metrics

Typical regression metrics include:

- MAE
- RMSE
- R²

Explain **why the chosen metrics are appropriate**.

---

# 7. Baseline Model

Implement a **baseline regression model**.

Examples include:

- linear regression
- regularised regression (Ridge/Lasso)

Document:

- preprocessing pipeline
- encoding strategies
- scaling decisions
- missing data handling

Report:

- model performance
- residual diagnostics
- error analysis

---

# 8. PCA Analysis

Investigate whether **Principal Component Analysis (PCA)** is appropriate for the dataset.

Include:

- variables selected for PCA
- standardisation decisions
- explained variance analysis
- number of components selected

Discuss:

- what structure PCA reveals
- interpretability of components
- limitations of PCA in this dataset

---

# 9. Regression with PCA Features

Evaluate whether PCA improves the modelling pipeline.

Compare models using:

- baseline features
- PCA-transformed features

Report:

- performance differences
- model stability
- interpretability trade-offs

Present results in a **comparison table**.

---

# 10. Error Analysis and Limitations

Discuss:

- where the model performs poorly
- possible sources of error
- dataset limitations
- modelling assumptions

This section should read like something a **professional reviewer could trust**.

---

# 11. Reproducibility Statement

Explain how someone can reproduce the analysis.

Include:

- software used
- library versions
- instructions to run the analysis

Example:
```
pip install -r requirements.txt
```


---

# Evaluation Criteria

Your project will be evaluated based on the following dimensions:

| Criterion | Description |
|------|------|
| Analytical discipline | Justified decisions and clear reasoning |
| Data understanding | Quality of EDA and dataset interpretation |
| Modelling clarity | Well-defined regression strategy |
| PCA analysis | Correct and thoughtful application |
| Reproducibility | Ability to reproduce results |
| Communication | Clear and structured report |

---

# Final Deliverables

Students must submit:

- a **Git repository** containing the full project
- a **final report** (PDF or Markdown)
- **reproducible code** used to generate the analysis

All figures and results in the report must be reproducible from the repository.