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
![image.png](https://drive.google.com/file/d/1Jkek-qzo0NT1hOUCNG_Jd62KtQKNI3k8/view?usp=sharing)

Pengamatan:
Data terdiri dari 1470 baris
Tidak ada kolom yang memiliki null/missing values
Terdapat kolom dengan tipe data yang tidak sesuai, akan di handle pada saat preprocessing 


## Checking Duplicate
```bash
duplicate = df[df.duplicated()]
print(duplicate)
print('Jumlah data duplicate',df.duplicated().sum()
```

Pengamatan:
Tidak ada data duplicate

## Descriptive Statistics
```bash
df[nums].describe()
```
```bash
df[cats].describe()
```

![image.png]

Pengamatan:
Kolom EmployeeCount, EmployeeNumber dan StandardHours hanya memiliki 1 nilai
Kolom DistanceFromHome, MonthlyIncome, NumCompaniesWorked, PercentSalaryHike, TotalWorkingYears, YearsInCurrentRole, YearsSinceLastPromotion dan YearsWithCurrManager tampaknya skew ke kanan (long-right-tail)
Untuk kolom yang memiliki 1 nilai akan di drop pada saat data pre-processing
No-attrition data mendominasi dan kita akan melakukan SMOTE pada data Yes-Attrition. Persentase data attrion Yes : No = 17% : 83%
Kita akan aplikasikan teknik encoding pada kolom: Attrition, Gender and OverTime
Kita akan menggunakan teknik one-hot encoding pada columns : Business Travel, Department, Education Field, Job Role, Marital Status
Data categoric didominasi oleh pegawai yang berusia diatas 18 tahun (Over18), tidak attrion (Attrition), jarang berpergian / perjalan bisnis (BusinessTravel), tidak lembur (OverTime), dan berasal dari department resert & development (Department) serta berjenis kelamin laki-laki(Gender)
Data Over18 ternyata hanya memiliki 1 nilai, sehingga akan di drop pada saat data pre-processing

## Pie Chart Attrition

```bash
colors = ['#5B7DB1', '#FF6B6B']
fig = go.Figure(data=[go.Pie(labels=['No','Yes'], values=df['Attrition'].value_counts())])
fig.update_layout(autosize=False, width=400, height=350)
fig.update_traces(marker=dict(colors=colors))
fig.show()
```
No-attrition data mendominasi dan kita akan melakukan SMOTE pada data Yes-Attrition. Persentase data attrion Yes : No = 16,1% : 83,9%

## Univariate Analysis

