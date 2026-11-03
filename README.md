# Dashboard Analisis Saham BBNI Menggunakan Microsoft Excel

## 1. Gambaran Umum Project

Project ini merupakan analisis data historis harga saham **PT Bank Negara Indonesia (Persero) Tbk (BBNI.JK)** menggunakan Microsoft Excel. Analisis dilakukan untuk memahami pergerakan harga saham, mengevaluasi performa tahunan, mengidentifikasi pola perdagangan, serta mengukur volatilitas dan risiko penurunan harga saham.

Melalui proses data cleaning, data transformation, perhitungan statistik, dan visualisasi data, informasi historis saham diolah menjadi insight yang lebih terstruktur dan mudah dipahami.

Hasil akhir project ini berupa **Dashboard Analisis Saham BBNI** yang menyajikan indikator kinerja utama (KPI), grafik analisis, serta ringkasan insight berdasarkan data historis dalam satu tampilan.

## 2. Tujuan Project

Project ini bertujuan untuk:

- Menganalisis pergerakan harga saham BBNI berdasarkan data historis.
- Mengidentifikasi harga penutupan tertinggi dan terendah.
- Mengevaluasi performa saham berdasarkan return tahunan.
- Menganalisis volume perdagangan dan aktivitas pasar.
- Mengidentifikasi pola return berdasarkan bulan.
- Mengukur volatilitas dan risiko penurunan harga saham.
- Mengidentifikasi tren pergerakan saham menggunakan indikator Moving Average.
- Menyajikan hasil analisis melalui dashboard interaktif berbasis Microsoft Excel.

## 3. Dataset

Dataset yang digunakan berasal dari Kaggle:

**Nama Dataset:** Bank Negara Indonesia Stock Historical Price

