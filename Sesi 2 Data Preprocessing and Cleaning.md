---
tags:
  - bootcamp
  - dqlab
  - ml
---
## Data Preprocessing

Preprocessing adalah proses persiapan data sebelum dilakukan analisis. Proses ini melibatkan berbagai teknik seperti cleaning, transforming, dan encoding.

**Kenapa harus preprocessing?**

Input yang tidak baik akan menghasilkan output yang tidak baik pula. Hasil model tidak akan optimal apabila input yang diberikan memiliki kualitas yang jelek.

Contoh di dalam data terdapat informasi yang tidak sesuai dengan keadaan sebenarnya, seperti umur yang bernilai negatif, atau data yang hilang.

## Data Cleaning

Data cleaning adalah proses mengidentifikasi dan memperbaiki (atau menghapus) data yang tidak lengkap, tidak akurat, tidak relevan, atau tidak terkonsisten.

**Kenapa harus data cleaning?**

Data yang kotor akan menghasilkan model yang buruk. Data yang tidak lengkap, tidak akurat, atau tidak relevan akan menghasilkan model yang tidak akurat.

## Basic Cleaning

### Duplicate Values

Hal ini dapat terjadi karena kesalahan operator dalam pengumpulan atau pemrosesan data. Data diusahakan unique untuk setiap row, sehingga tidak ada data yang sama.

### Handling Missing Value

Data yang hilang akan menghasilkan model yang buruk. Ada beberapa cara untuk mengatasi missing value:
- Leave as it: biarkan saja data yang kosong tersebut
- Drop it: hapus data yang kosong tersebut apabila data tersebut tidak terlalu penting
- Imputation: isi data yang kosong tersebut dengan nilai yang masuk akal

### Rename Columns

Format standar untuk nama kolom adalah snake_case
- ID_: id
- Name: name
- G: gender

### Drop Columns

Hal ini tidak disarankan, namun apabila kolom tersebut tidak penting, maka kolom tersebut dapat dihapus.

Cara menghapusnya yaitu membuat data frame baru tanpa kolom tersebut.

## Deteksi Outlier dengan Box Plot

Outlier adalah data yang berbeda dari data lainnya. Outlier dapat mempengaruhi hasil analisis data. Contoh:

Jumlah pendapatan pekerja di indonesia, ketika terdapat outliter, hasil rata-rata gajinya sangat tinggi. Padahal realitasnya tidak demikian.

Untuk menghilangkan outlier, dapat menggunakan box plot:
1. Hitung nilai median
2. Hitung nilai min dan max
3. Hitung kuartil bawah Q1 dan kuartil atas Q3
4. Hitung panjang langkah dengan rumus `1.5 * (Q3-Q1)`
5. Hitung pagar dalam = `Q1 - langkah`
6. Hitung pagar luar = `Q3 + langkah`

> Data yang berada di luar pagar luar dan pagar dalam adalah outlier.

**Apa itu kuartil?**

Q1 : 25% data terkecil
Q2 : 50% data terkecil
Q3 : 75% data terkecil

Q -> Quat: 1/4
P -> Percentil: 1/100

Contoh:
```
data = [1,2,3,4,5,6,7,8,9,10]

Q2 = 5
Q1 = 3
Q3 = 7
```

Penentuan Q1 - Q3 datanya harus diurutkan terlebih dahulu.

Terdapat beberapa istilah lain:
- Inter Quartile Range (IQR): Q3 - Q1
- Step: Inter Quartile Range * 1.5
- Max Limit: Q3 + Step
- Min Limit: Q1 - Step

Dikatakan outlier jika

```
X < Min Limit atau X > Max Limit untuk setiap X yang ada di dalam data
```

## Transformasi Data

Proses mengubah data mentah menjadi format atau struktur yang lebih cocok untuk model/algoritma dan juga penemuan data secara umum.

- Scaling: mengubah data ke dalam skala tertentu
- Normalization: berusaha mengubah data sesuai distribusi normal.

## Feature Encoding

Feature encoding adalah proses mengubah data kategorikal menjadi data numerik.

Contoh:
- Status perkawinan: single, married, divorced
	- Single: 1
	- Married: 2
	- Divorced: 3
- Jenis kelamin: laki-laki, perempuan
	- Laki-laki: 1
	- Perempuan: 2
