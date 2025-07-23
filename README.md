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
Immaculata Viandra

Capstone Project - Machine Learning @Purwadhika

GitHub: @immaculataviandra

https://www.linkedin.com/in/immaculataviandraap
   
