## Neural Networks

Neural networks adalah bagian dari **Deep Learning**, digunakan untuk memproses data dengan cara yang terinspirasi oleh cara kerja otak manusia. Konsep ini pertama kali diperkenalkan oleh **Frank Rosenblatt** pada tahun 1958, yang terinspirasi oleh bagaimana manusia belajar dan merespons lingkungan. Sejak itu, neural networks telah berkembang pesat, dan salah satu tonggak penting adalah ketika **Convolutional Neural Networks (CNN)** memenangkan **ImageNet Challenge 2012**, yang menunjukkan potensi besar dalam pengenalan gambar.

### Manfaat Neural Networks:
- **Mengatasi data tidak terstruktur** seperti gambar atau teks.
- **Menghilangkan kebutuhan akan feature engineering manual**.
- **Dapat memproses berbagai jenis data** dengan arsitektur yang disesuaikan, seperti **CNN** untuk gambar atau **RNN** untuk teks.

## Struktur Neural Networks

Neural networks terdiri dari beberapa komponen penting:

- **Neuron buatan**: Terinspirasi dari neuron biologis, neuron buatan menerima input, melakukan pemrosesan, dan menghasilkan output.
- **Lapisan**: Neural networks biasanya terdiri dari lapisan input, lapisan tersembunyi, dan lapisan output. Lapisan tersembunyi dapat terdiri dari beberapa lapisan, dan jumlah neuron dalam setiap lapisan bervariasi tergantung pada arsitektur jaringan.

Proses di dalam neuron buatan melibatkan fungsi aktivasi yang mentransformasi output menjadi non-linear, memberikan kemampuan bagi neural networks untuk memodelkan pola yang kompleks dalam data.

## Jenis Neural Networks

Terdapat beberapa jenis neural networks yang sering digunakan:

- **Feedforward Neural Networks (FNN)**: Digunakan untuk data statis seperti klasifikasi gambar. Data hanya mengalir maju dari input ke output, tanpa memori dari langkah sebelumnya.
- **Convolutional Neural Networks (CNN)**: Khusus untuk data gambar atau video, CNN menggunakan **filter** untuk mengekstraksi fitur dari data input, seperti deteksi tepi atau bentuk.
- **Recurrent Neural Networks (RNN)**: Didesain untuk memproses data urutan seperti teks atau time-series, RNN memiliki **memori internal** yang memungkinkan informasi dari langkah sebelumnya digunakan untuk langkah berikutnya.

### Aplikasi:

- **CNN**: Digunakan untuk tugas pengenalan gambar dan segmentasi objek.
- **RNN**: Sangat berguna dalam **analisis teks**, **terjemahan neural**, dan **generasi teks**.

## Activation Functions

**Fungsi aktivasi** membuat neural networks menjadi non-linear dan sangat penting dalam menentukan output dari setiap neuron. Beberapa fungsi aktivasi yang umum digunakan adalah:

- **Sigmoid**: Menghasilkan output antara 0 dan 1, cocok untuk **binary classification**.
- **Tanh**: Menghasilkan output antara -1 dan 1, digunakan untuk **hidden layers**.
- **ReLU (Rectified Linear Unit)**: Fungsi yang hanya menerima nilai positif, membuat neural networks belajar lebih cepat dan mengatasi masalah vanishing gradient.

## Membangun Neural Networks Menggunakan Keras

**Keras** adalah library populer untuk membangun neural networks di atas TensorFlow. Berikut langkah-langkah sederhana untuk membangun neural networks menggunakan Keras:

1. **Inisialisasi Model**: Menggunakan `Sequential()` untuk membuat model.
2. **Menambahkan Lapisan (Layer)**: Menambahkan **dense layer** untuk hidden layers dan output layer, di mana jumlah neuron dan fungsi aktivasi dapat disesuaikan.
3. **Kompilasi Model**: Model dikompilasi menggunakan **optimizer** seperti **Adam**, dan fungsi loss seperti **Mean Squared Error (MSE)** untuk regresi atau **categorical crossentropy** untuk klasifikasi.
4. **Pelatihan Model (Training)**: Menggunakan `model.fit()` untuk melatih model pada data training.
5. **Prediksi dan Evaluasi**: Model diuji menggunakan data test, dan performanya dievaluasi menggunakan `model.evaluate()`.