# ✈️ Airline Delay Analysis

This project explores the **Reporting Carrier On-Time Performance Data** to uncover patterns and insights related to flight arrival delays. The focus is on identifying which factors most significantly contribute to delays, with an emphasis on carrier performance and delay causes.

---

## 📊 Project Overview

- **Goal:** Investigate the main causes of arrival delays in U.S. domestic flights.
- **Dataset:** Reporting Carrier On-Time Performance Data from the [U.S. Bureau of Transportation Statistics](https://www.transtats.bts.gov/OT_Delay/OT_DelayCause1.asp).
- **Toolkits:** `Pandas`, `NumPy`, `Matplotlib`, `Seaborn`, `Jupyter Notebook`.

---

## 🔍 Key Questions Explored

- What is the distribution of arrival delays?
- Which carriers tend to have more delays?
- How do different types of delay (e.g., weather, security) affect arrival time?
- Are there seasonal or monthly patterns in delay behavior?
- How does flight volume relate to performance?

---

## 🧹 Data Wrangling

- Removed **cancelled** and **diverted** flights to focus on operational flights.
- Excluded rows with missing critical delay data.
- Selected relevant columns related to delay causes and flight metadata.

---

## 📈 Exploratory Data Analysis

### Univariate
- Arrival delays (`arr_delay`) are **right-skewed** with a long tail of extreme values.
- Most flights arrive on time or slightly early.

### Bivariate
- Strong correlation between **carrier delay** and **arrival delay**.
- Some carriers (e.g., OO, MQ) appear more frequently and show varying delay behavior.

### Multivariate
- `late_aircraft_delay` and `carrier_delay` have the **strongest influence** on overall delays.
- Delays fluctuate across **months** and **airlines**, indicating seasonal and operational patterns.

---

## 💡 Key Insights

1. **Carrier and Late Aircraft Delays** are the strongest predictors of arrival delay.
2. Some airlines consistently experience **more delays** than others.
3. **Security-related delays** are rare and have minimal impact.
4. Delays vary significantly across **months**, revealing **seasonal trends**.
5. **High flight volume ≠ Poor performance** — some busy carriers still perform well.

---

## 🛠️ Technologies Used

- Python 3
- Jupyter Notebook
- Pandas, NumPy
- Matplotlib, Seaborn

