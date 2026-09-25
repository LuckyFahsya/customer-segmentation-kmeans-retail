# Penerapan Clustering K-Means untuk Segmentasi Pelanggan pada Bisnis Retail

Proyek segmentasi pelanggan menggunakan **RFM Analysis** dan **K-Means Clustering** pada dataset transaksi ritel online. Proyek ini merupakan tugas akhir mata kuliah Machine Learning (semester 5) yang telah dipublikasikan pada jurnal ilmiah terindeks **Sinta 5**.

## 📊 Dataset

[Online Retail — UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail)
Transaksi sebuah perusahaan ritel online asal Inggris periode 01/12/2010–09/12/2011 (541.909 baris transaksi, 8 kolom).


## 🎯 Tujuan

Mengidentifikasi segmen pelanggan bernilai tinggi (loyal customers) berdasarkan perilaku transaksi, sebagai dasar rekomendasi strategi retensi pelanggan.

## 🔧 Metodologi

1. **Data Cleaning** — membuang transaksi dengan CustomerID kosong, transaksi pembatalan, dan anomali quantity/price → 397.884 transaksi valid dari 4.338 pelanggan
2. **Feature Engineering** — membangun fitur RFM (Recency, Frequency, Monetary) per pelanggan
3. **Standardisasi** — StandardScaler agar setiap fitur setara bobotnya
4. **K-Means Clustering** (k=3) — divalidasi dengan Elbow Method & Silhouette Score
5. **Evaluasi Cluster** — Silhouette Score, Davies-Bouldin Index, Calinski-Harabasz Score
6. **Interpretasi Bisnis** — profiling tiap segmen & rekomendasi strategi retensi

## 📈 Hasil

| Metrik | Nilai |
|---|---|
| Silhouette Score | 0.594 |
| Davies-Bouldin Index | 0.710 |
| Calinski-Harabasz Score | 3.018,43 |

Segmen pelanggan **loyal** (kelompok kecil dengan frekuensi & nilai belanja tertinggi) menyumbang porsi revenue yang jauh melampaui proporsi jumlah mereka — menegaskan prinsip Pareto pada basis pelanggan bisnis ini.

## 🛠️ Tools & Libraries

- Python (Pandas, NumPy)
- Scikit-learn (StandardScaler, KMeans, evaluation metrics)
- Matplotlib, Seaborn

## 🚀 Cara Menjalankan

```bash
pip install pandas numpy scikit-learn matplotlib seaborn openpyxl
jupyter notebook K_Means_Customer_Segmentation.ipynb
```

## 📁 Struktur Repo

```
├── K_Means_Customer_Segmentation.ipynb   # Notebook analisis lengkap
├── Online Retail.xlsx                     # Dataset
├── README.md
└── requirements.txt
```

---
*Catatan: Notebook ini merupakan rekonstruksi dari proyek asli (berkas kerja sebelumnya hilang akibat instal ulang laptop), dibangun ulang mengikuti metodologi yang sama seperti pada publikasi jurnal.*
