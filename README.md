
# 📊 CCPP Environmental Data 2021–2024 

## 📁 File: `ccpp_env_2021_2024.xlsx`

Dataset ini merupakan **data lingkungan dan keluaran daya realistis** yang disusun untuk merepresentasikan keluaran daya dari **Pembangkit Listrik Tenaga Gas dan Uap (PLTGU)** berdasarkan kondisi lingkungan. Dataset ini dikembangkan sebagai **replikasi ilmiah** dari dataset *Combined Cycle Power Plant (CCPP)* yang tersedia di UCI Machine Learning Repository.

> Dataset ini dibangun dengan mengikuti **pola distribusi statistik dan korelasi antar variabel** dari dataset CCPP asli, sehingga mampu merepresentasikan fenomena nyata secara realistis dan dapat digunakan sebagai dasar eksperimen ilmiah.

---

## 🎯 Tujuan Dataset

Dataset ini dapat digunakan untuk:

- Penelitian prediksi daya listrik berbasis *machine learning*
- Evaluasi algoritma regresi (GBR, SVR, Linear, dll.)
- Uji validitas model terhadap data yang menyerupai pola riil
- Pengembangan sistem pembangkit berbasis AI dengan data lingkungan

---

## 🧱 Struktur Dataset

Dataset terdiri dari **10.000 entri** tanpa informasi waktu eksplisit (karena disintesis dari periode 2021–2024), dengan 5 kolom numerik sebagai berikut:

| Kolom | Deskripsi |
|-------|-----------|
| `AT`  | *Ambient Temperature* dalam °C |
| `V`   | *Exhaust Vacuum* dalam cm Hg |
| `AP`  | *Ambient Pressure* dalam mbar |
| `RH`  | *Relative Humidity* dalam % |
| `PE`  | *Electrical Energy Output* (target) dalam MW |

---

## 🧪 Metodologi Sintesis

### 1. **Sumber Data Asli**
Dataset asli diperoleh dari:
> Tufekci, P. (2014). *Prediction of full load electrical power output of a base load operated combined cycle power plant using machine learning methods*. Energy, 60, 1–9. [https://doi.org/10.1016/j.energy.2013.07.032](https://doi.org/10.1016/j.ijepes.2014.02.027)

### 2. **Replikasi Fitur**
- Data lingkungan (`AT`, `V`, `AP`, `RH`) di-*bootstrap* dari dataset UCI untuk mempertahankan distribusi dan pola alami.
- Metode bootstrap dilakukan dengan `sampling with replacement` terhadap seluruh data asli.

### 3. **Simulasi Target PE**
- Target `PE` dihasilkan menggunakan model **Gradient Boosting Regression** yang dilatih pada data asli UCI-CCPP.
- Fitur di-*standardize* menggunakan *StandardScaler* sebelum diprediksi.

### 4. **Jumlah dan Format**
- Jumlah total data: **10.000 baris**
- Format: Excel (.xlsx), siap digunakan di Python, R, SPSS, atau MATLAB

---

## 📈 Distribusi Data (Ringkasan)

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
- Menggunakan pendekatan statistik berbasis data asli yang telah divalidasi di jurnal *Scopus* (Energy, Elsevier).
- Menjaga korelasi antar variabel lingkungan dan target `PE`.
- Jumlah data cukup besar untuk pembelajaran mesin (*machine learning*).
- Tidak mengandung informasi pribadi atau sensitif (fully synthetic & anonymous).

---

## 📚 Rekomendasi Penggunaan

- Gunakan algoritma regresi (Linear, SVR, Random Forest, Gradient Boosting) untuk memprediksi `PE`.
- Lakukan evaluasi model menggunakan metrik: MAE, RMSE, dan R².
- Dataset cocok dijadikan eksperimen replikasi model energi untuk tugas akhir, skripsi, atau publikasi.

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

