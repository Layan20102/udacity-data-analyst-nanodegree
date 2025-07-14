# 📊 Exploring the Relationship Between Population Size and GDP per Capita

## Overview

In this project, we investigate whether there is a clear relationship between a country's **population size** and its **GDP per capita**. The assumption that high population correlates negatively with per capita income is often taken for granted—but is it true across all countries?

Using economic and demographic data from reliable sources, this analysis combines data processing, cleaning, and visualization to explore patterns and answer the core research question:

> **Is there a clear relationship between a country's population size and the level of income per person (GDP per capita)?**

---

## 📁 Dataset Sources

### 1. **GDP Data**

* **Source:** [World Bank API](https://data.worldbank.org/)
* **Method:** Collected using `pandas-datareader`'s `wb.download()` function.
* **Variable of interest:** `NY.GDP.MKTP.CD` — GDP (current US\$)

### 2. **Population Data**

* **Source:** Manually downloaded CSV from the World Population Dataset
* **Additional features:** Country rank, area, density, growth rate, etc.

---

## 🛠️ Data Processing

1. **Standardized column names** for consistency.
2. **Reshaped population data** to long format using `pd.melt()`.
3. **Merged** the GDP and population datasets on `country` and `year`.
4. **Derived GDP per capita** by dividing GDP by population.
5. **Mapped countries to ISO Alpha-3 codes** using the `pycountry` package.

---

## 🔍 Data Quality and Tidiness Fixes

* Converted `year` columns to `int` type for consistency.
* Addressed scientific notation in GDP display for readability.
* Added a computed `GDP_per_capita` column.
* Standardized country codes for integration with external data.

---

## 📈 Visualizations

* **Scatter Plot**: Shows GDP per capita vs. population (log-log scale).
* **Box Plot**: Shows GDP per capita distribution across population quartiles.

These plots indicate **no strong linear relationship** between population size and GDP per capita. While some high-income, small-population countries exist, large countries can also be wealthy (e.g., the U.S.), and vice versa.

---

## 💡 Key Insights

* Population size alone is **not a reliable predictor** of GDP per capita.
* Variance in GDP per capita is highest among low-population countries.
* Other factors likely influence income levels—such as education, infrastructure, governance, and natural resources.

---

## 🔄 Future Work

If extended, the analysis could include:

* Time-series trends over more years (e.g., 2000–2022)
* Additional predictors (education, employment, trade data)
* Advanced modeling (e.g., multivariate regression)

---

## 💾 Files

| File Name                            | Description                                  |
| ------------------------------------ | -------------------------------------------- |
| `raw_data_population_gdp.csv`        | Combined raw data (GDP and population)       |
| `cleaned_data_population_gdp.csv`    | Cleaned and processed dataset                |
| `Data_Wrangling_Project_Starter.ipynb` | Jupyter notebook with full code and analysis |
| `README.md`                          | Project overview and documentation           |

---

## 🧰 Technologies Used

* Python (Pandas, Matplotlib, Seaborn)
* pandas-datareader
* pycountry
* Jupyter Notebook

