Nama : Widya Rustri Pratiwi
NPM : G1A024059
Program Studi : Teknik Informatika
Instansi : Universitas Bengkulu

A. Latar Belakang

Sistem peringatan deforestasi satelit biasa (seperti RADD atau GLAD) sudah bagus dalam memberi tahu LOKASI di mana pohon hilang/gundul. Namun, sistem tersebut TIDAK BISA memberi tahu PENYEBAB mengapa pohon itu hilang.

Apakah karena pembukaan tambang? Apakah untuk jalan baru? Atau lahan pertanian?

Tujuan Proyek Ini: Membangun model Kecerdasan Buatan (AI/Deep Learning) yang secara otomatis bisa menebak PENYEBAB UTAMA dari area hutan yang dirusak berdasarkan data karakteristik satelit.

B. Data Satelit yang Digunakan (Input)

Model AI dalam proyek ini dilatih menggunakan 5 jenis karakteristik (fitur) data dari satelit dan topografi:

1. Radar VV (Satelit Sentinel-1): Mengukur kekasaran permukaan tanah (tidak terhalang oleh awan).


2. Radar VH (Satelit Sentinel-1): Mengukur kerapatan tajuk/daun-daun pohon.


3. Optik SWIR (Satelit Sentinel-2): Mengukur kadar air tanah dan pantulan tanah terbuka.


4. Optik NIR (Satelit Sentinel-2): Mengukur tingkat kesegaran/kesehatan vegetasi.


5. Slope (Topografi SRTM): Mengukur kemiringan kontur lahan/tanah.


C. Kategori Penyebab Deforestasi (Output Prediksi)

Model AI bertugas memprediksi dan mengelompokkan kerusakan hutan ke dalam 4 kategori:

1. Smallholder Agriculture: Pembukaan lahan untuk pertanian skala kecil / kebun masyarakat.
2. Mining: Aktivitas pertambangan (misal tambang emas) yang mengeruk habis lapisan tanah.


3. Road Development: Pembukaan/pembuatan jaringan jalan baru di tengah hutan.


4. Selective Logging: Penebangan pohon secara tebang pilih (diambil kayu-kayu tertentu saja).


D. Cara Kerja Algoritma (Model AI)

1. Data Preprocessing & Scaling: Data sinyal satelit disamakan skalanya agar model AI bisa belajar dengan stabil.
2. Arsitektur Model: Menggunakan Multi-Layer Perceptron (MLPClassifier) yang merupakan bentuk dari Deep Neural Network. Model ini memiliki 2 hidden layer (masing-masing 64 dan 32 neuron) untuk mempelajari pola unik dari tiap penyebab deforestasi.


3. Pembagian Data: Dataset dibagi menjadi data latihan (70%), validasi (15%), dan data pengujian (15%).

E. Hasil Uji Performa Model

Berdasarkan pengujian pada data uji (test set), model berhasil menebak penyebab deforestasi dengan sangat akurat:

- Akurasi Keseluruhan (Accuracy): 94.17%
- Macro F1-Score: 0.9416

Detail Hasil Per Kategori (Classification Report):

text
                   precision    recall  f1-score   support

 Smallholder Agri       0.91      0.97      0.94        30
           Mining       0.91      1.00      0.95        30
 Road Development       1.00      0.90      0.95        30
Selective Logging       0.96      0.90      0.93        30

         accuracy                           0.94       120
        macro avg       0.94      0.94      0.94       120
     weighted avg       0.94      0.94      0.94       120
