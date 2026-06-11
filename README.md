# Analisis Klaster Provinsi Berdasarkan Produksi Komoditas Peternakan

## Project Information
- **Project Name:** Analisis Klaster Provinsi Berdasarkan Produksi Komoditas Peternakan  
- **Created By:** Data Engineering Team 7  
- **Date:** 17 February 2026  
- **Version:** 1.0  

---

# 1. Executive Summary

## 1.1 Project Overview

### Tujuan Project
Mengidentifikasi pola pengelompokan provinsi berdasarkan tingkat produksi komoditas peternakan (daging ayam, sapi, kambing, kerbau, telur, dan susu) di Indonesia pada tahun 2021–2022.

### Scope Project
Project ini mencakup:
- Pengumpulan data produksi 6 komoditas peternakan (daging ayam, sapi, kambing, kerbau, telur, susu) per provinsi tahun 2021–2022.
- Pembersihan dan transformasi data (ETL) untuk menyiapkan data siap analisis.
- Penerapan metode klasterisasi (misalnya K-Means atau Hierarchical Clustering) untuk mengelompokkan provinsi berdasarkan tingkat produksi.
- Interpretasi hasil klaster untuk mengidentifikasi provinsi dengan produksi tinggi, sedang, dan rendah.
- Visualisasi hasil dalam bentuk peta klaster, diagram batang.

### Expected Outcomes
- Pengelompokan Provinsi (Klaster)
- Profil Produksi per Provinsi
- Visualisasi Peta Klaster dan dashboard

### Timeline
Durasi proyek: **3 bulan (Februari – April 2026)**

---

## 1.2 Stakeholders

### Project Owner
Kementerian Pertanian Republik Indonesia

### Team Members
- **Project Manager:** Davin Rafael Suryatmoko 
- **Data Engineer:** Alvian Dwiky Putra Santoso 
- **Data Analyst:** Nadia Tifara Sidiq 

### End Users
- Kementerian Pertanian Republik Indonesia
- Badan Pangan Nasional (Bapanas)
- Direktorat Jenderal Peternakan dan Kesehatan Hewan (Ditjen PKH)
- Peternak

---

# 2. Data Source Analysis

## 2.1 Data Pemerintah

### Source Details
- **Dataset Name:** Struktur Ongkos Total Usaha Ternak dan Unggas di Rumah Tangga dengan Pola Pemeliharaan Dikandangkan, 2017  
- **Data Owner:** Badan Pusat Statistik  
- **URL:** https://www.bps.go.id/id/statistics-table/1/MTk3OCMx/struktur-ongkos-total-usaha-ternak-dan-unggas-di-rumah-tangga-dengan-pola-pemeliharaan-dikandangkan-2017.html  
- **Update Frequency:** Terakhir diperbarui tahun 2017  

### Data Analysis
- **Format Data:** CSV  
- **Volume Data:** 16.8 KB  
- **Time Coverage:** Data tahun 2017 (hasil survei BPS)

### Data Quality
- **Completeness:** Sangat lengkap. Data mencakup pembelian bibit, biaya pakan, obat-obatan, biaya sewa lahan, serta jasa penggembalaan.  
- **Accuracy:** Tinggi (dihasilkan oleh Badan Pusat Statistik).  
- **Consistency:** Baik (kategori biaya konsisten untuk setiap jenis ternak).  
- **Timeliness:** Terbatas karena hanya mencakup kondisi tahun 2017.

---

## 2.2 Dataset Kaggle

### Source Details
- **Dataset Name:** Produksi Peternakan  
- **Creator:** Yulinda Rizky  
- **URL:** https://www.kaggle.com/datasets/yulindarizky/produksi-peternakan  
- **Last Update:** 2024  

### Data Analysis
- **Format Data:** CSV  
- **Size:** 8.12 KB  

### Data Fields
- `provinsi`
- `hasil_produksi`

### Quality Metrics
- **Missing Values:** Rendah karena dataset telah melalui proses pembersihan.  
- **Data Types:** Data numerik untuk produksi dan kategori wilayah.  
- **Consistency:** Konsisten dalam penulisan nama wilayah dan kategori ternak.  
- **Documentation Quality:** Cukup baik dan mudah dipahami.

---

## 2.3 Data Pemerintah

### Source Details
- **Dataset Name:** Indeks Harga yang Diterima Petani (IT), Indeks Harga yang Dibayar Petani (IB), dan Nilai Tukar Petani Subsektor Peternakan (NTPT) serta Perubahannya (2018=100), 2025  
- **Creator/Publisher:** Badan Pusat Statistik  
- **URL:** https://www.bps.go.id/id/statistics-table/2/MTcyMCMy/indeks-harga-yang-diterima-petani--it---indeks-harga-yang-dibayar-petani--ib---dan-nilai-tukar-petani-subsektor-peternakan--ntpt--serta-perubahannya--2018-100-.html  
- **Last Update:** 2 Maret 2026  

### Data Analysis
- **Format Data:** CSV  
- **Volume Data:** 5.3 KB  
- **Time Coverage:** Data tahun 2025 (hasil survei BPS)

### Data Quality
- **Completeness:** Sangat lengkap dengan berbagai indikator harga sektor peternakan.  
- **Accuracy:** Tinggi karena berasal dari Badan Pusat Statistik.  
- **Consistency:** Sangat konsisten karena menggunakan sistem indeks standar.  
- **Timeliness:** Cukup baik karena data relatif terbaru.
