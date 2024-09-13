## Bias dan Variance

Bias adalah perbedaan antara rata-rata hasil prediksi model yang kita develop dengan data nilai yang sebenarnya. Semakin tinggi bias, semakin buruk model kita dalam mempelajari data. Bias yang tinggi akan menyebabkan underfitting.

Variance adalah variabilitas dari prediksi model kita terhadap data yang berbeda. Semakin tinggi variance, semakin buruk model kita dalam mempelajari data. Variance yang tinggi akan menyebabkan overfitting.

Bias dan Variance adalah dua sisi dari trade-off yang harus kita pertimbangkan ketika kita membangun model machine learning. Kita harus memperhatikan kedua nilai ini agar model yang kita bangun tidak underfitting atau overfitting.

## Underfitting dan Overfitting

Underfitting adalah kondisi dimana model machine learning yang kita bangun terlalu sederhana untuk mempelajari pola pada data. Hal ini bisa diindikasikan pada data train dan test yang memiliki nilai error yang tinggi.

Overfitting adalah kondisi dimana model machine learning yang kita bangun terlalu kompleks untuk mempelajari pola pada data. Hal ini bisa diindikasikan pada data train yang memiliki nilai error yang rendah, tetapi pada data test memiliki nilai error yang tinggi.

## Trade-off Bias dan Variance

Ketika mengurangi bias, maka variance akan meningkat. Sebaliknya, ketika mengurangi variance, maka bias akan meningkat. Kita harus memperhatikan trade-off ini ketika membangun model machine learning.

Metode yang bisa digunakan untuk mengurangi bias dan variance adalah:
- Regularization
- Cross Validation
- Feature Selection

### Regularization

Tujuan dari regularization adalah untuk mengurangi kompleksitas model. Regularization dilakukan dengan menambahkan penalty terhadap kompleksitas model. Contoh dari Regularization adalah Ridge dan Lasso Regression.

**Ridge**
Menambah bobot di fungsi loss dengan menentukan lambda, semakin besar lambda semakin besar penalty yang diberikan.

Rumus:
```
rigde = loss + lambda * (slope^2)
```

**Lasso**
Digunakan ketika banyak fitur sehingga bisa diseleksi secara otomatis. Lasso akan membuat beberapa bobot menjadi 0.

Rumus:
```
lasso = loss + lambda * |slope|
```

Perbedaan utama dari rigde dan lasso adalah cara menambahkan penalty terhadap kompleksitas model.

Performa dari rigde dan lasso mirip, hal ini dapat digabung menjadi elastic net regression.

**Elastic Net Regression**
Kombinasi dari Ridge dan Lasso.

Rumus:
```
elastic_net = loss + lambda1 * (slope^2) + lambda2 * |slope|
```

### Cross Validation

Cross Validation adalah teknik validasi model yang digunakan untuk mengukur performa model machine learning. Cross Validation dilakukan dengan membagi data menjadi beberapa subset, lalu melakukan training dan testing pada subset tersebut.

### Feature Selection

Feature Selection adalah proses memilih fitur yang paling berpengaruh terhadap model machine learning. Feature Selection dilakukan untuk mengurangi kompleksitas model dan mengurangi overfitting.

Beberapa metode Feature Selection adalah:
- Univariate Selection
- Feature Importance
- Correlation Matrix with Heatmap
- Recursive Feature Elimination
- Principal Component Analysis
- Feature Selection dengan SelectFromModel

## Model Evaluation

Beberapa model evaluation yang dapat diterapkan:
- RMSE
- MAE
- MAPE

### RMSE (Root Mean Squared Error)

RMSE adalah metode untuk mengukur seberapa besar rata-rata error dari prediksi model. Semakin kecil RMSE, semakin baik model kita dalam melakukan prediksi.

Rumus:
```
RMSE = sqrt((1/n) * Σ(actual - pred)^2)
```

### MAE (Mean Absolute Error)

MAE adalah metode untuk mengukur rata-rata dari nilai absolut error dari prediksi model. Semakin kecil MAE, semakin baik model kita dalam melakukan prediksi.

Rumus:
```
MAE = (1/n) * Σ|actual - pred|
```

### MAPE (Mean Absolute Percentage Error)

MAPE adalah metode untuk mengukur rata-rata dari nilai persentase error dari prediksi model. Semakin kecil MAPE, semakin baik model kita dalam melakukan prediksi.

Rumus:
```
MAPE = (1/n) * Σ(|actual - pred| / actual) * 100
```

## Gradient Descent

Gradient Descent adalah algoritma optimasi yang digunakan untuk mencari nilai minimum dari fungsi. Gradient Descent bekerja dengan mengiterasi nilai slope dari fungsi hingga menemukan nilai minimum.

Ada beberapa tipe dari Gradient Descent:
- Batch Gradient Descent
- Stochastic Gradient Descent
- Mini Batch Gradient Descent
