# Students Performance in Exams — Exploratory Data Analysis

An exploratory data analysis (EDA) and statistical analysis project investigating factors associated with students' academic performance using the **Students Performance in Exams** dataset.

> **Main question:** Is completing a test-preparation course associated with higher total exam scores?

## 📌 Project Overview

This project analyzes student performance across **Math, Reading, and Writing** scores. It combines data-quality checks, feature engineering, exploratory visualization, outlier detection, and statistical hypothesis testing.

The analysis is based on **1,000 student records** and **8 original variables**.

## 🎯 Objectives

The notebook investigates:

- The overall distribution of student scores
- Performance differences by gender
- Performance differences across race/ethnicity groups
- The relationship between parental education and performance
- Differences between students who completed the test-preparation course and those who did not
- Whether the difference in total scores is statistically significant
- Potential outliers in total scores

## 🗂️ Dataset

The dataset contains the following original variables:

| Variable | Description |
|---|---|
| `gender` | Student gender |
| `race/ethnicity` | Race/ethnicity group |
| `parental level of education` | Highest parental education level |
| `lunch` | Lunch program/category |
| `test preparation course` | Whether the preparation course was completed |
| `math score` | Math exam score |
| `reading score` | Reading exam score |
| `writing score` | Writing exam score |

### Data Quality

- **Rows:** 1,000
- **Original columns:** 8
- **Missing values:** 0
- **Duplicate rows:** 0
- Score variables range from **0 to 100**

## ⚙️ Feature Engineering

Two additional features are created:

- **`average score`** — mean of Math, Reading, and Writing scores
- **`total score`** — sum of Math, Reading, and Writing scores

## 🔬 Analysis Workflow

1. Setup and data loading
2. Data understanding and quality checks
3. Feature engineering
4. Exploratory data analysis
   - Test-preparation participation
   - Overall score distribution
   - Parental education
   - Gender
   - Race/ethnicity
5. Outlier analysis
6. Hypothesis testing
7. Key findings and conclusion

## 📊 Key Findings

### Test Preparation

- **358 students** completed the preparation course.
- **642 students** did not complete it.
- Students who completed the course had a higher average total score.

### Overall Performance

The average scores in the dataset are:

| Subject | Mean Score |
|---|---:|
| Math | 66.09 |
| Reading | 69.17 |
| Writing | 68.05 |

Reading has the highest average score among the three subjects.

### Gender

- Female students have higher average **Reading** and **Writing** scores.
- Male students have a higher average **Math** score.
- The female group has the higher overall average performance.

### Parental Education

Students whose parents have a **master's degree** have the highest average total score, while the **high-school** parental-education group has the lowest average in this dataset.

### Race/Ethnicity

- **Group E** has the highest average performance across Math, Reading, and Writing.
- **Group A** has the lowest averages among the five groups.

## 🧪 Hypothesis Testing

The project uses an **independent two-sample Welch's t-test** to compare total scores between students who completed the preparation course and those who did not.

### Hypotheses

**H₀:** The mean total score is the same for both groups.

**H₁:** The mean total score differs between the two groups.

### Results

| Group | Mean Total Score |
|---|---:|
| Completed preparation | 218.01 |
| Did not complete | 195.12 |

- **t-statistic:** 8.5945
- **p-value:** 4.4267 × 10⁻¹⁷
- **Significance level:** 0.05

Because the p-value is far below 0.05, the analysis **rejects the null hypothesis**. There is strong statistical evidence that the mean total scores differ between the two groups.

> **Important:** This statistical result demonstrates an association/difference between the groups; it does **not** prove that completing the preparation course caused the higher scores.

## 🔎 Outlier Analysis

The IQR method was applied to `total score`.

- Q1: **175**
- Q3: **233**
- IQR: **58**
- Lower bound: **88**
- Upper bound: **320**
- Detected outliers: **6**

The identified observations are unusually low total scores. They were retained because an outlier is not automatically an error and may represent a genuine observation.

## 🛠️ Technologies & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- SciPy

## 📓 Notebook

The complete analysis is available in:

`students-performance-eda-statistical-analysis(1).ipynb`

The notebook includes the data-processing steps, visualizations, outlier analysis, and statistical test.

## ⚠️ Limitations

- This is an **observational dataset**, so associations should not be interpreted as causal relationships.
- The demographic categories are analyzed using the labels provided by the dataset and are not intended to support broader claims about demographic groups.
- Outliers are retained rather than automatically removed.
- The hypothesis test compares group means without controlling for other variables such as lunch type, parental education, or gender.

## 💡 Conclusion

The analysis shows meaningful differences in academic performance across several student characteristics.

The strongest statistical result explored in this project is the significant difference in total scores between students who completed the test-preparation course and those who did not. Other factors—including gender, parental education, and race/ethnicity—also show differences in average performance within this dataset.

---

⭐ If you find this analysis useful, consider giving the repository a star!
