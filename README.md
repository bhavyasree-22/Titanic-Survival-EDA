# Titanic-Survival-EDA
An end-to-end exploratory data analysis (EDA) of the Titanic dataset to identify key factors influencing passenger survival, featuring feature engineering and automated profiling.
# Titanic Survival Prediction: End-to-End EDA 🚢

An exhaustive exploratory data analysis (EDA) performed in **Google Colab**, focusing on identifying the socio-demographic drivers of survival rates among Titanic passengers.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Zt0yFhGwSBtfYH6qUU_QKLJw9O76CuZx?usp=sharing)

## 📌 Project Objective
This project performs a rigorous, end-to-end exploratory analysis to isolate and quantify the situational factors (Class, Gender, Age) that determined passenger survival. The analysis confirms the "women and children first" protocol and highlights significant social inequalities of the time.

## 🛠️ Tech Stack
* **Environment:** Google Colab
* **Libraries:** `Pandas`, `NumPy` (Data Manipulation)
* **Visualization:** `Seaborn`, `Matplotlib` (Statistical Graphics)
* **Automated EDA:** `ydata-profiling`

---

## 📈 Analytical Workflow

### 1. Data Acquisition & Inspection
Assessment of the dataset structure (891 entries) and identifying missing values in `Age`, `Cabin`, and `Embarked`.

### 2. Data Sanitation (Cleaning)
* **Missing Age:** Imputed with the **median** (28.0) to maintain distribution integrity.
* **Missing Embarked:** Imputed with the **mode** ('S').
* **Missing Cabin:** Transformed into a new binary feature `Has_Cabin` (1 if assigned, 0 if missing).

### 3. Feature Engineering
Created new metrics to uncover hidden correlations:
* **Title Extraction:** Extracted titles (Mr, Mrs, Miss, Master) from names using Regex to identify social status and age groups.
* **Family Metrics:** Derived `FamilySize` and `IsAlone` to analyze the impact of traveling with relatives.

### 4. Multivariate Analysis
Used statistical visualizations to identify relationships:
* **Survival by Pclass & Sex:** Confirmed that females in 1st and 2nd class had the highest survival probability.
* **Age Distribution:** Used `ViolinPlots` to see survival density across different age brackets.
* **Correlation Heatmap:** Identified strong negative correlations between `Pclass` and `Fare`.

---

## 💡 Key Findings
* **Primary Predictors:** Being female (Mrs, Miss) was the single most significant advantage.
* **Class Hierarchy:** Survival followed a clear trend: **1st > 2nd > 3rd class**.
* **The "Master" Title:** Young boys (Master) had significantly higher survival rates than adult men (Mr), reinforcing the "children first" protocol.
* **Family Size:** Small families (2–4 members) had better survival odds than those traveling alone or in very large groups.

## 🚀 How to Use
Since this project was built in **Google Colab**, no local setup is required.
1. Click the **Open in Colab** badge above.
2. The notebook includes a command `!pip install ydata-profiling` to set up the automated reporting tool.
3. Run all cells to view the interactive charts and the generated HTML profile report.

---

**Project by:** Bhavya  
*2nd Year Student at VIT-AP | Aspiring AI/ML Engineer*
