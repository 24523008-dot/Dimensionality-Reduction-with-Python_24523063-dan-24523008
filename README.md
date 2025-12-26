# Dimensionality-Reduction-with-Python_24523063-dan-24523008

## Deskripsi Kasus

Dataset handwritten digits memiliki jumlah fitur yang tinggi, di mana setiap citra direpresentasikan sebagai vektor piksel berdimensi besar. Kondisi ini menyulitkan proses eksplorasi data dan visualisasi pola, khususnya untuk melihat struktur atau cluster antar kelas digit.

Pada proyek ini dilakukan analisis perbandingan metode reduksi dimensi, yaitu Principal Component Analysis (PCA) dan t-Distributed Stochastic Neighbor Embedding (t-SNE). Tujuannya adalah menentukan metode reduksi dimensi yang lebih sesuai untuk visualisasi cluster serta memahami bagaimana masing-masing metode merepresentasikan struktur data berdimensi tinggi ke dalam ruang dua dan tiga dimensi.

---

## Dataset yang Digunakan

Dataset yang digunakan adalah Digits Dataset dari sklearn.datasets.

Karakteristik dataset:
- Berisi citra angka tulisan tangan (0–9)
- Setiap citra berukuran 8×8 piksel
- Total fitur: 64 fitur numerik
- Label kelas: 10 digit (0–9)

Dataset ini sering digunakan sebagai contoh klasik dalam machine learning karena memiliki dimensi yang cukup tinggi dan pola kelas yang jelas, sehingga cocok untuk eksperimen reduksi dimensi dan visualisasi data.

---

## Ringkasan Metode

### Pra-pemrosesan Data
Sebelum reduksi dimensi, data dinormalisasi menggunakan StandardScaler. Tahap ini penting karena PCA dan t-SNE sensitif terhadap perbedaan skala fitur.

### Principal Component Analysis (PCA)
PCA digunakan untuk mereduksi dimensi data menjadi dua dan tiga dimensi. PCA bekerja dengan memaksimalkan variansi data dan menghasilkan komponen utama yang bersifat linier.

### t-Distributed Stochastic Neighbor Embedding (t-SNE)
t-SNE digunakan sebagai metode non-linier untuk mereduksi data ke ruang dua dimensi dengan tujuan mempertahankan hubungan lokal antar data dan menampilkan cluster dengan jarak yang lebih jelas.

---

## Analisis Hasil

Hasil reduksi dimensi menunjukkan perbedaan karakteristik yang jelas antara PCA dan t-SNE. PCA mampu menangkap struktur global data dan mempertahankan variasi utama, namun pemisahan antar kelas digit masih terlihat saling tumpang tindih, terutama pada visualisasi dua dimensi.

Sebaliknya, t-SNE menghasilkan visualisasi cluster yang lebih terpisah dan jelas. Digit-digit dengan karakteristik serupa cenderung membentuk kelompok yang kompak, sehingga hubungan lokal antar data lebih mudah diamati. Hal ini menunjukkan bahwa t-SNE lebih efektif untuk tujuan visualisasi cluster pada dataset digit.

Secara keseluruhan, PCA lebih sesuai digunakan untuk analisis awal dan reduksi dimensi berbasis variansi, sedangkan t-SNE lebih unggul dalam menampilkan struktur cluster secara visual. Oleh karena itu, untuk keperluan visualisasi dan eksplorasi cluster, t-SNE merupakan metode yang lebih representatif pada kasus ini.
