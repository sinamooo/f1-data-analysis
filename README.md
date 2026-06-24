# f1-data-analysis

# 🏎️ Formula 1 Performance & Pit Stop Exploratory Data Analysis (EDA)

Proyek ini melakukan analisis mendalam terhadap performa balapan dan efisiensi operasional pit stop di Formula 1 menggunakan teknik analisis data univariat dan bivariat. Tujuan utamanya adalah mengidentifikasi faktor penentu kemenangan serta tolok ukur efisiensi kru pit.

---

## 🛠️ Tools & Libraries Used
Proyek ini dibangun menggunakan ekosistem Data Science Python:
* **Python** (Bahasa pemrograman utama)
* **Jupyter Lab / Notebook** (Lingkungan pengembangan)
* **Pandas**: Untuk manipulasi, pembersihan, dan penggabungan (*merging*) dataset.
* **Matplotlib & Seaborn**: Untuk visualisasi data tingkat lanjut, pembuatan grafik regresi, distribusi, hingga heatmap korelasi.

---

## 📊 Dataset Information
Analisis ini menggunakan dua dataset utama yang saling terhubung:
1. **Race Results Dataset**: Berisi 1,024 baris data hasil balapan dari ~50 seri, mencakup informasi posisi start, posisi finish, poin, jumlah laps, dan tim konstruktor.
2. **Pit Stops Dataset**: Berisi 1,726 baris catatan waktu pit stop pembalap, termasuk durasi berada di pit lane dalam satuan detik.

---

## 🎯 3 Key Findings

### 1. Tolok Ukur Efisiensi Pit Stop (Pit Lane Window)
Berdasarkan analisis distribusi operasional, batas median waktu yang dihabiskan pembalap di area *pit lane* adalah **23.33 detik**, dengan mayoritas performa kompetitif berkerumun rapat di rentang **21 hingga 26 detik**. Margin waktu ini menjadi acuan mutlak bagi tim strategi untuk menghitung window *under-cut* atau *over-cut* saat balapan.

### 2. Kualifikasi Adalah 50% Kunci Kemenangan
Melalui pemodelan regresi linear antara posisi start (`grid_pos`) dan posisi finish (`position`), ditemukan korelasi positif yang sangat kuat. Pembalap yang berhasil mengamankan posisi *Top 3* saat sesi Kualifikasi hari Sabtu memiliki probabilitas yang jauh lebih tinggi untuk mengakhiri balapan di zona podium hari Minggu. 

### 3. Validasi Logika Skor & Keseimbangan Data
Analisis Heatmap menunjukkan korelasi negatif sempurna (-1.00) antara posisi finish dengan perolehan poin. Hal ini memvalidasi integritas dataset sekaligus menegaskan aturan F1: semakin kecil angka posisi finishnya (Juara 1), perolehan poin yang dibawa pulang ke klasemen justru semakin maksimal. Selain itu, sebaran posisi start yang seragam (*uniform distribution*) membuktikan dataset ini bersih dan tidak bias.

---

## 🚀 How to Run
1. Clone repository ini:
   ```bash
   git clone [https://github.com/username-kamu/f1-data-analysis.git](https://github.com/username-kamu/f1-data-analysis.git)
