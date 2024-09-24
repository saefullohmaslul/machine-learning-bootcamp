## Tipe Machine Learning

Terdapat 2 tipe machine learning:
- Supervised learning: labeled data
- Unsupervised learning: unlabeled data

## Unsupervised Learning

Unsupervised Learning adalah pendekatan **machine learning** di mana algoritma belajar dari data tanpa diberi label atau jawaban yang diinginkan. Tujuannya adalah untuk menemukan pola atau struktur tersembunyi dalam data tersebut. Contoh penerapannya termasuk:

- **Clustering** (pengelompokan data),
- **Dimensionality Reduction** (reduksi dimensi),
- **Anomaly Detection** (deteksi anomali), dan
- **Association Rule Mining** (pencarian aturan asosiasi).

Keuntungan utama dari unsupervised learning adalah lebih mudah mendapatkan data tanpa label daripada data berlabel, dan penggunaannya semakin penting dalam berbagai bidang seperti pengelompokan pasien berdasarkan ekspresi gen atau kelompok pelanggan berdasarkan perilaku belanja.
### Tantangan:

Unsupervised learning lebih subjektif dibandingkan supervised learning karena tidak ada jawaban yang jelas dan melibatkan pemahaman mendalam tentang data. Tantangan lainnya termasuk:

- Menentukan jumlah cluster,
- Variasi hasil karena inisialisasi K-means yang berbeda,
- Penilaian performa metode unsupervised learning.

## Clustering

Clustering adalah teknik yang digunakan untuk mengelompokkan data menjadi beberapa grup berdasarkan kemiripan di antara data tersebut. Semakin tinggi tingkat kemiripan dalam satu grup (intra-cluster), dan semakin besar perbedaan antar grup (inter-cluster), semakin baik hasil clustering-nya.

### Penerapan Clustering:

- **Pemasaran**: Mengelompokkan pelanggan berdasarkan preferensi.
- **Segmentasi Pasar**: Berdasarkan karakteristik demografi.
- **Segmentasi Pasien**: Berdasarkan profil kesehatan.
- **Sistem Rekomendasi**: Rekomendasi item kepada pengguna dengan preferensi serupa.

### Intuisi Clustering:

Kemiripan antara dua data bisa diukur menggunakan berbagai metrik seperti:

- **Euclidean Distance**: Jarak terdekat antara dua titik.
- **Manhattan Distance**: Jumlah panjang ruas garis tiap sumbu.
- **Cosine Similarity**: Mengukur cosinus sudut antara dua vektor, semakin besar nilai, semakin mirip kedua vektor.

## Tipe Clustering

- **Well-separated Clusters**: Setiap cluster terpisah dengan jelas tanpa tumpang tindih.
- **Center-based Clusters**: Cluster memiliki pusat (centroid) dan data dalam cluster lebih dekat ke pusat dibanding cluster lain.
- **Contiguity-based Clusters**: Cluster dibentuk berdasarkan kedekatan data.
- **Density-based Clusters**: Cluster terbentuk berdasarkan kepadatan titik data.

## Metode Clustering

Ada berbagai metode clustering yang digunakan tergantung pada jenis data dan tujuan analisis:

### Partitional Clustering

- Membagi data menjadi sejumlah cluster secara eksklusif (setiap data hanya berada dalam satu cluster). Salah satu metode yang paling umum adalah **K-Means Clustering**.

### Hierarchical Clustering

- Membentuk cluster secara bertahap dengan menyusun hubungan antar data dalam bentuk **dendrogram**.
- Dua pendekatan yang umum digunakan adalah:
    - **Agglomerative (bottom-up)**: Menggabungkan dua titik data yang paling mirip.
    - **Divisive (top-down)**: Memulai dengan satu cluster besar lalu membaginya.

### **Density-Based Clustering**

- Cluster terbentuk berdasarkan area kepadatan tinggi yang dikelilingi oleh area dengan kepadatan rendah, contohnya algoritma **DBSCAN**.

## K-Means Clustering

Algoritma ini mengelompokkan data ke dalam **k cluster**. Setiap cluster memiliki pusat (centroid), dan data ditempatkan ke dalam cluster dengan jarak terdekat ke centroid. Proses ini bertujuan meminimalkan jarak antar data dengan centroid dalam cluster yang sama, serta memaksimalkan jarak antar centroid dari cluster yang berbeda.

### Tantangan K-Means:

- **Initial Centroid**: Pemilihan centroid awal yang acak bisa mempengaruhi hasil clustering, dan dapat menimbulkan variasi hasil. Beberapa solusi termasuk **pengulangan algoritma**, **PCA (Principal Component Analysis)**, dan **preprocessing data** untuk mengurangi noise.

### Limitasi K-Means:

1. Rentan terhadap **outliers**.
2. Menghasilkan **cluster yang berbeda** dibandingkan dengan klasifikasi data asli.
3. Tidak cocok untuk **cluster berbentuk tidak globular**.

## Hierarchical Clustering

Hierarchical clustering menghasilkan sekumpulan nested clusters yang divisualisasikan sebagai **pohon hierarki** (dendrogram). Teknik ini fleksibel karena tidak mengasumsikan jumlah cluster tertentu dan dapat memotong dendrogram untuk mendapatkan jumlah cluster yang diinginkan. Namun, metode ini memiliki kompleksitas waktu yang lebih tinggi dibandingkan metode lain.

### **Linkage Methods** dalam Hierarchical Clustering:

- **Single Linkage**: Menggunakan jarak minimum antar cluster.
- **Complete Linkage**: Jarak maksimum antar cluster.
- **Average Linkage**: Menghitung jarak rata-rata antar cluster.
- **Centroid Linkage**: Jarak antar centroid dari cluster.

## Evaluasi Kinerja Clustering

Beberapa metrik yang digunakan untuk mengevaluasi hasil clustering antara lain:

- **Sum of Squared Errors (SSE)**: Mengukur seberapa baik data cocok dengan centroid.
- **Silhouette Score**: Mengukur seberapa baik data cocok dengan cluster-nya dibandingkan dengan cluster lain.
- **Dunn Index**: Mengukur kualitas cluster berdasarkan jarak antar cluster dan jarak antar data dalam cluster.
- **Davies-Bouldin Index (DBI)**: Semakin kecil nilai DBI, semakin baik kualitas clustering.

## Menentukan Jumlah Optimal Cluster (k)

Ada beberapa metode yang digunakan untuk menentukan jumlah cluster yang optimal:

- **Elbow Method**: Mencari titik “elbow” pada plot SSE vs k, di mana penurunan SSE mulai melambat.
- **Silhouette Method**: Memilih nilai k yang menghasilkan silhouette score tertinggi.

## Hands-on Clustering

Bagian hands-on memberikan kesempatan untuk mencoba berbagai teknik clustering melalui platform pembelajaran online yang disediakan, di mana pengguna dapat belajar lebih dalam tentang bagaimana menerapkan algoritma clustering pada data.