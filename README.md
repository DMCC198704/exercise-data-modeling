# Exercise Data Modeling & User Behavior Analysis

## Overview

This project develops a unified framework for analyzing and modeling exercise data using both **unsupervised and supervised machine learning techniques**.

The goal is to:

* Identify meaningful **behavioral patterns** in users
* Build **predictive models** for activity metrics
* Handle **incomplete data scenarios**
* Create interpretable **summary scores** of physical activity

The project is structured around five core components that together form a complete analysis pipeline.

---

## 1. Clustering of Exercise Behavior (Primary Component)

### Objective

To group users into distinct categories based on their physical activity patterns.

### Features Used

* Steps
* Active Minutes
* Calories Burned
* Total Distance

### Methods

#### K-Means Clustering

* Segments users into clusters representing different activity levels
* Identifies natural groupings such as low, moderate, and high engagement

**Use Cases:**

* User segmentation
* Social matching and engagement
* Behavioral analysis

#### DBSCAN (Exploratory)

* Tested density-based clustering
* Did not produce meaningful clusters for this dataset
* Included to document modeling exploration and comparison

### Key Insight

Exercise behavior is not uniform—users naturally fall into **distinct activity profiles**, which can be leveraged for personalization and analysis.

---

## 2. Overall Activity Score

### Objective

To create a single, interpretable metric that summarizes a user’s daily activity.

### Approach

* Combined:

  * Steps
  * Minutes
  * Calories
  * Distance
* Generated a composite score
* Calculated percentile rankings relative to other users

### Outcome

Provides a simple way to benchmark activity levels and compare individuals.

---

## 3. Calories Prediction (Regression Models)

### Objective

To predict caloric expenditure based on user activity inputs.

### Methods

* Applied multiple regression models
* Designed to incorporate additional real-world data over time

### Use Case

* Estimating calories when direct measurement is unavailable
* Supporting fitness tracking systems

---

## 4. Missing Data Prediction

### Objective

To estimate missing values when only partial activity data is available.

### Approach

* Modeled relationships between:

  * Steps
  * Minutes
  * Calories
  * Distance
* Predicted the missing variable given the others

### Importance

Improves robustness in real-world datasets where incomplete entries are common.

---

## 5. Modeling Pipeline Integration

These components form a connected system:

* Clustering → identifies user types
* Activity Score → summarizes behavior
* Regression → predicts outcomes
* Input Prediction → fills missing data

Together, they provide a structured approach to analyzing and modeling exercise behavior.

---

## Tools & Technologies

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib / Seaborn
* Jupyter Notebook

---

## Key Takeaways

* User activity can be segmented into meaningful behavioral groups
* Predictive models can estimate key fitness metrics
* Missing data can be handled systematically
* Combining multiple methods produces a more complete analytical framework

---

## Author

Darren McCauley
2025
