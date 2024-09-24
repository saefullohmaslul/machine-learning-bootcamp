## High Dimensionality Data

**Dimensionality** dalam machine learning mengacu pada jumlah fitur atau atribut input dalam dataset. Saat jumlah dimensi meningkat secara eksponensial, data menjadi lebih sulit untuk dianalisis. Walaupun ada keyakinan bahwa lebih banyak data dapat membantu model mempelajari pola yang lebih baik, data dengan banyak dimensi dapat memperkenalkan **noise** yang dapat menurunkan performa model.

### Curse of Dimensionality
**Curse of dimensionality** terjadi ketika jumlah fitur yang sangat tinggi membuat data menjadi renggang dan sulit untuk dianalisis. Hal ini menyebabkan model **overfit** pada data pelatihan dan kurang mampu menangani data baru. Penambahan dimensi yang tidak relevan juga meningkatkan kebutuhan resource komputasi.

### Hughes Phenomenon
Fenomena ini terjadi ketika performa model meningkat seiring bertambahnya fitur, hingga mencapai titik di mana performanya menurun saat fitur terus ditambahkan. Ini juga dikenal sebagai "overlearning."

## Dimensionality Reduction

**Dimensionality reduction** adalah teknik untuk mengurangi jumlah dimensi data dari dataset berdimensi tinggi menjadi dataset berdimensi rendah, dengan tetap mempertahankan informasi yang paling relevan. Ini dilakukan dengan mengidentifikasi dan menghapus fitur yang tidak relevan atau kurang penting.

### Manfaat Dimensionality Reduction:
1. **Mempermudah visualisasi**: Data dapat direpresentasikan dalam 2D atau 3D, sehingga lebih mudah dipahami.
2. **Meningkatkan kecepatan pelatihan model**: Dataset dengan dimensi yang lebih rendah lebih cepat diproses.
3. **Meningkatkan interpretasi model**: Model menjadi lebih sederhana dengan hanya mempertahankan fitur-fitur penting.
4. **Mengurangi overfitting**: Dengan mengurangi noise dari fitur yang tidak relevan, risiko overfitting berkurang.

## Teknik Dimensionality Reduction

Teknik ini dibagi menjadi dua kategori utama: **Feature Selection** dan **Feature Extraction**.

### **Feature Selection**
Feature selection berfokus pada memilih fitur terbaik dalam dataset. Ada beberapa metode yang digunakan, termasuk:
- **Filter Methods**: Menggunakan teknik statistik seperti variance dan correlation untuk mengidentifikasi fitur penting.
- **Wrapper Methods**: Menguji berbagai subset fitur menggunakan model machine learning dan memilih subset terbaik.
- **Embedded Methods**: Memilih fitur selama proses pelatihan model, contohnya menggunakan Decision Trees atau Regularization.

### **Feature Extraction**
Feature extraction bertujuan menciptakan fitur baru dari fitur yang ada. Teknik umum meliputi:
- **Principal Component Analysis (PCA)**: Menggabungkan fitur-fitur yang berkorelasi untuk mengurangi dimensi.
- **Linear Discriminant Analysis (LDA)**: Mencari kombinasi fitur yang memaksimalkan pemisahan antar kelas.
- **t-distributed Stochastic Neighbor Embedding (t-SNE)**: Digunakan untuk memetakan hubungan non-linear dalam data berdimensi tinggi ke ruang berdimensi rendah.

## Principal Component Analysis (PCA)

**PCA** adalah salah satu teknik **feature extraction** yang paling umum. PCA mengurangi dimensi data dengan menggabungkan fitur yang berkorelasi tinggi menjadi satu fitur yang disebut **principal component**. PCA memungkinkan kita memproyeksikan data ke dalam ruang berdimensi lebih rendah dengan tetap mempertahankan sebagian besar informasi.

### Langkah-Langkah PCA

1. **Standarisasi data**: Setiap fitur dinormalisasi agar memiliki mean 0 dan variance 1.
2. **Menghitung matriks kovarians**: Menghitung hubungan antar variabel.
3. **Menghitung eigenvector dan eigenvalue**: Menemukan komponen utama data.
4. **Mengurutkan eigenvalue**: Memilih eigenvector yang relevan berdasarkan nilai eigen terbesar.
5. **Membuat matriks proyeksi**: Memproyeksikan data ke dalam ruang berdimensi rendah.
6. **Transformasi data**: Data asli diubah melalui matriks proyeksi untuk menghasilkan dataset dengan dimensi yang lebih sedikit.

### Explained Variance

Explained variance menunjukkan berapa banyak variansi data yang dapat dijelaskan oleh setiap principal component. Dengan melihat grafik **Cumulative Explained Variance**, kita dapat menentukan berapa banyak komponen utama yang dibutuhkan untuk menjelaskan sebagian besar informasi dalam data.

## Studi Kasus PCA

Dokumen ini memberikan contoh implementasi PCA dengan **Iris Dataset**, yang memiliki empat fitur:

1. Dataset distandarisasi.
2. Menghitung matriks kovarians.
3. Menghitung eigenvector dan eigenvalue.
4. Memilih eigenvector terbesar.
5. Menghitung explained variance.
6. Membuat matriks proyeksi dan memproyeksikan data ke subspace berdimensi lebih rendah.

Dengan PCA, dataset 4-dimensi ini dapat direduksi menjadi 2-dimensi sambil mempertahankan 95.8% informasi asli.

## Linear Discriminant Analysis (LDA)

**LDA** berbeda dengan PCA karena bersifat supervised dan memaksimalkan pemisahan antara kelas-kelas yang berbeda. LDA memproyeksikan data ke ruang fitur yang baru, di mana jarak antar kelas lebih jauh, namun jarak antar data dalam kelas yang sama lebih dekat.

## t-SNE (t-distributed Stochastic Neighbor Embedding)

**t-SNE** digunakan untuk dimensionality reduction dalam data berdimensi tinggi yang mengandung hubungan non-linear. Teknik ini sering digunakan untuk memvisualisasikan data yang kompleks dalam bentuk 2D atau 3D.