# 📊 FinTech Customer Lifetime Value (LTV) — Data Analyst Report
---

<img width="1540" height="852" alt="Screenshot 2025-10-29 083558" src="https://github.com/user-attachments/assets/5b01bc92-58cd-4305-af52-e283d2e7e501" />

## Deskripsi Umum
Analisis ini dilakukan untuk memahami pola perilaku pelanggan dompet digital (digital wallet) seperti PayTM dan Khalti berdasarkan dataset **FinTech Customer LTV**.  
Tujuannya adalah mengidentifikasi faktor-faktor yang mempengaruhi nilai **Customer Lifetime Value (LTV)** serta memberikan insight strategis untuk meningkatkan retensi pelanggan.

Analisis dilakukan menggunakan **Tableau**, dengan fokus pada eksplorasi visual terhadap segmentasi pelanggan, aktivitas transaksi, loyalitas, dan distribusi nilai LTV.

---

## 1. Analisis Segmen LTV
### Temuan:
- **Segment Low**: Pelanggan yang *dulunya sangat aktif* dalam bertransaksi, namun kini telah berhenti (*churn*).  
- **Segment High**: Pelanggan dengan jumlah transaksi yang relatif sedikit, tetapi masih *aktif bertransaksi baru-baru ini*.

### Interpretasi:
- Frekuensi transaksi terakhir (*recency*) memiliki pengaruh lebih besar terhadap nilai LTV dibandingkan total transaksi kumulatif.
- Pelanggan dengan total transaksi tinggi namun aktivitas terbaru rendah *tidak selalu bernilai tinggi* bagi perusahaan.

### Insight Bisnis:
> Fokus retensi sebaiknya diarahkan pada pelanggan aktif dengan *recent transactions* meskipun historinya masih pendek, karena mereka berpotensi menjadi pelanggan bernilai tinggi di masa depan.

---

## 2. Analisis Lokasi & Tingkat Pendapatan
### Temuan:
- Distribusi pelanggan berdasarkan lokasi relatif seimbang:
  - Urban: ~34%
  - Suburban: ~33%
  - Rural: ~33%
- Distribusi tingkat pendapatan juga seimbang:
  - Low: ~33%
  - Middle: ~34%
  - High: ~33%

### Insight Bisnis:
> Karena distribusi seimbang, strategi pemasaran tidak perlu diferensiasi lokasi atau pendapatan.  
> Perusahaan dapat mengoptimalkan kampanye nasional tanpa bias wilayah atau ekonomi.

---

## 3. Analisis Aktivitas Pelanggan (Active Days)
### Temuan:
- Segment **Low** mendominasi total pelanggan aktif (~82.83%) dibandingkan **High** (~17.17%).
- Sebagian besar pelanggan *pernah aktif intensif*, namun kini tidak lagi.

### Distribusi Active Days:
- Distribusi *flat* menandakan tidak ada pola musiman tertentu.
- Terdapat satu bar dengan jumlah rendah (anomali), kemungkinan merepresentasikan pelanggan **segment High**.

### Insight Bisnis:
> Perlu dilakukan kampanye *re-engagement* terhadap pelanggan lama yang dulunya aktif, misalnya melalui email marketing atau cashback reaktivasi.

---

## 4. Analisis Loyalitas Pelanggan
### Temuan:
- **Segment Low** memiliki total poin loyalitas yang jauh lebih besar dibandingkan **Segment High**.
- Program loyalitas gagal memotivasi pelanggan dengan LTV tinggi.

### Insight Bisnis:
> Pelanggan bernilai tinggi mungkin tidak tertarik pada reward poin.  
> Coba strategi alternatif seperti:
> - Diskon layanan premium
> - Akses eksklusif produk finansial
> - Program *VIP retention*

---

## 5. Distribusi Nilai LTV
### Temuan:
- Distribusi nilai LTV **miring ke kanan (right-skewed)**.
- Sebagian besar pelanggan memiliki LTV rendah, dengan sedikit pelanggan bernilai tinggi (*long tail pattern*).

### Rekomendasi Statistik:
> Lakukan **transformasi log (log-normalization)** untuk menstabilkan distribusi sebelum pemodelan prediktif.

### Insight Bisnis:
> Perusahaan dapat menerapkan pendekatan *Pareto Principle (80/20)*:  
> 20% pelanggan bernilai tinggi kemungkinan menyumbang sebagian besar pendapatan.

---

## Kesimpulan Utama

| Area Analisis         | Temuan Utama                                                                 | Rekomendasi Bisnis                                                                 |
|------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| LTV Segment            | Recency transaksi lebih penting dari total transaksi                        | Fokus pada pelanggan yang masih aktif baru-baru ini                               |
| Location & Income      | Distribusi seimbang, tidak ada bias wilayah atau pendapatan                  | Strategi promosi bisa bersifat nasional                                            |
| Active Days            | Banyak pelanggan churn dari segment aktif sebelumnya                         | Program reaktivasi pelanggan lama                                                  |
| Loyalty Program        | Program poin tidak menarik bagi pelanggan LTV tinggi                         | Ciptakan reward berbasis layanan eksklusif                                        |
| Distribusi LTV         | Miring ke kanan, perlu normalisasi                                           | Terapkan log-transform sebelum pemodelan                                          |

---

## Tools yang Digunakan
- **Tableau Public / Desktop**
- **Excel / CSV Preprocessing**
- **Python (EDA ringan & ekspor data ke Tableau)**

---

## Insight Akhir
> Pelanggan dengan **aktivitas baru-baru ini tinggi** tetapi **riwayat transaksi belum panjang** memiliki potensi menjadi pelanggan bernilai tinggi di masa depan.  
> Upaya *retention dan personalization* pada kelompok ini akan berdampak signifikan pada peningkatan Customer Lifetime Value.

---
