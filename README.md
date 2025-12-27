# Tugas Analisis Statistik: Deskriptif, Korelasi, dan Regresi

## 1. Informasi Penyusun

- **Nama:** `[KADEK JULITA WIDIANTI]`
- **NIM:** `[2515091010]`
- **Program Studi:** `[S1 SISTEM INFORMASI]`
- **Mata Kuliah:** Statistika dan Probabilitas

---

## 2. Deskripsi Proyek

> Dataset yang digunakan dalam proyek ini adalah data_startup_saas.csv yang berisi informasi komprehensif mengenai berbagai perusahaan rintisan (startup) berbasis Software as a Service (SaaS). Dataset ini mencakup beberapa informasi penting, yaitu Nama_Startup yang merepresentasikan identitas perusahaan, Kategori_Layanan yang menunjukkan jenis layanan digital yang ditawarkan, Pendapatan_Tahunan_Miliar_IDR sebagai ukuran pendapatan perusahaan dalam satu tahun, Biaya_Akuisisi_Pelanggan_Juta_IDR yang menggambarkan besarnya biaya yang dikeluarkan untuk memperoleh pelanggan baru, Nilai_Pelanggan_Juta_IDR yang mewakili nilai ekonomi pelanggan bagi perusahaan (customer value), serta Tingkat_Churn_Persen yang menunjukkan persentase pelanggan yang berhenti menggunakan layanan. Variabel kunci dalam analisis ini adalah Pendapatan_Tahunan_Miliar_IDR dan Nilai_Pelanggan_Juta_IDR, arena analisis difokuskan pada hubungan utama yang ingin dikaji, yaitu bagaimana nilai yang dihasilkan dari pelanggan berkaitan dengan pendapatan yang diperoleh perusahaan. Tujuan utama proyek ini adalah untuk memahami karakteristik data melalui analisis statistik deskriptif, menguji hubungan antara Nilai_Pelanggan_Juta_IDR dan Pendapatan_Tahunan_Miliar_IDR menggunakan analisis korelasi guna mengetahui arah dan kekuatan antara 2 variabel ini, serta membangun model regresi linier untuk memprediksi Pendapatan_Tahunan_Miliar_IDR dengan Nilai_Pelanggan_Juta_IDR sebagai variabel prediktor. Melalui pendekatan ini, diharapkan dapat memperoleh pemahaman yang lebih mendalam mengenai sejauh mana nilai pelanggan berkontribusi terhadap pendapatan tahunan startup SaaS, sekaligus memberikan analisis dasar untuk pengambilan strategi atau keputusan berbasis data.
	
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
  > *Hasil:* Analisis statistik deskriptif untuk ukuran pemusatan data terhadap variabel Pendapatan_Tahunan_Miliar_IDR dari 650 startup SaaS menunjukkan nilai mean sebesar 31,88 miliar IDR, median 31,30 miliar IDR, dan modus 1,87 miliar IDR.
  > *Interpretasi:*
    Berdasarkan hasil analisis statistik deskriptif terhadap data startup SaaS, diperoleh nilai rata-rata (mean) pendapatan tahunan sebesar 31,88 miliar IDR, sedangkan nilai median sebesar 31,30 miliar IDR. Kedua nilai ini relatif berdekatan, yang menunjukkan bahwa secara umum distribusi pendapatan tidak terlalu miring dan tidak didominasi oleh satu sisi ekstrem secara berlebihan. Nilai mean dalam hal ini memberikan gambaran umum mengenai skala pendapatan industri secara keseluruhan.
	Namun demikian, analisis menjadi lebih bermakna ketika memperhatikan nilai modus pendapatan tahunan, yaitu 1,87 miliar IDR. Nilai ini jauh lebih rendah dibandingkan mean dan median, yang menunjukkan bahwa pendapatan yang paling sering muncul dalam data berada pada tingkat yang relatif kecil. Temuan ini mengungkap bahwa mayoritas startup SaaS masih memiliki pendapatan rendah, meskipun terdapat sejumlah startup yang telah mencapai pendapatan menengah hingga tinggi.
	Perbedaan antara mean, median, dan modus ini mengindikasikan adanya kesenjangan kinerja dalam industri SaaS. Sejumlah kecil startup dengan pendapatan sangat tinggi berkontribusi besar dalam mendorong nilai rata-rata, sementara sebagian besar startup berada pada tingkat pendapatan yang lebih rendah. Pola ini umum terjadi dalam ekosistem startup, di mana keberhasilan segelintir perusahaan besar dapat memengaruhi statistik agregat (nilai statistik yang mewakili keseluruhan startup dalam dataset) secara signifikan.
	Dengan demikian, rata-rata pendapatan yang tinggi tidak serta-merta mencerminkan bahwa seluruh startup telah sukses secara finansial, melainkan merupakan hasil dari distribusi pendapatan yang tidak merata. Oleh karena itu, penggunaan mean, median, dan modus secara bersama-sama memberikan pemahaman yang lebih utuh mengenai struktur pendapatan startup SaaS untuk dasar pengambilan keputusan, serta menjadi dasar yang penting sebelum dilakukan analisis lanjutan seperti korelasi dan regresi.

