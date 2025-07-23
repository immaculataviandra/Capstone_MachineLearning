# 📦 Costumer Churn Analytics: Data Scientists’ Journey
**Capstone Project - Machine Learning Module**  
By: *Immaculata Viandra*

---

## 🧾 Deskripsi Proyek

Project ini bertujuan untuk membangun model machine learning untuk **memprediksi apakah pelanggan e-commerce akan churn (berhenti menggunakan layanan)** atau tidak. Dengan prediksi ini, perusahaan dapat lebih proaktif dalam mengambil langkah retensi pelanggan yang tepat.

---

## 🎯 Tujuan
- Melakukan analisis eksploratif terhadap data pelanggan
- Membersihkan dan menyiapkan data untuk modeling
- Membangun beberapa model klasifikasi
- Mengevaluasi dan memilih model terbaik
- Menyimpan model terbaik untuk keperluan deployment

---

## 📂 Struktur File

| File | Deskripsi |
|------|-----------|
| `Immaculata Viandra_CAPSTONE M3.ipynb` | Notebook utama berisi proses lengkap dari preprocessing hingga evaluasi model |
| `data_ecommerce_customer_churn.csv` | Dataset yang digunakan dalam project |
| `bestmodel_GradientBoost_v1.sav` | Model terbaik (Gradient Boosting) yang telah disimpan |
| `E-commerce Customer Churn.docx` | Dokumen penjelas (opsional) |
| `Contoh_CapstoneProject_...ipynb` | Draft dan contoh awal project klasifikasi & regresi |

---
## ℹ️ Features
| Features | Description |
| --- | --- |
| Tenure | Lama waktu (dalam bulan) pelanggan telah menggunakan layanan atau menjadi anggota |
| WarehouseToHome | Jarak pengiriman dari gudang/store ke alamat pelanggan (dalam kilometer) |
| NumberOfDeviceRegistered | Jumlah perangkat yang terdaftar oleh pelanggan untuk mengakses platform/website supermarket |
| PreferedOrderCat | Kategori pesanan yang biasa pelanggan beli/suka |
| SatisfactionScore | Skor kepuasan (1, 2, 3, 4, 5) |
| MaritalStatus | Satus perkawinan pelanggan |
| NumberOfAddress | Nomor alamat rumah |
| Complain | Apakah pelanggan pernah komplain? 0 untuk tidak pernah | 1 untuk pernah |
| DaySinceLastOrder | Pembelian terakhir yang dilakukan oleh pelanggan (dalam hari) |
| CashbackAmount | Jumlah cashback yang diberikan kepada pelanggan |

---
### Transformer
<img width="2023" height="358" alt="image" src="https://github.com/user-attachments/assets/f2bcb635-3449-49c4-85fa-b91af7814739" />

---
### Hyperparameter Tuning
<img width="2179" height="750" alt="image" src="https://github.com/user-attachments/assets/7d4e77f3-6eb8-4dd2-8b0f-dc81d0992f5d" />

---
### Confusion Matrix GBoost
<img width="951" height="393" alt="image" src="https://github.com/user-attachments/assets/01e28551-6f36-444c-b078-0b44164843db" />

---
### Interpretation
<img width="797" height="780" alt="image" src="https://github.com/user-attachments/assets/43fbff10-85de-4595-9896-0b0b999e1bf4" />
---
<img width="2291" height="326" alt="image" src="https://github.com/user-attachments/assets/e2e2ad51-f33a-4794-b36e-88de9525a62e" />
---

## 🔧 Tools & Teknologi

- Python (Jupyter Notebook)
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- GradientBoostingClassifier

---

## 📊 Evaluasi Model

Model terbaik dalam project ini adalah **Gradient Boosting Classifier**, dipilih berdasarkan performa yang optimal untuk mendeteksi churn.

### Metrics

#### ✅ False Positive (FP)
- **Definisi:** Model memprediksi pelanggan akan churn (1), padahal sebenarnya pelanggan tidak churn (0).
- **Konsekuensi:**
  - Perusahaan memberikan promosi atau diskon retensi yang sebenarnya tidak diperlukan.
  - Pemborosan anggaran pemasaran kepada pelanggan yang loyal.
- **Dampak:** Biaya retensi meningkat, tetapi tidak langsung merugikan pendapatan.

#### ❌ False Negative (FN)
- **Definisi:** Model memprediksi pelanggan tidak akan churn (0), padahal sebenarnya pelanggan churn (1).
- **Konsekuensi:**
  - Pelanggan yang benar-benar akan churn tidak terdeteksi → tidak ada tindakan retensi.
  - Potensi kehilangan pendapatan dan loyalitas pelanggan.
- **Dampak:** Lebih besar karena bisa menurunkan pertumbuhan dan profitabilitas bisnis.

### 🎯 Fokus Evaluasi: Recall dan F2-Score
- Dalam konteks prediksi churn, **Recall untuk kelas churn (1)** sangat penting.
- Tujuannya adalah **meminimalkan False Negative**, yaitu pelanggan yang churn tapi tidak terdeteksi.
- Oleh karena itu, digunakan **F2-score**, yang lebih menekankan Recall dibanding Precision.

---

## 📈 Hasil Singkat

- **Model:** Gradient Boosting
- **F2-score churn (1):** 0.77%

_Model ini dipilih karena performa F2-nya yang paling optimal dalam mendeteksi pelanggan yang berpotensi churn._

---

## ▶️ Cara Menjalankan

1. Clone repositori ini:
   ```bash
   git clone https://github.com/immaculataviandra/Capstone_MachineLearning.git
2. Jalankan Jupyter Notebook dan buka:
   ```bash
   Immaculata Viandra_CAPSTONE M3.ipynb
3. Model tersimpan (.sav) dapat di-load kembali dengan:
   ```bash
   import joblib
   model = joblib.load("bestmodel_GradientBoost_v1.sav")

## 📝 Catatan Tambahan
Dataset ini bersifat fiktif/sintetik dan digunakan untuk pembelajaran.

Model belum dideploy ke dalam aplikasi, namun sudah siap untuk tahap selanjutnya seperti API deployment atau dashboard dengan Streamlit.

## 🙋‍♀️ Author
Immaculata Viandra.

Capstone Project - Machine Learning @Purwadhika

GitHub: @immaculataviandra

https://www.linkedin.com/in/immaculataviandraap
   
