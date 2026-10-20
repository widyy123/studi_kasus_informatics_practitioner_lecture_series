# studi-kasus-late-payment-analytics

Studi kasus ini merupakan analisis data dan pemodelan Machine Learning untuk memprediksi potensi keterlambatan pembayaran tagihan (late payment). Menggunakan dataset historis invoice, model dikembangkan untuk mendeteksi risiko keterlambatan agar tim manajemen dapat mengambil tindakan pencegahan secara tepat waktu.

1. Data Understanding & Preparation:
   * Membaca file dataset `invoices_dataset.csv` secara otomatis dengan deteksi delimiter.
   * Pembersihan nama kolom (`df.columns.str.strip()`).
   * Ekstraksi fitur utama: `customer_segment`, `invoice_amount`, `payment_method`, dan `historical_late_count`.
   * Menghindari data leakage dengan mengeliminasi variabel id (`invoice_id`, `customer_id`) dari fitur pelatihan.

2. Feature Engineering & Preprocessing:
   * Mengubah variabel kategorikal (`customer_segment`, `payment_method`) menggunakan `OneHotEncoder`.

3. Modeling & Evaluation:
   * Pembagian dataset dengan proporsi 80% data latih dan 20% data uji
   * Klasifikasi menggunakan algoritma Random Forest Classifier
   * Evaluasi performa model menggunakan metrik Precision, Recall, F1-Score, dan Accuracy


4. Struktur Repositori:
```text
.
├── invoices_dataset.csv          # File dataset transaksi dan pembayaran invoice
├── notebook_late_payment.ipynb   # File Jupyter Notebook / Google Colab
└── README.md                     # Dokumentasi proyek