- **Ukuran Sebaran (Standar Deviasi, Range, Kuartil):**
  - *Hasil:* Pendapatan startup SaaS menunjukkan variasi yang signifikan dengan standar deviasi sebesar 19,79 miliar IDR dan rentang yang lebar dari 1 hingga 66,89 miliar IDR (selisih 65,89 miliar IDR). Distribusi pendapatan terlihat dari ringkasan lima angka: minimum 1,00 miliar IDR, kuartil pertama 14,31 miliar IDR, median 31,30 miliar IDR, rata-rata 31,88 miliar IDR, kuartil ketiga 49,04 miliar IDR, dan maksimum 66,89 miliar IDR.
  - *Interpretasi:*
    Nilai standar deviasi yang cukup tinggi menunjukkan bahwa pendapatan startup SaaS sangat beragam dan tidak terkumpul pada satu tingkat tertentu. Artinya, terdapat perbedaan yang jelas antara startup dengan pendapatan rendah, menengah, dan tinggi. Rentang pendapatan yang lebar semakin menegaskan adanya kesenjangan pendapatan yang signifikan dalam industri ini.
	Berdasarkan ringkasan lima angka, sekitar 25% startup memiliki pendapatan di bawah 14,31 miliar rupiah, yang mencerminkan kelompok startup dengan pendapatan relatif rendah. Di sisi lain, sekitar 25% startup memiliki pendapatan di atas 49,04 miliar rupiah, yang menunjukkan kelompok startup dengan pendapatan tinggi. Sementara itu, 50% startup lainnya berada di antara kedua nilai tersebut, dengan pendapatan yang terkonsentrasi di sekitar nilai median, yaitu sekitar 31 miliar rupiah per tahun.
	Secara keseluruhan, hasil ini menunjukkan bahwa ekosistem startup SaaS di Indonesia memiliki kesenjangan pendapatan yang cukup besar. Terdapat kelompok startup dengan pendapatan rendah, kelompok menengah yang relatif stabil, dan kelompok kecil startup dengan pendapatan sangat tinggi. Oleh karena itu, meskipun rata-rata pendapatan industri terlihat cukup besar, nilai tersebut tidak sepenuhnya mencerminkan kondisi seluruh startup. Pemahaman terhadap penyebaran data ini penting agar analisis lanjutan tidak hanya bergantung pada nilai rata-rata, tetapi juga mempertimbangkan variasi dan kesenjangan yang ada.

    
- **Visualisasi (Histogram/Boxplot):**
  - *Histogram:*
  - *Boxplot:*
  - *Interpretasi :* Berdasarkan boxplot dan histogram, pendapatan tahunan startup SaaS menunjukkan penyebaran yang cukup lebar. Boxplot memperlihatkan bahwa setengah dari data berada pada rentang yang luas, menandakan adanya perbedaan pendapatan yang cukup besar antar startup. Rentang nilai yang panjang ke arah pendapatan tinggi menunjukkan bahwa sebagian startup memiliki pendapatan jauh lebih besar dibandingkan mayoritas lainnya.
Histogram mendukung temuan tersebut dengan menunjukkan sebaran pendapatan yang tidak terpusat pada satu nilai tertentu. Data tersebar dari pendapatan rendah hingga tinggi, dengan nilai rata-rata dan median yang hampir sama, sehingga distribusi pendapatan cenderung relatif seimbang. Secara keseluruhan, grafik ini menunjukkan bahwa pendapatan startup SaaS tidak merata, di mana sebagian besar berada pada level rendah hingga menengah, sementara hanya sebagian kecil yang telah mencapai pendapatan tinggi.

### 5.2. Uji Normalitas
- **Hasil Uji Shapiro-Wilk:**
  - *Nilai p-value:* sebesar 1,497 × 10⁻¹⁴
  - *Interpretasi:* Nilai p-value yang jauh lebih kecil dari tingkat signifikansi 0,05 menunjukkan bahwa data pendapatan tahunan tidak terdistribusi normal. Hal ini berarti sebaran data tidak membentuk pola simetris seperti distribusi normal dan kemungkinan dipengaruhi oleh perbedaan pendapatan yang cukup besar antar startup, termasuk adanya beberapa nilai pendapatan yang sangat tinggi dibandingkan mayoritas data lainnya. Ketidaknormalan distribusi data ini memiliki implikasi penting terhadap metode analisis yang digunakan pada tahap selanjutnya, yaitu analisis korelasi. Dalam analisis korelasi digunakan dua metode yaitu metode Pearson dan Spearman. Karena korelasi dengan metode Pearson mensyaratkan data berdistribusi normal, maka metode tersebut tidak sesuai untuk digunakan pada data ini. Oleh karena itu, analisis korelasi dalam proyek ini menggunakan korelasi dengan metode Spearman, yang tidak bergantung pada asumsi normalitas dan lebih stabil terhadap distribusi data yang tidak simetris serta keberadaan nilai ekstrem. Pemilihan metode ini bertujuan untuk menghasilkan analisis hubungan antar variabel yang lebih akurat dan representatif sesuai dengan karakteristik data pendapatan startup SaaS.
    
