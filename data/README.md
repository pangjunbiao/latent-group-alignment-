# Beijing Public Transport Carbon-Incentive Survey Dataset

## Overview

This dataset is derived from a real-world survey conducted in Beijing to study public transport preferences, behavioral intentions, and responses to carbon-incentive mechanisms. It is designed to support research on policy-guided behavioral change, especially the problem of shifting individuals or groups toward greener public transport choices under feasible and constrained interventions.

The survey contains responses from **1021 participants** and originally includes **40 raw fields**. After excluding non-analytic fields such as the respondent index and personal contact information, the dataset contains **38 substantive survey variables** used for analysis.

The variables cover behavioral intention, attitudinal beliefs, policy and reward preferences, incentive-response behavior, and demographic/contextual characteristics. This combination makes the dataset suitable for studying both **behavioral alignment** and **actionable intervention design**.

---

## Dataset Summary

| Property | Value |
|---|---:|
| Survey respondents | 1021 |
| Raw survey fields | 40 |
| Excluded non-analytic fields | 2 |
| Substantive survey variables | 38 |
| Model-ready features after preprocessing | 78 |
| Controllable candidate features | 32 |
| Survey domain | Public transport carbon-incentive behavior |
| Data source | Real-world Beijing survey |

---

## Survey Variable Groups

The 38 substantive variables are organized into four groups:

| Group | Count | Description |
|---|---:|---|
| Behavioral and attitudinal variables | 11 | Measures willingness to adopt public transport and attitudes toward carbon-incentive programs |
| Policy and incentive variables | 15 | Describes preferences for intervention mechanisms such as monetary rewards, health-related benefits, and environmental contributions |
| Reward-response variables | 4 | Captures stated behavioral reactions under different incentive levels |
| Demographic and contextual attributes | 8 | Includes socioeconomic and travel-context attributes such as occupation, income, and residential location |

Total substantive variables: **11 + 15 + 4 + 8 = 38**

---

## Variable Categories

### 1. Behavioral and Attitudinal Variables (11)

These variables measure the respondent’s beliefs, willingness, and attitudes toward public transport and carbon-incentive schemes. They include perceived economic value, health benefits, environmental contribution, social influence, convenience, comfort, and willingness to increase public transport usage.

These variables are primarily represented as **ordered categorical / Likert-type responses**.

---

### 2. Policy and Incentive Variables (15)

These variables capture preferences regarding specific policy levers and incentive mechanisms. Examples include preferences for converting carbon points into consumer discounts, transport benefits, health services, insurance discounts, ecological programs, donation mechanisms, and collaborative reward systems.

In the modeling pipeline, these variables are especially important because they form the main pool of **actionable policy-related candidate intervention variables**.

---

### 3. Reward-Response Variables (4)

These variables record how long respondents would be willing to continue using public transport under different carbon-incentive reward levels. They reflect stated behavioral responses under incremental reward amounts rather than general opinions alone.

These variables provide direct evidence of **incentive sensitivity** and are useful for analyzing how behavioral commitment changes with reward magnitude.

---

### 4. Demographic and Contextual Attributes (8)

These variables describe background and contextual characteristics such as occupation, education, income, vehicle ownership, and residential/travel-related location information.

These attributes are useful for segmentation, group analysis, and feasibility-aware intervention design. In the modeling framework, many of these variables are treated as **fixed or non-intervenable attributes**.

---

## Data Types

The dataset contains mixed-type survey variables, including:

- **Ordered categorical variables**  
  Example: Likert-scale agreement levels

- **Nominal categorical variables**  
  Example: occupation, district, or category-based attributes

- **Binary variables**  
  Example: yes/no style attributes such as ownership indicators

- **Numeric or count-like variables**  
  Example: certain quantitative survey responses where applicable

This mixed-type structure is one of the main motivations for the preprocessing and representation-learning pipeline used in the project.

---

## Excluded Fields

Two raw fields are excluded from analysis:

1. **Respondent index / serial number**
2. **Personal phone number field**

These fields are non-analytic and are removed before preprocessing and modeling.

---

## Preprocessing Summary

The raw survey responses are transformed into a model-ready representation through preprocessing steps that include:

1. removal of non-analytic and private fields,
2. cleaning and standardization of survey responses,
3. encoding of ordered categorical variables,
4. one-hot encoding of nominal categorical variables where needed,
5. construction of a nonnegative feature matrix for downstream representation learning.

After preprocessing, the dataset is converted from **38 substantive survey variables** into **78 model-ready features**.
