# hpc-local-challenges-analytics

Berikut versi teks polos tanpa format bold dan tanpa emotikon:

# Bridging Global Infrastructure to Address Local Challenge with HPC

Deskripsi Proyek
Proyek ini dibuat untuk memenuhi tugas Informatics Practitioner Lecture Series pada sesi kedua bertema Bridging Global Infrastructure to Address Local Challenge with HPC bersama narasumber Asst. Prof. Dr. Worawan Diaz Carballo dari Thammasat University. Proyek ini berfokus pada studi kasus penerapan High Performance Computing (HPC) dan algoritma Machine Learning untuk mensimulasikan akselerasi prediksi kualitas udara (kadar partikel PM2.5) berdasarkan parameter cuaca lokal, sebagai bentuk penyelesaian tantangan nyata di masyarakat.

Pertanyaan Analitis & Pendekatan

1. Descriptive Analytics: Mengetahui distribusi serta nilai rata-rata konsentrasi PM2.5 berdasarkan data sensor lingkungan.
2. Diagnostic Analytics: Mengidentifikasi hubungan korelasi antara parameter cuaca (suhu, kelembapan, kecepatan angin) terhadap peningkatan polusi PM2.5.
3. Predictive Analytics: Membangun model pemodelan regresi (Random Forest Regressor) dengan paralisasi komputasi (n_jobs=-1) untuk memprediksi kadar PM2.5 secara akurat.
4. Prescriptive Analytics: Memanfaatkan pemrosesan HPC agar prediksi kualitas udara dapat diperbarui dalam hitungan menit untuk mendukung sistem peringatan dini publik.

Teknologi & Library

* Bahasa Pemrograman: Python 3.x
* Environment: Google Colab / Jupyter Notebook
* Library Utama: pandas, numpy, scikit-learn

Struktur Repositori
.
├── pm25_hpc_dataset.csv
├── hpc_pm25_prediction.ipynb
└── README.md

Hasil Evaluasi Model
Berdasarkan pengujian model Random Forest Regressor menggunakan paralisasi komputasi pada data uji, diperoleh metrik evaluasi sebagai berikut:

* Mean Absolute Error (MAE): 2.19
* Root Mean Squared Error (RMSE): 2.71
* R-squared (R2 Score): 0.92 (Model mampu menjelaskan 92% variasi data)
