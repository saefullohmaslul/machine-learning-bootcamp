## Tipe Machine Learning:

- Supervised Learning
  Menggunakan dataset **memiliki label** untuk memprediksi target label.

- Unsupervised Learning
  Menggunakan dataset **tidak memiliki label** untuk mempelajari struktur data.

- Semi-Supervised Learning
  Menggunakan dataset **sebagian memiliki label** untuk memprediksi target label.  

- Reinforcement Learning
  Menggunakan dataset **tidak memiliki label** untuk mempelajari keputusan yang diambil.

## Imbalance

Data yang memiliki proporsi target label yang tidak seimbang.

## Effect Imbalance

- Model akan lebih mudah mempelajari pola yang berlaku untuk kelas mayoritas daripada minoritas
- Model cenderung memprediksi semua sampel sebagai kelas mayoritas tanpa memperharikan kelas minoritas

## Penanganan Imbalance

**Oversampling**
Memperbanyak minoritas dengan data baru hasil prediksi.

**Undersampling**
Mengurangi mayoritas dengan menghapus data sehingga kuantitas yang mirip minoritas.

## Algoritma Undersampling

**Tomek Links**
```
tl = TomekLinks(sampling_strategy='majority')
```

**Near Miss**
```
near = NearMiss(sampling_strategy='majority')
```

## Algoritma Oversampling

**SMOTE**
```
smote = SMOTE(sampling_strategy='minority')
```

## Alternative For Classification Case

**K-Nearest Neighbour**

KNN adalah algoritma klasifikasi yang mengklasifikasikan data berdasarkan data pembelajaran yang paling mirip dengan data yang akan diprediksi.

Advantages:
- Teknik sederhana yang mudah diimplementasikan
- Pembangunan model yang murah
- Skema klasifikasi yang sangat fleksibel
- Cocok baik untuk kasis multi class maupun multi label
Disadvantages:
- Prediksi data yang tidak diketahui relatif mahal secara komputasi terutama jika ukuran training data cukup besar karna membutuhkan perhitungan jarak dari seluruh data yang disimpan
- Akurasi dapat terpengaruh secara signifikan oleh adanya fitur yang berisik atau tidak relevan

**Naive Bayes**

Metode klasifikasi yang didasari oleh theorema bayesian dengan asumsi setiap fitur saling independent satu sama lain (naive).

Advantages:
- Sederhana dan mudah diimplementasikan.
- Efisien secara komputasi. Hanya menyimpan angka-angka probability dan statistic dari training data.
- Robust terhadap fitur yang tidak relevan.
Disadvantages:
- Asumsi fitur saling independent tidak selalu terpenuhi.
- Sensitif terhadap distribusi data. Jika data test berbeda dengan data training, maka model akan memberikan hasil yang buruk.
- Menangani nilai yang hilang dengan mengabaikan data.
