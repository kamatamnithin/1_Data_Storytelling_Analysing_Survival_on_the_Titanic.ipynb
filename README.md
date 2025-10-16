🧭 Exploratory Data Analysis (EDA) on the Titanic Dataset
📘 Overview

This project performs an in-depth Exploratory Data Analysis (EDA) on the famous Titanic dataset to uncover meaningful insights about the passengers and their survival patterns. The goal is to understand the data, clean it, visualize key relationships, and prepare it for machine learning modeling.

EDA is a critical step in any data science workflow — it helps identify patterns, detect anomalies, handle missing data, and generate hypotheses before building predictive models.

🎯 Objectives

Understand the structure, types, and quality of the Titanic dataset.

Perform data cleaning and preprocessing (handle missing values, outliers, and transformations).

Conduct univariate, bivariate, and multivariate analysis using visualizations.

Engineer new features such as FamilySize, IsAlone, and Title to enhance predictive power.

Generate a data profiling report using ydata-profiling for automated analysis.

Summarize key findings that reflect social and demographic patterns in survival rates.

🧰 Libraries Used
Library	Purpose
Pandas	Data manipulation and cleaning
NumPy	Numerical computations
Matplotlib	Data visualization (base plotting library)
Seaborn	Advanced statistical data visualization
YData-Profiling	Automated exploratory data profiling and report generation
⚙️ Step-by-Step Process
1️⃣ Setup

Imported essential libraries — pandas, numpy, matplotlib, and seaborn — and configured visualization styles.

2️⃣ Data Loading & Inspection

Loaded the Titanic dataset and explored its structure, data types, and missing values using:

titanic_df.info()
titanic_df.describe()

3️⃣ Data Cleaning

Handled missing data:

Age filled with median.

Embarked filled with mode.

Created a new column Has_Cabin from Cabin due to 77% missing values.

4️⃣ Univariate Analysis

Visualized distributions of individual variables:

Categorical: Survived, Sex, Pclass, Embarked

Numerical: Age, Fare

5️⃣ Bivariate Analysis

Explored relationships between features and the survival outcome:

Higher survival for females, 1st class, Cherbourg passengers, and those with cabins.

6️⃣ Feature Engineering

Created new meaningful features:

FamilySize = SibSp + Parch + 1

IsAlone (binary indicator for solo travelers)

Extracted Title (Mr, Miss, Mrs, etc.) from passenger names.

7️⃣ Multivariate & Correlation Analysis

Combined variables (e.g., Sex vs Pclass vs Survived).

Plotted a correlation heatmap for numerical features.

8️⃣ YData-Profiling Report

Generated a detailed automated profiling report for the cleaned dataset:

from ydata_profiling import ProfileReport
profile = ProfileReport(titanic_df, title="Titanic Dataset Profiling Report")
profile.to_file("titanic_profile.html")


The report summarizes data types, missing values, correlations, and distribution details.

🧩 Key Insights

Women and children first: Female passengers and young children had the highest survival rates.

Socioeconomic inequality: 1st-class passengers had over 60% survival, while 3rd-class dropped below 25%.

Family impact: Moderate family sizes (2–4 members) improved survival; solo travelers had the lowest rates.

Cabin and fare correlation: Passengers with cabins or higher fares were more likely to survive.

Titles reveal hierarchy: Titles such as Mrs, Miss, and Master strongly correlated with survival chances.

📊 Final Output

Cleaned and well-structured Titanic dataset.

Interactive visualizations explaining passenger demographics and survival patterns.

Automated YData-Profiling HTML report summarizing the dataset quality and correlations.

📁 Repository Structure
├── .ipynb              # Jupyter Notebook containing full analysis
├── titanic_profile.html            # YData-Profiling HTML report
├── README.md                       # Project documentation (this file)
└── /datasets/Titanic-Dataset.csv   # Source dataset

🧠 Conclusion

This end-to-end EDA uncovers the critical factors influencing Titanic passengers’ survival and sets a strong foundation for building a machine learning classification model in future work.

Through effective data visualization, feature engineering, and profiling, this project demonstrates the power of EDA in revealing insights and improving model readiness
