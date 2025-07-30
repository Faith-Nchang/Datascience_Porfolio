 Predicting Airbnb Guest Review Scores

## Project Overview

This project uses the **Airbnb listings dataset** to predict the **guest review score** of a listing, specifically the `review_scores_ratings` column. Accurately predicting this score can help platforms like Airbnb improve guest satisfaction, maintain trust, and optimize search rankings.

---

## 🎯 Problem Type

* **Type:** Supervised Machine Learning
* **Category:** Regression
* **Label:** `review_scores_rating` (a continuous numeric target)

---

## 📌 Motivation

Predicting guest review scores serves multiple important business purposes:

* **Improved Guest Experience**: By identifying listings likely to offer poor experiences, the platform can intervene or suggest alternatives.
* **Search Ranking Optimization**: Listings predicted to perform well can be promoted in search, increasing guest trust and booking rates.
* **Host Coaching**: Hosts with predicted low ratings can receive guidance to improve service quality.
* **Revenue and Retention**: High-quality stays lead to better reviews, fewer refunds, more returning users, and stronger brand reputation.

## 🧠 Features Used

All columns in the dataset were used **except** the following:

* Dropped  Non-Predictive Columns:

  * utilized a correlation matrix to find the best features that correlates with the target label
  * Used sklearn SelectKBest to get the optimal features for the model
* Target column `review_scores_ratings` was excluded from the features during model training.


## 🔨 Models Used

* **Baseline Model**: Linear Regression
* **Improved Model**: Random Forest Regressor

  * **Tuning**: Performed hyperparameter optimization using **GridSearchCV**

## 🛠️ Tools & Libraries

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib / Seaborn (for visualization)


## 📈 Future Work

* Feature engineering (e.g., extracting useful info from `amenities`, text embeddings for descriptions)
* Model ensembling
* Incorporating NLP techniques for textual columns
* Deployment as a web app for real-time predictions


## ✨ Outcome

Using Random Forest and hyperparameter tuning, model performance significantly improved over the linear regression baseline, yielding better predictions on guest review scores and paving the way for practical application on platforms like Airbnb.

