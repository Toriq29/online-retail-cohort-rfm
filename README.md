# 📊 Customer Retention & Segmentation Analysis — Online Retail II

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458.svg)
![Tableau](https://img.shields.io/badge/Tableau-Visualization-E97627.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)

Analisis retensi pelanggan dan segmentasi customer menggunakan **Cohort Analysis** dan **RFM (Recency, Frequency, Monetary) Segmentation** pada dataset UCI Online Retail II, untuk mengidentifikasi pola churn dan customer bernilai tinggi.

📈 **[View Interactive Dashboard on Tableau Public](<!-- TODO: paste link Tableau Public kamu di sini -->)**

---

## 📌 Table of Contents
- [Business Problem](#business-problem)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [Business Recommendations](#business-recommendations)
- [Tech Stack](#tech-stack)
- [Repository Structure](#repository-structure)
- [How to Run](#how-to-run)

---

## Business Problem

Retail bisnis sering kehilangan pelanggan tanpa menyadari **kapan** dan **mengapa** hal itu terjadi. Tanpa memahami pola retensi dan nilai pelanggan, tim marketing kesulitan mengalokasikan budget campaign secara efektif.

Project ini menjawab dua pertanyaan utama:
1. **Kapan** pelanggan mulai berhenti bertransaksi setelah pembelian pertama? *(Cohort Analysis)*
2. **Siapa** pelanggan paling bernilai yang harus diprioritaskan untuk retention campaign? *(RFM Segmentation)*

## Dataset

- **Sumber:** [UCI Machine Learning Repository — Online Retail II](https://archive.ics.uci.edu/dataset/502/online+retail+ii)
- **Periode:** <!-- TODO: contoh Des 2009 – Des 2011 -->
- **Jumlah transaksi:** <!-- TODO -->
- **Jumlah unique customer:** <!-- TODO -->
- **Cakupan:** Transaksi online retail berbasis UK, mencakup invoice, produk, quantity, harga, dan customer ID.

## Methodology

### 1. Data Cleaning
- Menghapus transaksi dengan `CustomerID` null
- Menghapus cancelled orders (invoice berawalan 'C')
- Menangani outlier pada quantity & harga negatif

### 2. Cohort Analysis
- Mengelompokkan customer berdasarkan bulan transaksi pertama (*cohort month*)
- Menghitung retention rate tiap cohort dari bulan ke bulan
- Visualisasi heatmap retention untuk melihat pola drop-off

### 3. RFM Segmentation
- **Recency:** Berapa lama sejak transaksi terakhir
- **Frequency:** Seberapa sering customer bertransaksi
- **Monetary:** Total nilai pembelian
- Scoring tiap dimensi (1-5) → dikombinasikan jadi segment (contoh: *Champions*, *At Risk*, *Loyal Customers*, *Lost*)

## Key Findings

### 🔥 Cohort Retention Heatmap
![Cohort Retention Heatmap](visualizations/cohort.png)

<!-- TODO: 2-3 kalimat insight, contoh:
"Retention rate turun tajam ~40% pada bulan ke-2 setelah pembelian pertama, 
menandakan window kritis untuk re-engagement ada di 30-60 hari pertama." -->

### 🎯 RFM Customer Segments
![RFM Segmentation](visualizations/rfm.png)

<!-- TODO: 2-3 kalimat insight, contoh:
"X% customer masuk kategori 'Champions' namun berkontribusi Y% dari total revenue,
sementara segment 'At Risk' mencakup Z% customer yang berisiko churn dalam 30 hari." -->

## Business Recommendations

<!-- TODO: sesuaikan dengan findings aktual, contoh format: -->
1. **Segment "At Risk"** (X% dari customer base) → luncurkan win-back campaign dengan diskon personal dalam 30 hari sejak inactivity terdeteksi.
2. **Segment "Champions"** → prioritaskan untuk loyalty program / early access produk baru, karena berkontribusi terbesar terhadap revenue.
3. **Cohort onboarding** → perkuat komunikasi (email/push notif) di 60 hari pertama, karena periode ini adalah titik kritis retention.

## Tech Stack

| Kategori | Tools |
|---|---|
| Data Processing | Python (Pandas, NumPy) |
| Analysis | Jupyter Notebook |
| Visualization | Tableau Public |
| Version Control | Git & GitHub |

## Repository Structure

```
online-retail-cohort-rfm/
├── README.md
├── notebooks/
│   └── cohort_rfm_analysis.ipynb
├── data/
│   └── online_retail_II.csv          # atau link ke UCI jika file besar
├── visualizations/
│   ├── cohort_retention.png
│   └── rfm_segments.png
└── requirements.txt
```

## How to Run

```bash
# Clone repository
git clone https://github.com/<!-- TODO: username -->/online-retail-cohort-rfm.git
cd online-retail-cohort-rfm

# Install dependencies
pip install -r requirements.txt

# Jalankan notebook
jupyter notebook notebooks/cohort_rfm_analysis.ipynb
```

---

**📫 Contact:** <!-- TODO: LinkedIn / email kamu -->
