
# 📊 TMDB 5000 Movie Dataset Analysis

## 🔍 Project Overview

This project investigates what factors are most associated with a movie’s financial success using the **TMDB 5000 Movie Dataset**. The analysis explores relationships between revenue and other movie characteristics such as **budget**, **popularity**, **vote average**, and **genre**.

The dataset was sourced from [The Movie Database (TMDb)](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata), containing detailed metadata on over 5,000 movies including cast, crew, genre, and performance metrics.

---

## 📁 Files

* `tmdb_5000_movies.csv`: Contains metadata and performance details for 4800+ movies.
* `tmdb_5000_credits.csv`: Contains cast and crew data for the same movies.
* `tmdb_analysis.ipynb`: Jupyter Notebook used for cleaning, analyzing, and visualizing the data.
* `README.md`: Project overview and explanation (you’re here!).

---

## 🧠 Key Questions

> **What factors are most associated with high movie revenue?**

To answer this, the notebook explores the impact of:

1. **Budget**
2. **Popularity**
3. **Vote Average (Rating)**
4. **Genres**

---

## 🧹 Data Wrangling

* **Merging**: The `movies` and `credits` datasets were merged using the movie ID.
* **Cleaning**:

  * Filled or removed missing values.
  * Parsed JSON-like strings for genres.
  * Removed unnecessary and duplicate columns.
* **Transformation**: Added custom columns for genre analysis and binned vote averages.

---

## 📈 Analysis Highlights

* **Budget vs Revenue**: Strongest positive correlation (**r ≈ 0.73**).
* **Popularity vs Revenue**: Moderately strong correlation (**r ≈ 0.64**).
* **Vote Average vs Revenue**: Weak correlation (**r ≈ 0.19**).
* **Genres**: Animation and Adventure movies tend to have higher average revenues.

All results were visualized using histograms, scatterplots, bar plots, and boxplots with `matplotlib` and `seaborn`.

---

## 📌 Key Takeaways

* **Budget and Popularity** are the best predictors of revenue.
* **High Ratings ≠ High Revenue** – many low-rated films earn a lot.
* **Genre matters**, but not as much as budget or popularity.
* Movie revenue distribution is heavily **right-skewed**, with a few blockbusters driving most earnings.

---

## ⚠️ Limitations

* Correlation ≠ Causation: This is an exploratory analysis, not a predictive model.
* Key factors like marketing, release timing, or franchise status were **not included**.
* Outliers could still influence visual interpretation despite adjustments.

---

## 🛠️ Tools Used

* Python 3
* Jupyter Notebook
* pandas
* numpy
* seaborn
* matplotlib

