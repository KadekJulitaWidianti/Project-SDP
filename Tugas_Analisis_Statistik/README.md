# Tugas Analisis Statistik: Deskriptif, Korelasi, dan Regresi

## 1. Informasi Penyusun

- **Nama:** `[KADEK JULITA WIDIANTI]`
- **NIM:** `[2515091010]`
- **Program Studi:** `[S1 SISTEM INFORMASI]`
- **Mata Kuliah:** Statistika dan Probabilitas

---

## 2. Deskripsi Proyek
>Dataset yang digunakan dalam proyek ini adalah data_startup_saas.csv yang berisi informasi komprehensif mengenai 
berbagai perusahaan rintisan (startup) berbasis Software as a Service (SaaS). Dataset ini mencakup beberapa 
atribut utama, yaitu Nama_Startup yang merepresentasikan identitas perusahaan, Kategori_Layanan yang menunjukkan 
jenis layanan digital yang ditawarkan, Pendapatan_Tahunan_Miliar_IDR sebagai indikator kinerja finansial utama 
perusahaan, Biaya_Akuisisi_Pelanggan_Juta_IDR yang menggambarkan besarnya biaya yang dikeluarkan untuk memperoleh 
pelanggan baru, Nilai_Pelanggan_Juta_IDR yang mencerminkan nilai ekonomi pelanggan bagi perusahaan (customer value), 
serta Tingkat_Churn_Persen yang menunjukkan persentase pelanggan yang berhenti menggunakan layanan dalam periode 
tertentu. Variabel kunci dalam analisis ini adalah Pendapatan_Tahunan_Miliar_IDR dan Nilai_Pelanggan_Juta_IDR, 
karena keduanya dianggap paling merepresentasikan hubungan antara nilai pelanggan dan performa pendapatan 
perusahaan. Tujuan utama proyek ini adalah untuk memahami karakteristik data melalui analisis statistik 
deskriptif, menguji hubungan antara Nilai_Pelanggan_Juta_IDR dan Pendapatan_Tahunan_Miliar_IDR menggunakan 
analisis korelasi guna mengetahui arah dan kekuatan hubungannya, serta membangun model regresi linear untuk 
memprediksi Pendapatan_Tahunan_Miliar_IDR dengan Nilai_Pelanggan_Juta_IDR sebagai variabel prediktor. Melalui 
pendekatan ini, diharapkan dapat diperoleh pemahaman yang lebih mendalam mengenai sejauh mana nilai pelanggan 
berkontribusi terhadap pendapatan tahunan startup SaaS, sekaligus memberikan dasar analitis bagi pengambilan 
strategis berbasis data.

---

## 3. Struktur Proyek

Proyek ini diorganisir ke dalam beberapa folder:
- `/data`: Berisi dataset mentah yang digunakan untuk analisis.
- `/scripts`: Berisi semua skrip R yang digunakan dalam analisis, diurutkan berdasarkan alur kerja.
- `/results`: Berisi output dari analisis, seperti plot, gambar, atau tabel ringkasan.

---

## 4. Cara Menjalankan Analisis

Untuk mereproduksi hasil analisis ini, ikuti langkah-langkah berikut:
1. Pastikan Anda memiliki R dan RStudio terinstal.
2. Buka proyek R ini di RStudio.
3. Instal paket yang diperlukan dengan menjalankan perintah berikut di konsol R:
   ```R
   # install.packages(c("tidyverse", "corrplot", "knitr"))
   ```
4. Jalankan skrip di dalam folder `/scripts` secara berurutan, mulai dari `01_data_preparation.R` hingga `05_analisis_regresi.R`.

---

## 5. Hasil dan Interpretasi

Di bagian ini, mahasiswa diharapkan untuk menyajikan dan menginterpretasikan hasil dari setiap tahap analisis.

### 5.1. Statistik Deskriptif
- **Ukuran Pemusatan (Mean, Median, Modus):**
  - *Tabel atau ringkasan...*
  - *Interpretasi:* Jelaskan apa arti dari nilai-nilai tersebut terkait dengan data Anda.
- **Ukuran Sebaran (Standar Deviasi, Range, Kuartil):**
  - *Tabel atau ringkasan...*
  - *Interpretasi:* Jelaskan seberapa menyebar data Anda berdasarkan nilai-nilai ini.
- **Visualisasi (Histogram/Boxplot):**
  - *Sematkan gambar plot dari folder /results...*
  - *Interpretasi:* Jelaskan wawasan apa yang Anda dapatkan dari bentuk distribusi data.

### 5.2. Uji Normalitas
- **Hasil Uji Shapiro-Wilk:**
  - *Nilai p-value...*
  - *Interpretasi:* Apakah data Anda terdistribusi normal berdasarkan hasil uji? Apa implikasinya?
- **Plot Q-Q:**
  - *Sematkan gambar plot dari folder /results...*
  - *Interpretasi:* Apakah titik-titik data mengikuti garis lurus? Apa artinya?

### 5.3. Analisis Korelasi
- **Nilai Koefisien Korelasi:**
  - *Nilai r...*
  - *Interpretasi:* Seberapa kuat dan apa arah hubungan antara dua variabel yang Anda uji? (misalnya, korelasi positif kuat, negatif lemah, atau tidak ada korelasi).
- **Visualisasi (Scatter Plot):**
  - *Sematkan gambar plot dari folder /results...*
  - *Interpretasi:* Apakah pola pada scatter plot mendukung hasil koefisien korelasi?

### 5.4. Analisis Regresi
- **Model Regresi:**
  - *Persamaan regresi: Y = b0 + b1*X*
  - *Interpretasi:* Jelaskan arti dari koefisien intercept (b0) dan slope (b1) dalam konteks data Anda.
- **Evaluasi Model (R-squared):**
  - *Nilai R-squared...*
  - *Interpretasi:* Berapa persen variasi dari variabel dependen yang dapat dijelaskan oleh model regresi Anda?
- **Visualisasi (Garis Regresi pada Scatter Plot):**
  - *Sematkan gambar plot dari folder /results...*
  - *Interpretasi:* Jelaskan bagaimana garis regresi merepresentasikan hubungan antara variabel.

---

## 6. Kesimpulan

Rangkum temuan utama dari analisis Anda dalam beberapa kalimat. Apa wawasan paling penting yang Anda peroleh?
