# Final_Project_Rakamin_Bootcamp

Final Project Rakamin ini adalah membuat machine learning untuk data Attrition pada sebuah perusahaan.

1. [Exploratory Data Analysis](#exploratory-data-analysis)

2. [Data Preprocessing](#data-preprocessing)

3. [Data Modeling](#data-modeling)


## Exploratory Data Analysis
Analisis ini berkaitan dengan mengeksplorasi variabel kategori dan numerik dan hubungannya dengan attrition. 

Yang dilakukan pada tahap ini yaitu:

### 1. Checking Data
Pada tahap ini dilakukan pengecekan terhadap dataset yang akan digunakan, apakah ada missing value atau apakah ada kolom dengan tipe dataset yang tidak sesuai, serta mengecek jumlah dataset.


### Checking Duplicate
Tahap ini melakukan pengecekan apakah dataset yang digunakan terindikasi adanya duplicate atau tidak.

### Descriptive Statistics
Memberikan ringkasan dari setiap kolom di dataset yang dapat memberikan gambaan besar keadaan data.

### Pie Chart Attrition
Melihat target label Attrition apakah target memiliki jumlah data yang timpang atau tidak.

### Univariate Analysis
Pada tahap ini akan dilakukan analisis setiap kolom secara terpisah, melihat distribusi nilainya secara detail, serta melihat adanya outliers atau tidak

### Multivariate Analysis
Melakukan analisis beberapa kolom sekaligue untuk mencari hubungan antar kolom, melihat apakah feature meliki korelasi dengan target, atau apakah ada feature yang memiliki korelasi kuat dengan feature yang lain.

## Data Preprocessing
Data preprocessing adalah proses untuk membersihkan data agar data dapat digunakan dan mempermudah proses analisis data dalam machine learning.

### Data Cleaning
Pada tahap ini data akan dibersihkan melalui beberapa proses seperti mengisi nilai yang hilang, menghaluskan noisy data, dan menyelesaikan inkonsistensi yang ditemukan.

### Feature Encoding
Pada tahap ini akan mengubah feature categorical menjadi feature numeric.

### Feature Transformation
Akan dilakukan scaling data dengan menggunakan standardization

### Class Imbalance
Menyeimbangkan data target supaya data seimbang atau tidak timpang.

## Data Modeling
Pada tahap ini akan dilakukan modeling data terhadap data yang sudah di pre-procesing dengan menggunakan metode supervised learning classification, dengan menggunakan beberapa algoritma classification seperti logistic regression, decision tree, random forest, xgboost dan catboost.
