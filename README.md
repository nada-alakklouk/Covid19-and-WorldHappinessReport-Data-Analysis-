# 🦠 Covid-19 Global Spread vs. World Happiness Report Analysis

A comprehensive Data Science project aimed at analyzing and finding correlations between the spread of Covid-19 and global socioeconomic factors. This study combines international pandemic datasets with the **World Happiness Report** to determine if a country's economic status, life expectancy, or social support metrics correlate with its maximum infection rate.

---

## 📂 Project Structure & Assets

The repository contains the data analysis workbook and the corresponding structural data files:

* 💻 **[View Analysis Notebook (Jupyter)](./main.ipynb)** – The complete interactive Jupyter Notebook containing data pipeline steps, transformations, plotting, and correlation matrices.
* 🗃️ **Datasets Handled:**
  * `covid19_Confirmed_dataset.csv` – Global time-series data detailing confirmed Covid-19 cases by country/region.
  * `worldwide_happiness_report.csv` – Annual metrics evaluating national scores for GDP, social freedom, health, and corruption.

---

## 🛠️ Tech Stack & Methods

* **Programming Language:** Python 🐍
* **Data Engineering Libraries:** Pandas and NumPy for complex grouping, structural filtering, data cleaning, and dataset inner joining.
* **Data Visualization:** Matplotlib for line plotting trends and tracking the first derivative (infection speed curves).
* **Statistical Methods:** Pearson Correlation Matrix calculation to derive linear relationships.

---

## 🚀 Analytical Pipeline & Tasks

### Task 1: Covid-19 Infection Metrics Engineering
* **Data Refining:** Dropped irrelevant geographical attributes (`Lat` and `Long`).
* **Regional Aggregation:** Grouped global data by `Country/Region` to obtain a unified country-level daily timeline.
* **First Derivative Calculation (`.diff()`):** Extracted daily new case frequencies to identify the absolute **Maximum Infection Rate** for each country as a baseline spread metric.

### Task 2: Socioeconomic Integration & Correlation
* **Feature Selection:** Dropped secondary indices from the World Happiness Report, retaining `GDP per capita`, `Social support`, `Healthy life expectancy`, and `Freedom to make life choices`.
* **Dataset Alignment & Inner Join:** Consolidated both dataframes based on the country index to perform safe statistical computing on shared global records.
* **Correlation Computation (`.corr()`):** Generated an evaluation matrix to quantify links between socioeconomic health and the acceleration of the virus.

---

## 📊 Key Analytical Insights

* **GDP & Healthy Life Expectancy Impact:** The final correlation matrix reveals a positive correlation (~0.25 to 0.29) between a country's `GDP per capita` / `Healthy life expectancy` and its `max_infection_rate`. This suggests that more developed countries with advanced healthcare infrastructures often recorded higher infection acceleration rates, likely driven by denser international transit and broader testing capacities.
* **Strong Structural Alignments:** Predictably strong positive links exist within the socioeconomic report itself—such as the massive connection (~0.86) between high economic prosperity (`GDP`) and longer `Healthy life expectancy`.

---

## 👤 Developed by:
* **Nada Alaklook**
* 🔗 [Connect with me on LinkedIn](https://linkedin.com/in/nada-alaklook-725049252)
