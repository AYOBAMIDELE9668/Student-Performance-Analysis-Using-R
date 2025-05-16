# Student-Performance-Analysis-Using-R
This project explores how students' daily habits impact their academic performance. Using a dataset of 1,000 students and the power of **R** and **machine learning**, we uncover insights into how lifestyle factors like study hours, sleep, social media use, and diet influence exam scores.

## 📊 Objective

To analyze the relationship between students' daily routines and their academic outcomes, and to develop predictive models for estimating exam performance.

---

## 🧠 Dataset Overview

The dataset includes the following features:

- **Demographics**: `age`, `gender`, `parental_education_level`
- **Lifestyle Habits**: `study_hours_per_day`, `social_media_hours`, `netflix_hours`, `sleep_hours`, `diet_quality`, `exercise_frequency`
- **Academic Factors**: `attendance_percentage`, `part_time_job`, `extracurricular_participation`
- **Technology & Wellbeing**: `internet_quality`, `mental_health_rating`
- **Target Variable**: `exam_score`

> ✅ Clean data: No missing values were found  
> ✅ `student_id` column removed to prevent leakage

---

## 📈 Exploratory Data Analysis

- Summary statistics of all numeric variables
- Frequency tables for categorical features
- Visualizations:
  - Bar charts for categorical variables
  - Scatter plots of each numeric feature vs. `exam_score`
  - Histogram and boxplot of `exam_score`
  - Correlation matrix of numeric features

### 🔍 Notable Correlations

| Feature                  | Correlation with `exam_score` |
|--------------------------|-------------------------------|
| Study Hours              | **+0.83**                     |
| Mental Health Rating     | +0.32                         |
| Sleep Hours              | +0.12                         |
| Social Media Hours       | -0.17                         |
| Netflix Hours            | -0.17                         |

---

## 🤖 Machine Learning Models

Using the `caret` package with 5-fold cross-validation, we trained the following models:

- 📐 **Linear Regression**
- 🌳 **Decision Tree (`rpart`)**
- 📈 **Support Vector Machine (Radial)**
- 🧠 **Neural Network (`nnet`)**
- 🌲 **Random Forest**
- 🔥 **Gradient Boosting (`gbm`)**
- 🧍‍♂️ **K-Nearest Neighbors (`knn`)**

### 📊 Model Evaluation

All models were evaluated using **RMSE (Root Mean Square Error)** on the test set. The **Linear Regression** model performed exceptionally well, confirming the linear relationship between study habits and exam scores.

---

## 🛠 Tools & Technologies

- **Language**: R
- **Libraries**:
  - `caret` - Model training and tuning
  - `ggplot2` - Data visualization
  - `lattice` - Visualization support
  - `base R` - Data manipulation and analysis

