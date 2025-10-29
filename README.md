# FinTech Customer Lifetime Value (LTV) Prediction Project

## Deskripsi Proyek
Proyek ini bertujuan untuk **memprediksi Customer Lifetime Value (LTV)** pengguna dompet digital seperti PayTM atau Khalti.  
Dengan menganalisis perilaku transaksi dan karakteristik pelanggan, model ini membantu perusahaan **mengidentifikasi pelanggan bernilai tinggi** dan meningkatkan **strategi retensi**.

Dataset terdiri dari **7.000 sampel dengan 20 fitur**, mencakup:
- Demografi
- Riwayat transaksi
- Pola penggunaan aplikasi
- Skor kepuasan & loyalitas pelanggan

---

## Tujuan
- Mengembangkan model prediksi LTV yang akurat & stabil  
- Mengidentifikasi fitur paling berpengaruh terhadap nilai pelanggan  
- Memberikan insight strategis bagi tim bisnis & produk  

---

## Struktur Data

| Fitur | Deskripsi |
|-------|------------|
| Customer_ID | ID unik pelanggan |
| Age | Usia pelanggan (18–70 tahun) |
| Location | Lokasi (Urban/Suburban/Rural) |
| Income_Level | Tingkat pendapatan (Low/Middle/High) |
| Total_Transactions | Jumlah total transaksi |
| Avg_Transaction_Value | Nilai rata-rata transaksi |
| Total_Spent | Total pengeluaran pelanggan |
| Max_Transaction_Value | Transaksi tertinggi |
| Min_Transaction_Value | Transaksi terendah |
| Active_Days | Hari aktif pelanggan di aplikasi |
| Last_Transaction_Days_Ago | Hari sejak transaksi terakhir |
| Loyalty_Points_Earned | Total poin loyalitas |
| Referral_Count | Jumlah pelanggan yang direferensikan |
| Cashback_Received | Total cashback diterima |
| App_Usage_Frequency | Frekuensi penggunaan (Daily/Weekly/Monthly) |
| Preferred_Payment_Method | Metode pembayaran favorit |
| Support_Tickets_Raised | Jumlah keluhan pelanggan |
| Issue_Resolution_Time | Waktu penyelesaian rata-rata (jam) |
| Customer_Satisfaction_Score | Skor kepuasan pelanggan (1–10) |
| LTV | Nilai Lifetime Value (target variabel) |

---

## Alur Proyek

### [1] Data Analyst — Exploratory Analysis (Tableau)
- Menganalisis distribusi transaksi & pengeluaran pelanggan  
- Membuat segmentasi berdasarkan usia, lokasi, & pendapatan  
- Membuat dashboard interaktif di Tableau:
  - **Customer Segmentation Dashboard**
  - **Transaction Overview Dashboard**
  - **Retention & Churn Insight Dashboard**

### [2] Data Scientist — Predictive Modeling (Python)
- Melakukan preprocessing: encoding, normalisasi, dan feature engineering
- Mendeteksi outlier & pola korelasi antar fitur numerik  
- Membangun dua model utama:
  - **XGBRegressor**
  - **Lasso Regression**
- Mengevaluasi kinerja model dengan metrik: R², MAE, MSE, RMSE  
- Menganalisis feature importance untuk menemukan faktor penentu utama LTV  

---

## Hasil Evaluasi Model

| Model | R² Train | R² Test | MAE Test | RMSE Test | Catatan |
|--------|-----------|----------|-----------|------------|-----------|
| XGBRegressor | 0.9998 | 0.9984 | 0.025 | 0.0479 | Akurasi tinggi, overfitting |
| Lasso Regression | 0.8305 | 0.8163 | 0.3707 | 0.5121 | Stabil & generalisasi baik |

**Keputusan Model:**  
Model **Lasso Regression** dipilih karena memiliki keseimbangan terbaik antara akurasi & generalisasi, serta lebih mudah diinterpretasikan.

---

## Analisis Feature Importance

Berdasarkan hasil gabungan **XGBRegressor** dan **Lasso Regression**:

### Dua fitur paling dominan:
1. **Avg_Transaction_Value**  
2. **Total_Transactions**  

### Faktor pendukung lain:
- Customer_Satisfaction_Score  
- Loyalty_Points_Earned  
- Cashback_Received  

**Insight Bisnis:**  
Pelanggan dengan transaksi yang sering & bernilai tinggi memiliki LTV lebih besar.  
Peningkatan kepuasan & loyalitas juga berkontribusi positif meskipun dalam skala lebih kecil.

> Model memprediksi bahwa pelanggan dengan nilai transaksi tinggi dan frekuensi transaksi besar memiliki LTV tinggi. Namun, perilaku recency juga berpengaruh signifikan — pelanggan lama yang sudah tidak aktif akan mengalami penurunan nilai LTV.

---

## Insight Data Analyst

| Area Analisis | Temuan Utama | Rekomendasi Bisnis |
|----------------|---------------|--------------------|
| LTV Segment | Recency transaksi lebih penting dari total transaksi | Fokus pada pelanggan yang masih aktif baru-baru ini |
| Location & Income | Distribusi seimbang | Strategi promosi bisa bersifat nasional |
| Active Days | Banyak pelanggan churn dari segment aktif sebelumnya | Program reaktivasi pelanggan lama |
| Loyalty Program | Reward poin tidak menarik bagi pelanggan LTV tinggi | Ciptakan reward berbasis layanan eksklusif |
| Distribusi LTV | Miring ke kanan, perlu normalisasi | Terapkan log-transform sebelum pemodelan |

**Insight Akhir:**  
Pelanggan dengan aktivitas terbaru tinggi tetapi riwayat transaksi belum panjang memiliki potensi menjadi pelanggan bernilai tinggi.  
Upaya **retention dan personalization** pada kelompok ini akan berdampak signifikan terhadap peningkatan LTV.

---

## Tools & Teknologi
- **Python** (pandas, numpy, scikit-learn, xgboost, matplotlib, seaborn)  
- **Tableau** (visualisasi analisis)  
- **Jupyter Notebook:** `main.ipynb`

---

## Kesimpulan
- **Model Lasso Regression** memberikan hasil yang paling seimbang.  
- Dua fitur utama penentu LTV:  
  1. Avg_Transaction_Value  
  2. Total_Transactions  
- Model dapat digunakan untuk:
  - Memprediksi pelanggan bernilai tinggi  
  - Merancang strategi retensi & promosi personalisasi  

---

## Tim Proyek

| Peran | Tanggung Jawab |
|--------|----------------|
| **Data Analyst** | Eksplorasi data, visualisasi Tableau, segmentasi |
| **Data Scientist** | Pemodelan prediktif, evaluasi, interpretasi fitur |

### Author
Hidayat Bakri &copy; 2025
