## Pendahuluan: Apa itu Streamlit?

**Streamlit** adalah framework open-source yang memungkinkan pembuatan aplikasi web interaktif dari skrip Python dengan cepat dan mudah. Digunakan secara luas oleh komunitas data science, Streamlit memungkinkan kita membuat **dashboard** untuk memvisualisasikan data atau membuat aplikasi yang menggabungkan model machine learning.

### Manfaat Streamlit:

- **Cepat dan mudah**: Aplikasi dapat dibangun hanya dengan beberapa baris kode.
- **Integrasi dengan pustaka Python**: Kompatibel dengan berbagai library seperti Pandas, Matplotlib, dan Scikit-learn.
- **Widget sederhana**: Menambahkan input pengguna semudah mendeklarasikan variabel.

## Memulai dengan Streamlit
### Instalasi:

1. **Anaconda**: Instalasi Python dan pustaka yang dikelola menggunakan **Anaconda Navigator** untuk memudahkan pembuatan environment.
2. **VS Code**: Editor kode yang digunakan untuk menulis skrip Streamlit.

### Membuat Virtual Environment:

1. Buat environment baru di Anaconda.
2. Instal Streamlit menggunakan `pip install streamlit`.
3. Jalankan perintah `streamlit run app.py` untuk melihat aplikasi di browser.

## Struktur Aplikasi Streamlit

Setiap aplikasi Streamlit mengikuti struktur sederhana:

- **`app.py`**: File utama di mana kode ditulis.
- **Fungsi konfigurasi**: Gunakan `st.set_page_config()` untuk mengatur judul halaman, ikon, layout, dan pengaturan sidebar.
- **Menampilkan teks**: `st.write()` digunakan untuk menampilkan teks atau hasil. Kita juga dapat menggunakan format lain seperti **judul** atau **markdown** untuk menampilkan teks yang terstruktur.

---

## Input Widget dalam Streamlit

Streamlit menyediakan berbagai widget input untuk berinteraksi dengan pengguna:

- **st.button**: Tombol yang mengembalikan nilai **True** saat diklik.
- **st.checkbox**: Kotak centang yang dapat diaktifkan atau dinonaktifkan.
- **st.radio**: Opsi yang memungkinkan pengguna memilih satu nilai dari beberapa opsi.
- **st.selectbox**: Opsi dropdown untuk memilih nilai tunggal.
- **st.slider dan st.number_input**: Widget yang meminta input numerik.
- **st.text_input dan st.text_area**: Input teks singkat atau panjang.

Streamlit juga mendukung input yang lebih kompleks seperti **tanggal (date_input)**, **waktu (time_input)**, dan **pemilih warna (color_picker)**.

## Media dalam Streamlit

Aplikasi Streamlit dapat menampilkan media seperti:

- **Gambar**: Gunakan `st.image` bersama dengan library **PIL** untuk menampilkan gambar.
- **Audio**: Gunakan `st.audio` untuk memutar audio dalam berbagai format.
- **Video**: `st.video` dapat digunakan untuk menampilkan video dalam format yang didukung.

## Layout dan Kontainer

Streamlit mendukung berbagai elemen untuk mengatur tata letak aplikasi:

- **st.container**: Kontainer untuk mengelompokkan elemen dalam satu area.
- **Sidebar**: Sidebar interaktif yang collapsible, digunakan untuk menampilkan objek secara terpisah dari halaman utama.
- **st.columns**: Digunakan untuk mengelompokkan objek secara horizontal.
- **st.expander**: Kontainer collapsible yang dapat menampilkan lebih banyak elemen saat dibuka.
- **st.tabs**: Membagi konten aplikasi ke dalam beberapa tab, memudahkan navigasi di antara grup konten yang terkait.

## Membangun Aplikasi Streamlit dengan Model Machine Learning

Langkah-langkah untuk membangun aplikasi Streamlit yang menerima input pengguna, memprosesnya dengan model machine learning, dan menampilkan output:

1. **Mengimpor model**: Muat model machine learning yang sudah dilatih sebelumnya menggunakan pustaka seperti **joblib** atau **pickle**.
2. **Menerima input**: Gunakan widget input seperti **st.text_input** atau **st.slider** untuk menerima input dari pengguna.
3. **Prediksi output**: Setelah menerima input, masukkan data tersebut ke dalam model dan tampilkan hasil prediksi kepada pengguna.
4. **Visualisasi hasil**: Tampilkan hasil prediksi menggunakan `st.write` atau `st.plot` jika membutuhkan grafik.

## Penggunaan Gambar dan Media dalam Aplikasi

Untuk membuat aplikasi lebih menarik, kita dapat menambahkan gambar dengan `st.image`. Misalnya, menampilkan gambar **Iris** pada aplikasi klasifikasi Iris dataset. Gambar dapat disesuaikan ukurannya dan diberi keterangan menggunakan parameter **caption**.

## Kesimpulan

Streamlit memudahkan para pengembang dalam membangun aplikasi web interaktif dengan integrasi yang kuat terhadap model machine learning. Dari menerima input hingga menampilkan hasil prediksi, Streamlit menyediakan berbagai komponen siap pakai yang sangat fleksibel. Bagi siapa pun yang ingin membuat dashboard atau aplikasi berbasis data, Streamlit adalah pilihan yang cepat dan efisien.