**Sumber:** [Kaggle - Bank Negara Indonesia Stock Historical Price](https://www.kaggle.com/datasets/caesarmario/bank-negara-indonesia-stock-historical-price)

**Kode Saham:** BBNI.JK

**Perusahaan:** PT Bank Negara Indonesia (Persero) Tbk

**Periode Data:** 2 Januari 2019 – 30 Oktober 2026

**Jumlah Observasi:** 1.889 baris data perdagangan

### Deskripsi Kolom Dataset

| Kolom | Keterangan |
|---|---|
| Date | Tanggal perdagangan saham |
| Open | Harga pembukaan saham |
| High | Harga tertinggi selama sesi perdagangan |
| Low | Harga terendah selama sesi perdagangan |
| Close | Harga penutupan saham |
| Adj Close | Harga penutupan yang telah disesuaikan |
| Volume | Jumlah saham yang diperdagangkan |

## 4. Tools yang Digunakan

Seluruh proses pengolahan dan analisis dilakukan menggunakan Microsoft Excel.

| Tools / Fitur | Penggunaan |
|---|---|
| Microsoft Excel | Pengolahan dan analisis data |
| Excel Formulas | Perhitungan dan transformasi data |
| Excel Table | Pengelolaan data terstruktur |
| PivotTable | Analisis dan rekapitulasi data |
| Excel Charts | Visualisasi hasil analisis |
| Conditional Formatting | Penekanan informasi penting |
| Excel Dashboard | Penyajian KPI, grafik, dan insight |

## 5. Tahapan Pengerjaan Project

### A. Data Collection

Mengumpulkan data historis harga saham BBNI dari dataset Kaggle yang bersumber dari data historis pasar saham.

### B. Data Cleaning

Melakukan pemeriksaan dan pembersihan data untuk memastikan kualitas data sebelum dianalisis.

Tahapan yang dilakukan meliputi:

- Menghapus 14 baris data dengan volume perdagangan bernilai nol.
- Menghapus kolom `ingested_at_utc` karena tidak digunakan dalam analisis.
- Memeriksa kemungkinan data duplikat.
- Memeriksa missing values.
- Memastikan tipe data tanggal dan numerik sesuai.
- Memeriksa konsistensi nilai harga saham.
- Mengurutkan data berdasarkan tanggal perdagangan.

Setelah proses pembersihan, diperoleh **1.889 baris data** yang digunakan dalam analisis.

### C. Data Transformation

Menambahkan kolom perhitungan menggunakan formula Excel untuk menghasilkan variabel analisis tambahan.

| Kolom | Deskripsi |
|---|---|
| Year | Mengambil tahun dari tanggal perdagangan |
| Month | Mengambil bulan perdagangan |
| Daily Return | Menghitung persentase perubahan Adjusted Close harian |
| Price Range | Menghitung selisih harga tertinggi dan terendah |
| MA20 | Rata-rata harga penutupan selama 20 hari perdagangan |
| MA50 | Rata-rata harga penutupan selama 50 hari perdagangan |
| MA200 | Rata-rata harga penutupan selama 200 hari perdagangan |
| Volatility 20D | Mengukur volatilitas berdasarkan standar deviasi return selama 20 hari perdagangan |
| Signal | Mengklasifikasikan tren berdasarkan perbandingan MA20 dan MA50 |
| Running Max (Adj) | Menentukan nilai tertinggi historis Adjusted Close hingga tanggal tertentu |
| Drawdown | Mengukur persentase penurunan dari puncak historis |

### D. Exploratory Data Analysis (EDA)

Analisis dilakukan untuk menemukan pola, tren, dan karakteristik dari data historis saham BBNI.

Analisis mencakup:

1. **Analisis Harga Saham:** Mengamati pergerakan harga penutupan dan tren berdasarkan Moving Average.
2. **Analisis Performa Tahunan:** Membandingkan return, rata-rata harga, harga tertinggi, harga terendah, dan volume perdagangan setiap tahun.
3. **Analisis Seasonality:** Mengidentifikasi pola rata-rata daily return berdasarkan bulan.
4. **Analisis Volume Perdagangan:** Mengamati aktivitas perdagangan berdasarkan total dan rata-rata volume.
5. **Analisis Tren:** Mengklasifikasikan kondisi tren saham berdasarkan indikator MA20 dan MA50.
6. **Analisis Risiko:** Mengukur volatilitas dan maximum drawdown untuk memahami fluktuasi serta risiko penurunan harga.

## 6. Dashboard Analisis Saham BBNI

Dashboard dibuat menggunakan Microsoft Excel untuk menyajikan hasil analisis secara ringkas, informatif, dan mudah dipahami.

### A. Key Performance Indicators (KPI)

Dashboard menampilkan enam indikator utama:

| KPI | Keterangan |
|---|---|
| Latest Closing Price | Harga penutupan saham terbaru dalam dataset |
| YTD Price Change | Persentase perubahan harga sejak awal tahun |
| 52-Week High | Harga tertinggi dalam 52 minggu terakhir |
| 52-Week Low | Harga terendah dalam 52 minggu terakhir |
| Average Daily Volume | Rata-rata volume perdagangan harian |
| Maximum Drawdown | Penurunan terbesar dari puncak historis |

### B. Visualisasi Dashboard

Dashboard dilengkapi dengan tujuh visualisasi utama.

| No. | Visualisasi | Tujuan Analisis |
|---|---|---|
| 1 | Harga Close dan Moving Average | Melihat tren harga saham berdasarkan MA20, MA50, dan MA200 |
| 2 | Return Tahunan | Membandingkan performa saham setiap tahun |
| 3 | Total Volume per Tahun | Menganalisis aktivitas perdagangan tahunan |
| 4 | Monthly Seasonality | Mengidentifikasi pola rata-rata daily return berdasarkan bulan |
| 5 | Bullish vs Bearish | Melihat distribusi klasifikasi tren saham |
| 6 | Rata-rata Harga Close per Tahun | Membandingkan rata-rata harga penutupan setiap tahun |
| 7 | Drawdown | Mengidentifikasi tingkat penurunan harga dari puncak historis |

Selain visualisasi, dashboard juga dilengkapi dengan ringkasan insight otomatis untuk membantu memahami hasil analisis.

## 7. Hasil dan Temuan Analisis

Berdasarkan hasil pengolahan data dalam workbook, diperoleh beberapa temuan utama sebagai berikut.

### A. Pergerakan Harga Saham

Pada 30 Oktober 2026, harga penutupan saham BBNI tercatat sebesar **Rp3.320**.

Beberapa indikator harga yang diperoleh:

- Harga tertinggi dalam 52 minggu: Rp4.730.
- Harga terendah dalam 52 minggu: Rp2.830.
- Perubahan harga secara Year-to-Date: sekitar -24,03%.
- Perubahan harga dalam satu tahun: sekitar -24,72%.

### B. Performa Tahunan

Berdasarkan perhitungan return tahunan menggunakan Adjusted Close:

- Tahun 2022 mencatat performa tertinggi dengan return sekitar +39,19%.
- Tahun 2020 mencatat performa terendah dengan return sekitar -18,96%.

Hasil ini menunjukkan adanya perbedaan performa saham yang cukup bervariasi antarperiode pengamatan.

### C. Analisis Seasonality

Berdasarkan rata-rata daily return historis:

- Agustus memiliki rata-rata daily return tertinggi.
- Mei memiliki rata-rata daily return terendah.

Temuan ini menggambarkan pola historis berdasarkan bulan, bukan jaminan bahwa pola yang sama akan terjadi pada periode mendatang.

### D. Aktivitas Perdagangan

Rata-rata volume perdagangan selama periode pengamatan mencapai sekitar **65,12 juta saham per hari**.

Hasil perhitungan korelasi antara volume perdagangan dan daily return menunjukkan nilai sekitar **0,124**, yang mengindikasikan hubungan linear positif tetapi relatif lemah.

### E. Analisis Risiko dan Tren

Hasil analisis menunjukkan:

- Maximum Drawdown: sekitar -66,16%.
- Rata-rata volatilitas 20 hari: sekitar 1,97%.
- Klasifikasi tren terakhir: Bearish.

Klasifikasi Bearish diperoleh ketika nilai MA20 berada di bawah MA50.

### F. Performa Jangka Panjang

Berdasarkan Adjusted Close:

- Total cumulative return: sekitar +6,61%.
- Compound Annual Growth Rate (CAGR): sekitar +0,82%.

Perhitungan ini memberikan gambaran pertumbuhan harga yang telah disesuaikan selama periode pengamatan.

## 8. Struktur Workbook Excel

Workbook terdiri dari empat worksheet utama:

| Sheet | Fungsi |
|---|---|
| Dashboard | Menampilkan KPI, visualisasi, dan ringkasan insight |
| Analisis | Menyimpan hasil perhitungan, rekapitulasi tahunan, seasonality, dan analisis tren |
| Data | Menyimpan data historis saham beserta kolom hasil transformasi |
| README | Berisi dokumentasi dan penjelasan workbook |

## 9. Formula Excel yang Digunakan

Beberapa fungsi Excel yang digunakan dalam project ini antara lain:

| Formula | Fungsi |
|---|---|
| `YEAR()` | Mengambil tahun dari tanggal |
| `MONTH()` | Mengambil bulan dari tanggal |
| `AVERAGE()` | Menghitung nilai rata-rata |
| `AVERAGEIFS()` | Menghitung rata-rata berdasarkan kriteria |
| `SUMIFS()` | Menghitung total berdasarkan kriteria |
| `MAX()` | Menentukan nilai maksimum |
| `MIN()` | Menentukan nilai minimum |
| `MAXIFS()` | Menentukan nilai maksimum berdasarkan kriteria |
| `MINIFS()` | Menentukan nilai minimum berdasarkan kriteria |
| `INDEX()` | Mengambil nilai berdasarkan posisi |
| `MATCH()` | Mencari posisi suatu nilai |
| `STDEV()` | Menghitung standar deviasi |
| `CORREL()` | Menghitung korelasi |
| `COUNTIF()` | Menghitung jumlah data berdasarkan kriteria |
| `IF()` | Membuat logika kondisi |
| `IFERROR()` | Menangani kesalahan formula |

## 10. Keterbatasan Analisis

Beberapa hal yang perlu diperhatikan dalam menginterpretasikan hasil project:

- Analisis hanya menggunakan data historis harga dan volume perdagangan.
- Analisis tidak mencakup laporan keuangan fundamental perusahaan maupun indikator makroekonomi.
- Korelasi antara volume dan return tidak menunjukkan hubungan sebab-akibat.
- Moving Average merupakan indikator teknikal sederhana dan bukan alat prediksi harga yang pasti.
- Analisis seasonality hanya menggambarkan pola historis.
- Data tahun 2026 merupakan data parsial hingga 30 Oktober 2026.
- Hasil analisis tidak dapat dijadikan satu-satunya dasar pengambilan keputusan investasi.

## 11. Kesimpulan

Project ini menunjukkan penerapan Microsoft Excel dalam proses analisis data secara menyeluruh, mulai dari data cleaning, data transformation, perhitungan statistik, exploratory data analysis, hingga visualisasi melalui dashboard.

Melalui analisis historis saham BBNI, berbagai indikator seperti pergerakan harga, return, volume perdagangan, moving average, volatilitas, dan drawdown dapat digunakan untuk memahami karakteristik performa saham selama periode pengamatan.

Dashboard yang dihasilkan menyajikan informasi tersebut dalam bentuk KPI, grafik, dan ringkasan insight sehingga mempermudah proses eksplorasi serta interpretasi data.

Project ini juga menjadi salah satu implementasi kemampuan **Data Analysis menggunakan Microsoft Excel**, khususnya dalam pengolahan data historis, analisis statistik, dan pembuatan dashboard.

## 12. Disclaimer

Project ini dibuat untuk tujuan pembelajaran, eksplorasi data, dan portofolio analisis data. Seluruh hasil analisis didasarkan pada data historis dan tidak merupakan rekomendasi atau saran investasi.

## Author

**Dian Fatonah**

Lulusan Teknik Informatika | Data Analyst Enthusiast

- GitHub: [Dianftnh](https://github.com/Dianftnh)
- Portfolio: [Website Portofolio](https://website-dian-fatonah.vercel.app/)
