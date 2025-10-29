=====================================================================

# 📊 FinTech Customer Lifetime Value (LTV) Prediction Project

=====================================================================

## 🏦 DESKRIPSI PROYEK

Proyek ini bertujuan untuk memprediksi Customer Lifetime Value (LTV)
pengguna dompet digital seperti PayTM atau Khalti.
Dengan menganalisis perilaku transaksi dan karakteristik pelanggan,
model ini membantu perusahaan mengidentifikasi pelanggan bernilai tinggi
dan meningkatkan strategi retensi.

Dataset terdiri dari ~7.000 sampel dengan 20 fitur, mencakup:

- Demografi
- Riwayat transaksi
- Pola penggunaan aplikasi
- Skor kepuasan & loyalitas pelanggan

---

## 🧠 TUJUAN

• Mengembangkan model prediksi LTV yang akurat & stabil
• Mengidentifikasi fitur paling berpengaruh terhadap nilai pelanggan
• Memberikan insight strategis bagi tim bisnis & produk

---

## 📂 STRUKTUR DATA

| Fitur                       | Deskripsi                                   |
| --------------------------- | ------------------------------------------- |
| Customer_ID                 | ID unik pelanggan                           |
| Age                         | Usia pelanggan (18–70 tahun)                |
| Location                    | Lokasi (Urban/Suburban/Rural)               |
| Income_Level                | Tingkat pendapatan (Low/Middle/High)        |
| Total_Transactions          | Jumlah total transaksi                      |
| Avg_Transaction_Value       | Nilai rata-rata transaksi                   |
| Total_Spent                 | Total pengeluaran pelanggan                 |
| Max_Transaction_Value       | Transaksi tertinggi                         |
| Min_Transaction_Value       | Transaksi terendah                          |
| Active_Days                 | Hari aktif pelanggan di aplikasi            |
| Last_Transaction_Days_Ago   | Hari sejak transaksi terakhir               |
| Loyalty_Points_Earned       | Total poin loyalitas                        |
| Referral_Count              | Jumlah pelanggan yang direferensikan        |
| Cashback_Received           | Total cashback diterima                     |
| App_Usage_Frequency         | Frekuensi penggunaan (Daily/Weekly/Monthly) |
| Preferred_Payment_Method    | Metode pembayaran favorit                   |
| Support_Tickets_Raised      | Jumlah keluhan pelanggan                    |
| Issue_Resolution_Time       | Waktu penyelesaian rata-rata (jam)          |
| Customer_Satisfaction_Score | Skor kepuasan pelanggan (1–10)              |
| LTV                         | Nilai Lifetime Value (target variabel)      |

---

## 🧩 ALUR PROYEK

## [1] Data Analyst — Exploratory Analysis (Tableau)

• Menganalisis distribusi transaksi & pengeluaran pelanggan
• Membuat segmentasi berdasarkan usia, lokasi, & pendapatan
• Mendeteksi outlier & pola korelasi antar fitur numerik
• Membuat dashboard interaktif di Tableau:

- Customer Segmentation Dashboard
- Transaction Overview Dashboard
- Retention & Churn Insight Dashboard

## [2] Data Scientist — Predictive Modeling (Python)

• Melakukan preprocessing: encoding, normalisasi, dan feature engineering
• Membangun dua model: - XGBRegressor - Lasso Regression
• Mengevaluasi kinerja model dengan metrik:
R², MAE, MSE, RMSE
• Menganalisis feature importance untuk menemukan faktor penentu utama LTV

---

## 📈 HASIL EVALUASI MODEL

| Model            | R² Train | R² Test | MAE Test | RMSE Test | Catatan                     |
| ---------------- | -------- | ------- | -------- | --------- | --------------------------- |
| XGBRegressor     | 0.9998   | 0.9984  | 0.025    | 0.0479    | Akurasi tinggi, overfitting |
| Lasso Regression | 0.8305   | 0.8163  | 0.3707   | 0.5121    | Stabil & generalisasi baik  |

✅ Keputusan Model:
Lasso Regression dipilih karena memiliki keseimbangan terbaik
antara akurasi & generalisasi, serta lebih mudah diinterpretasikan.

---

## 🔍 ANALISIS FEATURE IMPORTANCE

• Berdasarkan XGBRegressor dan Lasso:

- Dua fitur paling dominan: 1. Avg_Transaction_Value 2. Total_Transactions
  • Faktor pendukung lain: - Customer_Satisfaction_Score - Loyalty_Points_Earned - Cashback_Received
  💡 Insight Bisnis:
  Pelanggan dengan transaksi yang sering & bernilai tinggi
  memiliki LTV lebih besar.
  Peningkatan kepuasan & loyalitas juga berkontribusi positif
  meskipun dalam skala lebih kecil.

---

## ⚙️ TOOLS & TEKNOLOGI

• Python (pandas, numpy, scikit-learn, xgboost, matplotlib, seaborn)
• Tableau (visualisasi analisis)
• Jupyter Notebook: main.ipynb

---

## 🧾 KESIMPULAN

• Model Lasso Regression memberikan hasil yang paling seimbang.
• Dua fitur utama penentu LTV: - Avg_Transaction_Value - Total_Transactions
• Model dapat digunakan untuk: - Memprediksi pelanggan bernilai tinggi - Merancang strategi retensi & promosi personalisasi

---

## 👥 TIM PROYEK

| Peran                | Tanggung Jawab                                    |
| -------------------- | ------------------------------------------------- |
| Data Analyst         | Eksplorasi data, visualisasi Tableau, segmentasi  |
| Data Scientist       | Pemodelan prediktif, evaluasi, interpretasi fitur |
| Business Stakeholder | Pengambilan keputusan & strategi berbasis insight |
