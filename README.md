# ANOVA Case Study on Titanic Dataset

## Overview

This repository contains a statistical case study using One-Way ANOVA (Analysis of Variance) on the Titanic dataset. The objective of this project is to examine whether the average age of passengers differs significantly across passenger classes (Pclass 1, 2, and 3).

The project follows a structured statistical workflow that includes data preparation, exploratory analysis, hypothesis testing, post-hoc comparisons, assumption checking, and effect size measurement. In addition to identifying whether a significant difference exists, the analysis also investigates which groups differ and how strong the effect is.

This project is intended as a practical application of inferential statistics using Python.

---

## Problem Statement

The main question addressed in this case study is:

Do passengers from different travel classes have significantly different average ages?

Since passenger class consists of multiple groups and age is a continuous variable, One-Way ANOVA is used to test for differences in group means.

---

## Objectives

The analysis aims to:

- Compare mean passenger age across travel classes.
- Test whether observed differences are statistically significant.
- Check whether ANOVA assumptions hold.
- Identify which specific class pairs differ using post-hoc tests.
- Measure the magnitude of the relationship using effect size.
- Support findings using statistical visualization.

---

## Dataset

This project uses the Titanic dataset.

### Variables Used

**Independent Variable (Factor)**  
- Pclass (Passenger Class)

**Dependent Variable (Response)**  
- Age

### Passenger Classes

- Class 1
- Class 2
- Class 3

---

## Methodology

The project follows the workflow below:

### 1. Exploratory Data Analysis

A boxplot is used to visually compare age distributions across passenger classes.

This helps identify:

- Differences in medians
- Spread of observations
- Potential outliers
- Initial patterns before testing

---

### 2. Assumption Checks

Before ANOVA, assumptions are checked.

#### Normality Test

Shapiro-Wilk test is used to assess whether age within each class is approximately normally distributed.

**Null Hypothesis:** Data is normally distributed.

---

#### Homogeneity of Variance

Levene’s Test is used to check whether group variances are equal.

**Null Hypothesis:** Variances are equal.

---

## 3. One-Way ANOVA

One-Way ANOVA is performed to test whether mean age differs across classes.

### Null Hypothesis (H0)

Mean ages are equal across all classes.

μ1 = μ2 = μ3

---

### Alternative Hypothesis (H1)

At least one group mean is different.

---

### Decision Rule

If p-value < 0.05

Reject the null hypothesis.

---

## 4. Post-Hoc Analysis

Since ANOVA only shows whether a difference exists overall, additional pairwise tests are performed.

### Pairwise Comparisons

- Class 1 vs Class 2  
- Class 1 vs Class 3  
- Class 2 vs Class 3

---

### Methods Used

#### Bonferroni Pairwise t-tests

Bonferroni correction is applied to control false positives caused by multiple testing.

Adjusted significance level:

0.05 / 3 = 0.0167

---

#### Tukey’s HSD Test

Tukey’s Honest Significant Difference test is used to identify which group pairs differ significantly.

---

## Analysis Workflow

The notebook follows this sequence:

1. Import libraries  
2. Load and clean data  
3. Visualize age distribution using boxplot  
4. Check normality assumption  
5. Check equal variance assumption  
6. Run One-Way ANOVA  
7. Perform post-hoc tests  
8. Compute effect size  
9. Interpret results  
10. Draw conclusions

---

## Key Findings

The analysis shows:

- Passenger age differs significantly across travel classes.
- Class 1 has significant age differences compared to Class 2.
- Class 1 has significant age differences compared to Class 3.
- Class 2 and Class 3 do not show significant differences.
- Passenger class explains part of the variation in age.

These findings suggest passenger class is associated with age differences.

---

## How to Run This Project

### Clone Repository

```bash
git clone https://github.com/your-username/repository-name.git
```

---

### Install Dependencies

```bash
pip install pandas numpy scipy statsmodels matplotlib seaborn
```

---

### Run Notebook

Open Jupyter Notebook or Google Colab and run:

```bash
Anova_Case_Study.ipynb
```

Run all cells in sequence.

---

This case study demonstrates more than just running an ANOVA test.

It shows a complete statistical workflow:

- Checking assumptions  
- Running the main test  
- Investigating significant differences  
- Measuring practical importance  
- Interpreting results correctly

This makes the project useful for learning inferential statistics as well as building analytical project experience.

---

## Conclusion

This project applies One-Way ANOVA to study whether passenger age varies across travel classes in the Titanic dataset.

Results show statistically significant differences in mean age across classes, particularly involving Class 1. Post-hoc analysis identifies where those differences occur, and effect size helps evaluate the strength of the relationship.

The project provides a practical example of using statistical methods to move from raw data to meaningful insights.

---

## Author

Saurabh Tripathi
