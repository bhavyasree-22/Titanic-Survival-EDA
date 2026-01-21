# 🚢 Titanic Survival Prediction: End-to-End EDA

This project performs a rigorous, end-to-end exploratory analysis of the Titanic passenger dataset. The primary goal is to isolate and quantify the socio-demographic and situational factors that determined passenger survival rates.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Zt0yFhGwSBtfYH6qUU_QKLJw9O76CuZx?usp=sharing)

---

## 📝 Project Description
In April 1912, the RMS Titanic sank after colliding with an iceberg, leading to the loss of over 1,500 lives. While there was an element of luck involved in survival, historical records suggest that certain groups—such as women, children, and the upper class—were prioritized during evacuation.

This project uses Python-based data science to move beyond historical narratives and provide a data-driven validation of the "women and children first" protocol. By performing detailed data sanitation, feature engineering, and multivariate analysis, this study identifies exactly how socio-economic status (Pclass), gender, and family structures influenced a passenger's probability of survival. The insights gained here serve as a foundational step for building high-accuracy predictive machine learning models.

---

## 📂 Dataset Information
The dataset contains information about 891 passengers, including features such as Age, Sex, Passenger Class, and Fare.
* **Download Dataset:** [Titanic-Dataset.csv](./Titanic-Dataset.csv)
* **Source:** Kaggle 

---

## 🛠️ Technical Skills Demonstrated
Before diving into the analysis, these are the core competencies and tools utilized in this project:
* **Languages:** Python (`Pandas`, `NumPy`)
* **Visualizations:** `Seaborn`, `Matplotlib`
* **Automated Profiling:** `ydata-profiling`
* **Data Science Techniques:** Missing Value Imputation, Regex Feature Extraction, Statistical Profiling, Multivariate Analysis, Correlation Mapping.

---

## 📈 Analytical Workflow

I followed a structured 10-step process to ensure data integrity and actionable insights:

### 1. Data Acquisition & Inspection
Initial assessment of the dataset structure (891 entries) and identifying missing values in `Age`, `Cabin`, and `Embarked`.

### 2. Data Sanitation (Cleaning)
* **Missing Age:** Imputed with the **median** (28.0) to handle skewness.
* **Missing Embarked:** Imputed with the **mode** ('S').
* **Missing Cabin:** Transformed into a new binary feature `Has_Cabin` (1 if assigned, 0 if not).

### 3. Feature Engineering
Derived new metrics to uncover hidden correlations:
* **Title Extraction:** Pulled titles (Mr, Mrs, Miss, Master) from names using Regex to identify social status.
* **Family Metrics:** Created `FamilySize` and `IsAlone` to see how social support influenced survival.

### 4. Multivariate Analysis
Utilizing statistical visualizations to identify relationships between Class, Gender, Age, and Survival.



---
## 📊 Technical Process (The 10-Step Framework)

I implemented a structured data science pipeline to ensure high data integrity and actionable results:

### 1️⃣ Step 1: Importing Libraries for the Project
Setting up the technical stack including `Pandas` for manipulation, `NumPy` for computation, and `Seaborn/Matplotlib` for high-level statistical graphics.

### 2️⃣ Step 2: Data Loading and Initial Inspection
Initial assessment of the 891 entries and 12 features. Evaluated data types and identified critical gaps in the `Age`, `Cabin`, and `Embarked` columns.

### 3️⃣ Step 3: Data Cleaning
* **Missing Age:** Imputed missing values using the **Median** (28.0) to maintain a robust central tendency against outliers.
* **Missing Embarked:** Filled nulls with the **Mode** ('S').
* **Missing Cabin:** Transformed 77% missing data into a binary feature `Has_Cabin`, acting as a proxy for luxury accommodations.

### 4️⃣ Step 4: Univariate Analysis
Independently analyzing variables to understand the underlying distribution.

> **Key Finding:** Identified a right-skewed distribution in `Fare`, indicating extreme outliers (luxury suites).

### 5️⃣ Step 5: Bivariate Analysis & Feature Relationships
Analyzing how individual features like `Sex` and `Pclass` directly relate to the target variable: `Survived`.


### 6️⃣ Step 6: Feature Engineering
Engineered high-signal features from raw strings:
* **Title Extraction:** Used Regex to extract titles (Mr, Miss, Master) to separate social status.
* **Family Metrics:** Developed `FamilySize` and `IsAlone` to quantify social support influence.

### 7️⃣ Step 7: Multivariate Analysis
Exploring 3-way interactions (e.g., Sex + Pclass + Survival) to see how gender advantages varied across different social classes.


### 8️⃣ Step 8: Correlation Analysis
Quantifying mathematical relationships between features using a Correlation Heatmap.

> **Observation:** Strong negative correlation found between `Pclass` and `Fare`.

### 9️⃣ Step 9: Automated Data Profiling with y-profiling
Integrated `ydata-profiling` to generate a 360-degree quality report, ensuring no hidden data quality issues were overlooked.

### 🔟 Step 10: Final Conclusion and Summary of Insights
Synthesizing all data points to confirm that Title, Sex, and Pclass were the primary determinants of survival.

---

## 💡 Key Findings
* **The Gender Advantage:** Being female was the strongest predictor (~75% survival rate).
* **Wealth Disparity:** 1st Class passengers had a >60% survival rate, nearly triple that of 3rd Class passengers.
* **Social Synergy:** Families of 2–4 members had the highest survival odds compared to individuals.

---

## 📬 Connect with Me

* **Email:** [gubbabhavya@gmail.com](mailto:gubbabhavya@gmail.com)
* **LinkedIn:** [Bhavya Sree](https://www.linkedin.com/in/bhavyasree-22/)
---
