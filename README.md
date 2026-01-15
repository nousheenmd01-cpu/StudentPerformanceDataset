# Student Performance Dataset

## Description
This dataset contains performance records of 99 students. It includes information on their weekly self-study hours, attendance, class participation, and total score. The target variable is `grade`, representing the student's performance as A, B, C, or D.

This dataset is suitable for **machine learning classification tasks** after minor preprocessing.

---

## Dataset Structure

| Column Name                | Description                                           | Data Type  |
|----------------------------|-------------------------------------------------------|------------|
| `student_id`               | Unique identifier for each student                   | int        |
| `weekly_self_study_hours`  | Number of hours the student studies per week        | float      |
| `attendance_percentage`    | Attendance of the student in percentage             | float      |
| `class_participation`      | Participation score in class                         | float      |
| `total_score`              | Total score obtained                                  | float      |
| `grade`                    | Target variable (A, B, C, D)                         | categorical|

---

## Data Summary

- **Rows:** 99  
- **Columns:** 6  
- **Data Types:** Numerical (int/float) for features, categorical (object) for target variable

### Statistics of Input Features

| Feature                  | Min   | 25%    | Median | 75%    | Max   | Mean   | Std    |
|---------------------------|-------|--------|--------|--------|-------|--------|--------|
| `weekly_self_study_hours` | 0     | 10.8   | 14.2   | 18.05  | 28    | 14.32  | 6.31   |
| `attendance_percentage`   | 64.4  | 78.15  | 83.7   | 89.85  | 100   | 83.80  | 8.88   |
| `class_participation`     | 2.5   | 4.6    | 6.0    | 7.6    | 9.7   | 6.05   | 1.81   |
| `total_score`             | 47.4  | 71.1   | 84.0   | 97.7   | 100   | 82.88  | 15.34  |

---

## Grade Distribution

| Grade | Number of Students |
|-------|------------------|
| A     | 48               |
| B     | 27               |
| C     | 19               |
| D     | 5                |

**Observation:** The dataset is imbalanced. Grade A has a significantly higher number of students compared to grade D. This should be considered when training machine learning models.

---

## Usage

1. Load the dataset using pandas:

```python
import pandas as pd
df = pd.read_csv("student_performance.csv")
