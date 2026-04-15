# Flight Delay and Cancellation Analysis

### Data Science Project using EDA & Machine Learning

## Project Overview

This project focuses on analyzing flight delays and cancellations using real-world aviation data. It combines **Exploratory Data Analysis (EDA)** and **Machine Learning techniques** to uncover patterns, identify key delay factors, and build predictive models.

The goal is to understand **why delays occur**, how they impact airline operations, and how data-driven models can help in predicting flight delays.

---

## Dataset

* Source: Bureau of Transportation Statistics (BTS)
* Records: **1,048,575 flights**
* Features: 30+ columns including:

  * Airline
  * Departure & Arrival Delay
  * Distance
  * Taxi Time
  * Month & Day
  * Delay Causes (Weather, Airline, Security, etc.)

---

## Data Preprocessing

* Removed missing values in critical columns
* Filled delay-cause columns with 0
* Created a new feature:
   `IS_DELAYED` (1 if delay > 15 minutes, else 0)
* Handled outliers using IQR method

---

## Exploratory Data Analysis (EDA)

Key insights derived from visualization and analysis:

*  **79.1% flights are on time**, 20.9% delayed
*  Frontier Airlines has highest delays (~23 mins)
*  Hawaiian Airlines has lowest delays (~1.7 mins)
*  Seasonal trend: March shows highest delays
*  Strong correlation (r ≈ 0.94) between departure & arrival delay
*  Delay distribution is right-skewed with extreme outliers

---

## Statistical Analysis

* **T-Test (AA vs DL)** → Significant difference in delays
* **Chi-Square Test (Month vs Delay)** → Seasonal impact confirmed

---

## Machine Learning Models

### Linear Regression

* Target: `ARRIVAL_DELAY`
* Feature: `DEPARTURE_DELAY`
* R² Score: **0.916**
* MAE: **7.25 minutes**

Shows strong prediction capability

---

### Logistic Regression

* Target: `IS_DELAYED`

* Features:

  * AIR_TIME
  * DISTANCE
  * MONTH
  * TAXI_OUT

* Balanced Dataset: 10,000 samples

* Accuracy: **~54%**

* Insight: Limited features reduce classification performance

---

## Key Insights

* Departure delay is the **strongest predictor** of arrival delay
* Delay propagation is a major factor in aviation systems
* Airline efficiency varies significantly
* External factors like **weather & congestion** play crucial roles

---

## Tech Stack

* Python 
* Pandas & NumPy
* Matplotlib & Seaborn
* Scikit-learn
* SciPy

---

## Visualizations Included

* Histogram (Delay Distribution)
* Pie Chart (On-time vs Delayed)
* Correlation Heatmap
* Boxplot (Outliers)
* Pairplot
* Confusion Matrix

---

## Future Work

* Integrate real-time weather API 
* Use advanced models:

  * Random Forest
  * XGBoost
  * LSTM (Deep Learning)
* Build a real-time delay prediction dashboard

---

## Author

**Thanda Sai Moukthika**
🎓 B.Tech CSE (Data Analytics)
🏫 Lovely Professional University

---


## Dataset Note
Full dataset is not uploaded due to size limitations. A sample dataset is provided.