- **Plot Q-Q:**
  - *Sematkan gambar plot dari folder /results...*
  - *Interpretasi:* Berdasarkan Q-Q Plot variabel Pendapatan_Tahunan_Miliar_IDR, terlihat bahwa sebagian besar titik data tidak mengikuti garis diagonal secara konsisten. Pada bagian tengah, beberapa titik masih mendekati garis, namun pada bagian awal dan terutama bagian akhir, titik-titik mulai menyimpang cukup jauh dari garis lurus/garis diagonal. Penyimpangan yang jelas di sisi kanan menunjukkan adanya nilai pendapatan yang sangat tinggi dibandingkan mayoritas data.
Pola ini menandakan bahwa distribusi data tidak simetris dan memiliki ekor kanan yang panjang (right-skewed). Dengan kata lain, terdapat sejumlah startup dengan pendapatan jauh lebih besar yang menyebabkan bentuk distribusi menyimpang dari distribusi normal. Hasil visual ini sejalan dengan temuan pada uji Shapiro-Wilk yang menyatakan bahwa data tidak terdistribusi normal. Sehingga hal ini akan mempengaruhi analisis selanjutnya yaitu analisis korelasi yang lebih tepat menggunakan metode Spearman karena distribusi data yang tidak normal. 


### 5.3. Analisis Korelasi
- **Nilai Koefisien Korelasi:**
  - *Nilai r:* 0,997  
  - *Interpretasi:* Nilai koefisien korelasi sebesar 0,997 menunjukkan hubungan yang **sangat kuat dan positif** antara Nilai_Pelanggan_Juta_IDR dan Pendapatan_Tahunan_Miliar_IDR. Artinya, semakin tinggi nilai pelanggan, semakin besar pula pendapatan tahunan startup.
    
- **Visualisasi (Scatter Plot):**
  - *Sematkan gambar plot dari folder /results...*
  - *Interpretasi:* Scatter plot menunjukkan pola titik yang membentuk tren naik yang jelas. Sebaran data tidak terlihat acak, dimana titik-titik pada scatter plot terlihat **berkumpul dan mengikuti pola garis linier yang menaik**. Kedekatan titik-titik dengan garis linier menunjukkan bahwa hubungan antara kedua variabel bersifat **konsisten dan stabil**, dengan tingkat penyimpangan yang relatif kecil. Hal ini memperkuat hasil koefisien korelasi yang menunjukkan hubungan positif yang sangat kuat.
    
### 5.4. Analisis Regresi
- **Model Regresi:**
  - *Persamaan regresi: Y = b0 + b1*X*
    Persamaan regresi: Pendapatan_Tahunan_Miliar_IDR = −0,99 + 0,33 × Nilai_Pelanggan_Juta_IDR
  - *Interpretasi:* Koefisien slope sebesar 0,33 menunjukkan bahwa setiap kenaikan 1 juta rupiah nilai pelanggan diperkirakan akan meningkatkan pendapatan tahunan sebesar 0,33 miliar rupiah. Hal ini mengindikasikan adanya hubungan positif dan searah antara nilai pelanggan dan pendapatan, di mana peningkatan nilai pelanggan berkontribusi langsung terhadap peningkatan pendapatan perusahaan.
Sementara itu, nilai intercept sebesar −0,99 merepresentasikan nilai pendapatan tahunan ketika nilai pelanggan bernilai nol. Dalam konteks bisnis startup, kondisi ini tidak realistis karena perusahaan tidak mungkin memperoleh pendapatan tanpa pelanggan. Oleh karena itu, intercept tidak memiliki makna praktis yang kuat, namun tetap diperlukan secara matematis untuk membentuk model regresi.

- **Evaluasi Model (R-squared):**
  - *Nilai R-squared:* 0,994 (99,4%)
  - *Interpretasi:* Nilai ini menunjukkan bahwa 99,4% variasi Pendapatan_Tahunan_Miliar_IDR dapat dijelaskan oleh Nilai_Pelanggan_Juta_IDR melalui model regresi linear. Hal ini menandakan bahwa model memiliki kemampuan penjelasan yang sangat kuat dan sangat sesuai dengan data.
  - 
- **Visualisasi (Garis Regresi pada Scatter Plot):**
  - *Sematkan gambar plot dari folder /results...*
  - *Interpretasi:* Sebagian besar titik data berada sangat dekat dengan garis regresi, yang menunjukkan bahwa prediksi model mendekati nilai aktual. Pola ini mendukung hasil regresi dan mengindikasikan bahwa hubungan antara nilai pelanggan dan pendapatan bersifat linear dan konsisten.

---

## 6. Kesimpulan

Rangkum temuan utama dari analisis Anda dalam beberapa kalimat. Apa wawasan paling penting yang Anda peroleh?
