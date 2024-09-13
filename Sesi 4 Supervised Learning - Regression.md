## Tipe Machine Learning

Terdapat 2 tipe machine learning:
- Supervised learning
- Unsupervised learning

Supervised Learning dibagi menjadi 2:
- Regresi: targetnya continous
- Klasifikasi: targetnya discrete

## Regression

Tardapat X dan Y:
- X adalah feature
- Y adalah target
X dan Y bisa terdapat lebih dari satu.

Tujuan regresi adalah untuk memodelkan terlebih dahulu target. Setelah mendapatkan model baru bisa melakukan prediksi.

Algoritma regresi ada banyak:
- Simple and multiple linear regression
- Logistic regression
- Polynomial regression
- Ridge regression and lasso regression

Cara memilik algoritma yang terbaik untuk saat ini sangat mudah, karna komputasi sangat cepat jadi bisa dicoba satu-satu algoritma yang ada.
Namun perlu dilihat juga case by case, karna setiap algoritma memiliki kelebihan dan kekurangan.

## Simple Linear Regression

Simple linear regression adalah regresi yang hanya memiliki satu feature dan satu target.

Rumus:
```
y = b0 + b1 * x
```

Dimana:
- y adalah target
- x adalah feature
- b0 adalah intercept
- b1 adalah slope

Tujuan dari simple linear regression adalah untuk mendapatkan b0 dan b1.

## Multiple Linear Regression

Multiple linear regression adalah regresi yang memiliki lebih dari satu feature dan satu target.

Rumus:
```
y = b0 + b1 * x1 + b2 * x2 + ... + bn * xn
```

Dimana:
- y adalah target
- x1, x2, ..., xn adalah feature
- b0 adalah intercept
- b1, b2, ..., bn adalah slope

## Poolynomial Regression

Polynomial regression adalah regresi yang memiliki feature yang berbentuk polynomial.

Rumus:
```
y = b0 + b1 * x + b2 * x^2 + ... + bn * x^n
```

Dimana:
- y adalah target
- x adalah feature
- b0 adalah intercept
- b1, b2, ..., bn adalah slope

## Logistic Regression

Logistic regression adalah regresi yang targetnya berbentuk discrete.

Rumus:
```
y = 1 / (1 + e^-(b0 + b1 * x))
```

Dimana:
- y adalah target
- x adalah feature
- b0 adalah intercept
- b1 adalah slope

## Ridge Regression and Lasso Regression

Ridge regression dan lasso regression adalah regresi yang memiliki regularisasi.

Rumus:
```
Ridge: y = b0 + b1 * x1 + b2 * x2 + ... + bn * xn + alpha * sum(bi^2)
Lasso: y = b0 + b1 * x1 + b2 * x2 + ... + bn * xn + alpha * sum(|bi|)
```

Dimana:
- y adalah target
- x1, x2, ..., xn adalah feature
- b0 adalah intercept
- b1, b2, ..., bn adalah slope
- alpha adalah hyperparameter

## Modeling

Ibaratkan membuat machine learning itu seperti mengajari anak kecil. Dimulai dari memberikan data, lalu anak kecil akan belajar dari data tersebut. Setelah anak kecil belajar, kita akan memberikan soal baru untuk anak kecil tersebut.

Dalam menentukan model, diawali dengan asumsi, dan antara feature tidak boleh memiliki korelasi yang tinggi. Apabila feature memiliki korelasi yang tinggi, maka akan terjadi multicollinearity. Sehingga salah satu feature harus dihilangkan.

### Aturan Dalam Modeling

Semua data tidak bisa digunakan untuk train model, harus dibagi menjadi beberapa porsi untuk test data. Tujuannya adalah agar model dapat bekerja baik terhadap data yang belum pernah dilihat. Kita bisa membaginya menjadi:
- 80:20 - Training 20% dan Testing 80%
- 70:30 - Training 30% dan Testing 70%
- 70:15:15 - Training 15%, Validation 15%, dan Testing 70%

## Model Evaluation

### R-Squared Score (R2)

R-Squared Score adalah metode evaluasi yang mengukur seberapa baik model kita dalam memprediksi target. Semakin mendekati 1, maka semakin baik model kita.

Rumus:
```
R2 = 1 - (sum((y - y_pred)^2) / sum((y - y_mean)^2))
```

R2 = 0: model tidak dapat menjelaskan variasi apapun dalam data
R2 = 1: model dapat menjelaskan semua variasi dalam data

### Root Mean Squared Error (RMSE)

RMSE adalah metode evaluasi yang mengukur seberapa baik model kita dalam memprediksi target. Semakin kecil RMSE, maka semakin baik model kita.

Rumus:
```
RMSE = sqrt(sum((y - y_pred)^2) / n)
```

RMSE = 0: model dapat memprediksi target dengan sempurna
RMSE > 0: model tidak dapat memprediksi target dengan sempurna

