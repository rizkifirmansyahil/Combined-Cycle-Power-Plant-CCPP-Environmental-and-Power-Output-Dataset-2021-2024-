
# 📊 CCPP Environmental Data 2021–2024 

## 📁 File: `ccpp_env_2021_2024.xlsx`

Dataset ini merupakan data lingkungan dan keluaran daya realistis yang disusun untuk merepresentasikan keluaran daya dari Pembangkit Listrik Tenaga Gas dan Uap (PLTGU) berdasarkan pengaruh faktor-faktor lingkungan. Dataset ini dikembangkan sebagai bentuk rekonstruksi akademik dari dataset Combined Cycle Power Plant (CCPP) yang tersedia di UCI Machine Learning Repository, guna menjawab kebutuhan analisis prediktif yang relevan dengan periode waktu dan skenario operasional terkini.
> Penyusunan data dilakukan dengan mengikuti pola distribusi statistik, hubungan antar variabel, serta karakteristik sistem pada data asli CCPP, sehingga tetap mewakili dinamika nyata dalam sistem pembangkitan energi dan dapat digunakan sebagai dasar eksperimen ilmiah.

---

## 🎯 Tujuan Dataset

Dataset ini dapat digunakan untuk:

- Penelitian prediksi daya listrik berbasis *machine learning*
- Evaluasi algoritma regresi (GBR, SVR, Linear, dll.)
- Uji validitas model terhadap data yang menyerupai pola riil
- Pengembangan sistem pembangkit berbasis AI dengan data lingkungan

---

## 🧱 Struktur Dataset

Dataset terdiri dari **10.000 entri** data yang memuat lima fitur numerik utama yang umum digunakan dalam studi sistem pembangkitan:

| Kolom | Deskripsi |
|-------|-----------|
| `AT`  | *Ambient Temperature* dalam °C |
| `V`   | *Exhaust Vacuum* dalam cm Hg |
| `AP`  | *Ambient Pressure* dalam mbar |
| `RH`  | *Relative Humidity* dalam % |
| `PE`  | *Electrical Energy Output* (target) dalam MW |

---

## 🧪 Metodologi Sintesis

### 1. **Sumber Referensi Ilmiah**
Dataset ini direkonstruksi berdasarkan penelitian berikut:
> Tufekci, P. (2014). *Prediction of full load electrical power output of a base load operated combined cycle power plant using machine learning methods*. Energy, 60, 1–9. [https://doi.org/10.1016/j.energy.2013.07.032](https://doi.org/10.1016/j.ijepes.2014.02.027)

### 2. **Replikasi Fitur**
- Data lingkungan (`AT`, `V`, `AP`, `RH`) di-*bootstrap* dari dataset UCI untuk mempertahankan distribusi dan pola alami.
- Metode bootstrap dilakukan dengan `sampling with replacement` terhadap seluruh data asli.

### 3. **Pemodelan Target PE**
- Target `PE` dihasilkan menggunakan model **Gradient Boosting Regression** yang dilatih pada data asli UCI-CCPP.
- Fitur di-*standardize* menggunakan *StandardScaler* sebelum diprediksi.

### 4. **Jumlah dan Format**
- Jumlah total data: **10.000 baris**
- Format: Excel (.xlsx), siap digunakan di Python, R, SPSS, atau MATLAB

---

## 📈 Distribusi Data (Ringkasan  Statistik)

| Kolom | Rata-rata | Min | Maks | Std Dev |
|-------|-----------|-----|------|----------|
| `AT`  | ~19–22 °C | ~5  | ~35  | ~5 |
| `V`   | ~50 cm Hg | ~25 | ~81  | ~12 |
| `AP`  | ~1010 mbar | ~990 | ~1030 | ~10 |
| `RH`  | ~60 %     | ~25 | ~100 | ~15 |
| `PE`  | ~450–500 MW | ~420 | ~540 | ~15–20 |

---

## ✅ Validitas Ilmiah

Dataset ini cocok untuk penelitian ilmiah karena:
- Disusun berdasarkan data publik yang berasal dari Combined Cycle Power Plant (CCPP) milik UCI Machine Learning Repository, serta didukung oleh referensi jurnal bereputasi (Scopus Q1), seperti yang diterbitkan dalam Energy (Elsevier).
- Dikontruksi menggunakan pendekatan statistik dan algoritma machine learning yang telah terverifikasi, dengan mempertahankan pola korelasi antar variabel yang sesuai dengan kondisi fisis sistem PLTGU.
- Mewakili hubungan multivariat antara parameter lingkungan (AT, V, AP, RH) dan keluaran daya (PE) secara konsisten dan realistis, sebagaimana ditemukan dalam data empirik.
- Memiliki cakupan data yang cukup besar (10.000 entri), sehingga mendukung generalisasi model pembelajaran mesin.
- Tidak mengandung informasi pribadi, sensitif, atau temporal, sehingga aman digunakan dalam eksperimen terbuka dan akademik.


---

## 📚 Rekomendasi Penggunaan

- Terapkan algoritma regresi (seperti Linear Regression, SVR, Random Forest, dan Gradient Boosting) untuk memodelkan hubungan antara variabel lingkungan dan output daya `PE`.
- Lakukan evaluasi model menggunakan metrik: MAE, RMSE, dan R².
- Dataset ini sesuai digunakan dalam proyek pengembangan model energi berbasis data, baik untuk tugas akhir, skripsi, maupun sebagai dasar eksperimen pada publikasi ilmiah.

---

## 📌 Catatan

- Dataset ini **tidak memuat kolom waktu** (`date`, `year`, `month`) karena fokus penelitian adalah pada hubungan antar variabel lingkungan dan output daya.
- Jika diperlukan versi per tahun atau versi dengan data musiman, silakan hubungi pengembang dataset.

---

## 🧑‍💻 Pengembang Dataset

Dataset ini disintesis sebagai bagian dari penelitian di bidang pembangkitan energi berbasis machine learning, khususnya untuk prediksi daya pada Pembangkit Listrik Tenaga Gas dan Uap (PLTGU). Proses sintesis dilakukan menggunakan bahasa pemrograman Python dengan bantuan pustaka *Scikit-learn* dan *Pandas* untuk manipulasi data serta pelatihan model prediktif.

---
## ⚖️ Lisensi

**Lisensi**: [CC BY 4.0 – Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/)

Anda bebas untuk:

- **Membagikan** — menyalin dan menyebarluaskan materi dalam format atau media apapun  
- **Mengadaptasi** — menggubah, mengubah, dan membuat turunan dari materi ini  

Dengan syarat:

- **Atribusi** — Anda harus menyertakan atribusi yang sesuai (contoh: nama pembuat dan sumber asal), menyediakan tautan ke lisensi ini, dan menyatakan jika ada perubahan yang dilakukan.

🔗 https://creativecommons.org/licenses/by/4.0/

> *Dataset ini disintesis berdasarkan karakteristik data publik dari UCI Machine Learning Repository: [Combined Cycle Power Plant (CCPP)](https://archive.ics.uci.edu/ml/datasets/Combined+Cycle+Power+Plant) – © UCI ML Repository*

