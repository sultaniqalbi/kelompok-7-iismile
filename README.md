# 🧠 Study Group I-Smile: EDA to Machine Learning
## Mini Project — Kelompok 7

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Library-scikit--learn-orange.svg)](https://scikit-learn.org/)
[![XGBoost](https://img.shields.io/badge/Library-XGBoost-red.svg)](https://xgboost.readthedocs.io/)

---

### 📌 Informasi Proyek
* **Laboratorium:** I-Smile · Program Studi S1 Teknik Komputer, Telkom University
* **Nomor Kelompok:** Kelompok 7
* **Judul Proyek:** *Prediksi Risiko Depresi Remaja Berdasarkan Penggunaan Media Sosial dan Gaya Hidup*
* **Jenis Masalah:** Klasifikasi Biner (*Binary Classification*)
* **Target:** `depression_label` (0 = Tidak Depresi, 1 = Depresi)
* **Dataset:** [Teen Mental Health Dataset (Kaggle)](https://www.kaggle.com/datasets/sunil123kumar/social-media-impact-on-mental-health?select=Teen_Mental_Health_Dataset.csv)

---

### 🎯 Pertanyaan Penelitian & Sasaran Pengguna
* **Pertanyaan:** *Berdasarkan pola penggunaan media sosial dan gaya hidup remaja (durasi medsos, platform, durasi tidur, screen time sebelum tidur, performa akademik, aktivitas fisik, serta tingkat stres, kecemasan, dan kecanduan), seberapa akurat kita dapat memprediksi risiko depresi remaja?*
* **Target Pengguna:** Konselor sekolah, psikolog/psikiater anak & remaja, serta orang tua untuk deteksi dini (*early warning system*) sebelum depresi berkembang ke tahap yang lebih parah.

---

### 📊 Karakteristik Dataset
* **Total Baris:** 1.200 baris
* **Total Kolom:** 13 kolom (10 numerik, 3 kategorik)
* **Missing Value:** 0 baris (lengkap)
* **Distribusi Target (Extreme Class Imbalance):**
  * Kelas 0 (Tidak Depresi): 1.169 remaja (97,42%)
  * Kelas 1 (Depresi): 31 remaja (2,58%)
* **Konsekuensi Analisis:** Menggunakan **Stratified Split** dan **Stratified 5-Fold Cross-Validation**. Evaluasi difokuskan pada **Recall, Precision, dan F1-Score**, bukan semata-mata Accuracy (*Accuracy Paradox*).

---

### 🔬 Model yang Dibandingkan

Sesuai materi Hari 1–4 dan Brief Kompetisi I-Smile, kami membandingkan 4 model dari rumpun algoritma berbeda:

| No | Model | Tipe Algoritma | Preprocessing Khusus | Peran |
|:---:|:---|:---|:---|:---|
| 1 | **KNN (K-Nearest Neighbors)** | *Distance-based* | `StandardScaler` (Wajib) + `GridSearchCV` ($k$ ganjil 1–21) | **Model Standar Wajib** (Baseline) |
| 2 | **Decision Tree** | *Tree-based* | Tanpa Scaling | Model *White-Box* & Pembelajaran Overfitting |
| 3 | **Random Forest** | *Ensemble (Bagging)* | Tanpa Scaling | **Model Utama / Rekomendasi Tabular** |
| 4 | **XGBoost** | *Ensemble (Boosting)* | Tanpa Scaling | Komparasi Boosting vs Bagging |

---

### 📂 Struktur Direktori
```text
├── Brief Mini Project - Study Group I-Smile.md   # Panduan & rubrik penilaian resmi
├── Kelompok_7_Final.ipynb                       # Notebook lengkap (EDA s/d Evaluasi)
├── Salinan_dari_Kelompok_7.ipynb                # Notebook awal tim
├── Teen_Mental_Health_Dataset.csv               # Dataset penelitian (1200 baris)
├── README.md                                    # Dokumentasi proyek
└── .gitignore                                   # File pengabaian git
```

---

### 🚀 Cara Menjalankan Notebook

#### A. Menggunakan Google Colab (Direkomendasikan)
1. Buka [Google Colab](https://colab.research.google.com/).
2. Pilih tab **Upload** dan unggah file `Kelompok_7_Final.ipynb`.
3. Unggah file `Teen_Mental_Health_Dataset.csv` ke area file session Google Colab.
4. Klik **Runtime** → **Run all** (Ctrl + F9). Seluruh 67 sel akan berjalan otomatis tanpa error.

#### B. Menggunakan Lingkungan Lokal (Jupyter / VS Code)
Pastikan dependensi telah terinstal:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```
Jalankan Jupyter Notebook atau VS Code, lalu buka dan run `Kelompok_7_Final.ipynb`.

---

### 👥 Anggota Kelompok 7 & Pembagian Tugas

| No | Nama Anggota | NIM | Kontribusi Utama |
|:---:|:---|:---:|:---|
| 1 | Muhamad Sultani Qalbi Nursalmi | *(NIM)* | Formulasi Masalah, Preprocessing, Modeling & Evaluasi |
| 2 | *(Anggota 2)* | *(NIM)* | Exploratory Data Analysis & Visualisasi Data |
| 3 | *(Anggota 3)* | *(NIM)* | Hyperparameter Tuning & Analisis Model |
| 4 | *(Anggota 4)* | *(NIM)* | Penyusunan Slide Presentasi & Interpretasi Metrik |

---
*Laboratorium I-Smile · Telkom University 2026*
