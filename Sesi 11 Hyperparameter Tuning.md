## Hyperparameter Tuning

Hyperparameter tuning adalah proses untuk memilih nilai optimal dari **hyperparameter** pada model machine learning. Hyperparameter berbeda dari parameter yang dipelajari selama pelatihan model. Hyperparameter harus ditetapkan sebelum pelatihan dan sangat memengaruhi kinerja model.

### Mengapa Hyperparameter Penting?

1. **Algoritma semakin kompleks**: Banyak model memiliki banyak hyperparameter, yang membuat tuning menjadi lebih penting.
2. **Waktu tuning**: Tuning memerlukan waktu yang signifikan karena melibatkan uji coba kombinasi nilai hyperparameter.
## Parameter vs Hyperparameter

- **Parameter**: Nilai yang dipelajari model dari data selama pelatihan, seperti koefisien dalam regresi linear.
- **Hyperparameter**: Nilai yang harus ditetapkan sebelum pelatihan, seperti jumlah pohon di random forest atau laju pembelajaran dalam gradient descent.

### Contoh Hyperparameter:
- **Logistic Regression**: Penalti (`penalty`), laju pembelajaran (`solver`), dan jumlah iterasi (`max_iter`).
- **Random Forest**: Jumlah pohon (`n_estimators`), kedalaman maksimum (`max_depth`), dan jumlah fitur yang dipertimbangkan (`max_features`).
## Proses Hyperparameter Tuning

Tuning hyperparameter memerlukan pemahaman yang baik tentang model yang digunakan, termasuk:

1. **Memahami dokumentasi**: Mengidentifikasi hyperparameter yang tersedia dan penting untuk di-tuning dari dokumentasi model.
2. **Memilih hyperparameter yang tepat**: Tidak semua hyperparameter memiliki pengaruh yang signifikan. Beberapa hanya mempercepat proses atau memberikan kontrol tambahan.
## Grid Search

**Grid Search** adalah metode brute-force untuk menemukan kombinasi hyperparameter terbaik. Metode ini mencoba semua kombinasi nilai hyperparameter yang ditentukan secara sistematis dan mengevaluasi performanya menggunakan cross-validation.

### Proses Grid Search:

1. Tentukan model yang akan digunakan.
2. Pilih hyperparameter yang akan di-tuning.
3. Tentukan rentang nilai untuk setiap hyperparameter.
4. Jalankan GridSearchCV untuk mencoba semua kombinasi.

Meskipun metode ini menjamin menemukan kombinasi optimal, Grid Search bisa sangat mahal dari segi waktu dan komputasi, terutama jika jumlah hyperparameter dan nilai yang diuji besar.

## Random Search

**Random Search** adalah alternatif dari Grid Search. Alih-alih mencoba semua kombinasi, Random Search memilih kombinasi hyperparameter secara acak dari rentang yang ditentukan. Hal ini mengurangi jumlah percobaan secara signifikan dan memungkinkan tuning yang lebih cepat.

### Keuntungan Random Search:

1. **Efisiensi**: Tidak mencoba semua kombinasi, sehingga lebih cepat.
2. **Tidak semua hyperparameter penting**: Random Search memungkinkan kita untuk fokus pada kombinasi yang lebih berpotensi memberikan hasil yang baik.

Studi oleh **Bengio & Bergstra (2012)** menunjukkan bahwa hanya sebagian kecil hyperparameter yang benar-benar penting, sehingga Random Search dapat memberikan hasil yang mendekati optimal dengan lebih cepat dibandingkan Grid Search.

## Perbandingan Grid Search vs Random Search

- **Grid Search**: Mencoba semua kombinasi hyperparameter, membutuhkan waktu yang lebih lama, tetapi menjamin menemukan kombinasi terbaik.
- **Random Search**: Mencoba subset acak dari kombinasi hyperparameter, lebih cepat, tetapi belum tentu menemukan kombinasi terbaik.

### Kapan menggunakan Grid Search atau Random Search?

- **Random Search** lebih cocok jika Anda memiliki banyak hyperparameter atau data yang besar, dan waktu terbatas.
- **Grid Search** lebih baik jika Anda ingin menjamin hasil terbaik dan memiliki waktu serta resource komputasi yang cukup.

## Informed Search (Pencarian Terinformasi)

Informed search adalah pendekatan yang menggabungkan **Random Search** dan **Grid Search** untuk efisiensi yang lebih baik. Proses ini dimulai dengan Random Search untuk mengeksplorasi ruang hyperparameter secara luas, kemudian diikuti oleh Grid Search di area yang lebih fokus berdasarkan hasil dari Random Search.

### Keuntungan:

1. **Optimalisasi efisien**: Menjaga keseimbangan antara kecepatan Random Search dan ketelitian Grid Search.
2. **Penggunaan resource yang lebih efektif**: Mengurangi waktu komputasi sambil tetap fokus pada area yang menjanjikan.