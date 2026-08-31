# Football Player Market Value Predictive Pipeline 

An end-to-end Python machine learning pipeline that explores, transforms, and models football player valuation 
data sourced from Transfermarkt datasets via the Kaggle Hub API. 

This project evaluates how regional macroeconomic environments (domestic league tiers) 
scale against isolated player demographics (age and position) when determining market value assets.

## Key Insights
* **The Power Law Discovery:** Statistical testing via SciPy Quantile-Quantile (Q-Q) plotting mathematically rejected normality. 
The asset market exhibits massive zero-inflation (squad-player compression near the €1M floor) with an exponential right-hand superstar tail.
* **Macro Environment > Demographics:** Utilizing only age and position yielded an R² of `0.025` (explaining only 2.5% of variance). 
Introducing categorical feature engineering for domestic competition tiers boosted the model's test R² to `0.119`—a **~400% performance surge** 
that cut baseline MAE by nearly €1 Million.

## 🛠️ Tech Stack & Architecture
* **Language:** Python 3.13
* **Data Engineering:** Pandas, NumPy
* **Statistical Analysis:** SciPy (Shapiro-Wilk test, Probplot / Q-Q distribution models)
* **Machine Learning & Pipeline Architecture:** Scikit-Learn (ColumnTransformer, OneHotEncoder, Random Forest Regressor, Pipeline)
* **Visualizations:** Seaborn, Matplotlib
