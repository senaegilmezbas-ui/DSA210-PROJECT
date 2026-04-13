# 🏃‍♂️ Longitudinal Analysis of Running Performance (2017–2026)

## 1. Project Motivation

Inspired by a national-level running career, this project analyzes how performance evolves over time using real-world running data. The goal is to move beyond intuition and understand how factors such as aging, environmental conditions, and training habits influence running performance.

By building a complete data science pipeline, this project aims to uncover meaningful patterns and provide data-driven insights into long-term athletic performance.

---

## 2. Data Pipeline & Methodology

### 2.1 Data Acquisition

* Source: Strava activity export
* Time range: January 2017 – March 2026
* Observations: ~2,800 running activities

The dataset includes key variables such as:

* Distance
* Pace
* Elevation Gain
* Average Heart Rate

---

### 2.2 Data Cleaning & Preprocessing

To ensure reliable analysis, the dataset was preprocessed as follows:

* Filtered for running activities only
* Removed missing values in key variables
* Converted date columns and extracted year information
* Calculated pace (minutes per kilometer)
* Removed unrealistic outliers (pace outside 3–12 min/km range)

---

### 2.3 Exploratory Data Analysis (EDA)

The analysis includes:

* Time-series visualization of performance trends
* Box plots to compare pace distributions across COVID periods
* Scatter plots to analyze relationships between variables
* Correlation matrices to explore feature interactions

---

### 2.4 Statistical Testing

To validate the hypotheses, the following methods were used:

* Independent Samples T-test (Welch’s t-test)
* Pearson Correlation Analysis

---

## 3. Testable Hypotheses

**H1:** There is a significant difference in average running pace between the COVID-19 period (2020–2021) and the pre/post-pandemic periods.

**H2:** There is a significant difference in running pace between runs with low elevation gain and runs with high elevation gain.

**H3:** There is a significant relationship between time (year) and running pace over the 9-year period.

**H4:** There is a significant relationship between weekly training frequency and average heart rate.

---

## 4. Key Findings

* Running pace slightly decreased (i.e., became slower) during the COVID-19 period
* Higher elevation runs are associated with slower pace values
* A weak but statistically significant trend suggests performance changes over time
* No statistically significant relationship was found between training frequency and heart rate

---

## 📂 Data Availability

A sample dataset (`sample_data.csv`) is provided to demonstrate the structure of the data and ensure reproducibility of the analysis.

The full dataset is based on personal Strava data and is not publicly shared for privacy reasons.

---

## 🛠️ Reproducibility

To reproduce the analysis:

1. Use the provided `sample_data.csv`
2. (Optional) Replace it with your own Strava export
3. Run the notebook

---

## ⚠️ Limitations

* The dataset represents a single athlete
* Elevation is measured via elevation gain, not exact terrain classification
* Training frequency does not capture intensity or recovery
* External factors such as weather are not included

---

## 🎓 Academic Integrity

This project was created for **DSA 210 – Introduction to Data Science**.

AI tools were used only for writing assistance and debugging, in accordance with academic integrity guidelines.

---
