# Students Performance Analysis

> Exploratory data analysis and statistical hypothesis testing of student academic performance using Python.

## Project Overview

This project analyzes the academic performance of 1,000 students
across Math, Reading, and Writing scores.

The analysis explores how performance varies across demographic
and educational factors and investigates whether completing a
test-preparation course is associated with higher overall scores.

## Objectives

- Understand the structure and quality of the dataset
- Explore student score distributions
- Compare performance across demographic groups
- Analyze the relationship between parental education and performance
- Investigate the impact of test-preparation participation
- Identify potential outliers
- Perform statistical hypothesis testing

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- SciPy
- Jupyter Notebook

## Analysis Workflow

Raw Data
↓
Data Understanding
↓
Data Quality Checks
↓
Feature Engineering
↓
Exploratory Data Analysis
↓
Outlier Analysis
↓
Hypothesis Testing
↓
Statistical Interpretation
↓
Key Findings

## Dataset

The dataset contains:

- 1,000 student records
- 8 original variables
- Math, Reading, and Writing scores
- Gender
- Race/Ethnicity
- Parental level of education
- Lunch type
- Test-preparation course status

## Key Analysis Areas

### Academic Performance

Analysis of score distributions across Math, Reading,
and Writing.

### Demographic Analysis

Comparison of performance across gender and race/ethnicity groups.

### Parental Education

Investigation of the relationship between parental education
and student performance.

### Test Preparation

Comparison of students who completed the test-preparation course
with those who did not.

### Outlier Analysis

Identification of unusually low or high total scores using
the IQR method.

## Hypothesis Testing

### Research Question

Do students who completed the test-preparation course have
a different mean total score from students who did not?

### Hypotheses

**H₀:** The mean total score is the same for both groups.

**H₁:** The mean total score differs between the two groups.

A Welch's t-test was used to compare the two independent groups.

### Result

The p-value was below the 0.05 significance level,
providing strong statistical evidence that the mean total
scores differ between students who completed the course
and those who did not.

> Statistical significance indicates an association between
> test preparation and score differences. It does not establish
> that the course itself caused the higher scores.

## Key Findings

- The dataset contains no missing values.
- Reading and Writing have higher average scores than Math.
- Students who completed the test-preparation course have a
  higher average total score.
- Welch's t-test indicates a statistically significant difference
  between the two groups.
- Female students perform better on average in Reading and Writing,
  while male students perform better in Math.
- The master's-degree parental education group has the highest
  average total score.
- Race/Ethnicity Group E has the highest average performance,
  while Group A has the lowest.
- A small number of unusually low total scores were identified
  using the IQR method.

## Limitations

- This is an observational dataset, so associations should not
  be interpreted as causal relationships.
- The hypothesis test compares group means without controlling
  for other variables.
- Outliers were retained because they may represent genuine
  observations.

## 🚀 How to Run

```bash
git clone https://github.com/YOUR_USERNAME/students-performance-analysis.git
cd students-performance-analysis
pip install -r requirements.txt
