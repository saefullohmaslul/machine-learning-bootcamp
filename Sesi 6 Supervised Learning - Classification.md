## Tipe Machine Learning:

- Supervised Learning
  Menggunakan dataset **memiliki label** untuk memprediksi target label.

- Unsupervised Learning
  Menggunakan dataset **tidak memiliki label** untuk mempelajari struktur data.

- Semi-Supervised Learning
  Menggunakan dataset **sebagian memiliki label** untuk memprediksi target label.  

- Reinforcement Learning
  Menggunakan dataset **tidak memiliki label** untuk mempelajari keputusan yang diambil.

## Classification Type

### Binary

Binary Classification adalah tipe klasifikasi yang hanya memiliki dua target label.
Contoh:
- Apakah email ini spam atau tidak.

### Multi-Class

Multi-Class Classification adalah tipe klasifikasi yang memiliki lebih dari dua target label.
Contoh:
- Jenis bunga: mawar, tulip, atau matahari.

### Multi-Label

Target lebih dari satu dan data bisa memiliki lebih dari 1 target label
Contoh:
- Foto manusia, bisa memiliki label: pria, dewasa, sedang berdiri.

### Imbalanced Data

Data yang memiliki proporsi target label yang tidak seimbang.

## Algoritma Klasifikasi

### Support Vector Machine

Support Vector Machine (SVM) adalah algoritma klasifikasi yang memisahkan data dengan membuat hyperplane dengan margin maksimal. SVM bisa digunakan untuk klasifikasi binary dan multi-class.

### Decision Tree

Decision Tree adalah algoritma klasifikasi yang menggunakan struktur pohon untuk mengklasifikasikan data. Decision Tree bisa digunakan untuk klasifikasi binary dan multi-class.

### Random Forest

Random Forest adalah algoritma klasifikasi yang menggunakan beberapa decision tree untuk mengklasifikasikan data. Random Forest bisa digunakan untuk klasifikasi binary dan multi-class.

### K-Nearest Neighbors

K-Nearest Neighbors (KNN) adalah algoritma klasifikasi yang mengklasifikasikan data berdasarkan data pembelajaran yang paling mirip dengan data yang akan diprediksi.

## Evaluasi Model Klasifikasi

- True Positive (TP)
  Contoh: Seorang pasien positif terkena penyakit dan hasil prediksi model juga positif.

- True Negative (TN)
  Contoh: Seorang pasien negatif terkena penyakit dan hasil prediksi model juga negatif.

- False Positive (FP)
  Contoh: Seorang pasien negatif terkena penyakit dan hasil prediksi model positif.

- False Negative (FN)
  Contoh: Seorang pasien positif terkena penyakit dan hasil prediksi model negatif.

### Akurasi

Adalah metode evaluasi yang menghitung rasio antara jumlah data yang diprediksi benar dengan total jumlah data yang diuji.

```
akurasi = (TP + TN) / (TP + TN + FP + FN)
```

### Precision

Adalah metode evaluasi yang menghitung rasio jumlah data yang diprediksi benar positif dengan total data yang diprediksi positif.

```
precision = TP / (TP + FP)
```

### Recall

Adalah metode evaluasi yang menghitung rasio antara jumlah data yang diprediksi benar positid dengan total data sebenarnya positif.

```
recall = TP / (TP + FN)
```

### F1-Score

Adalah metode evaluasi yang menghitung nilai rata-rata harmonis antara precision dan recall. Berkisar 0 hingga 1 dimana 1 menunjukan kinerja model yang sangat baik dan 0 menunjukan kinerja model yang buruk.
  
```
  f1-score = 2 * (precision * recall) / (precision + recall)
```
