# Final_Project_Rakamin_Bootcamp
Final Project Rakamin ini adalah membuat machine learning untuk data Attrition pada sebuah perusahaan.
1. [Exploratory Data Analysis](#exploratory-data-analysis)

2. [Data Preprocessing](#data-preprocessing)

3. [Modeling Data](#modeling-data)

3.1. [Logistic Regression](#logistic-regression)

3.2. [Decision Tree](#decision-tree)

3.3. [XGBoost](#xgboost)

3.4. [CatBoost](#catboost)

3.5. [Random Forest](#random-forest)

## Exploratory Data Analysis
Analisis ini berkaitan dengan mengeksplorasi variabel kategori dan numerik yang berbeda dan hubungannya dengan attrition. 

### 1. Checking Data

```bash
import pandas as pd
df = pd.read_csv('HR-Employee-Attrition.csv')
df.info()
```

![]

