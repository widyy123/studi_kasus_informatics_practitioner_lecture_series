Nama : Widya Rustri Pratiwi
NPM : G1A024059
Program Studi : Teknik Informatika
Instansi : Universitas Bengkulu

1. Latar Belakang dan Deskripsi Studi Kasus

Proses pemantauan rekapitulasi akademik mahasiswa di perguruan tinggi sering kali membutuhkan waktu untuk mendeteksi indikasi kendala studi secara manual. Dengan memanfaatkan algoritma Machine Learning, pihak pengelola akademik dapat memprediksi potensi risiko keterlambatan kelulusan secara otomatis berbasis data historis rekam jejak studi.

Proyek ini mengimplementasikan teknik Supervised Machine Learning (Multi-Layer Perceptron Classifier) untuk mengklasifikasikan tingkat risiko kelulusan mahasiswa berdasarkan indikator kinerja akademik awal.

2. Fitur Input Data Akademik

Model Machine Learning mengolah 5 variabel fitur input:

1. IPK Early: Rata-rata IPK mahasiswa pada tahun pertama perkuliahan.
2. Persentase Hadir: Persentase kehadiran perkuliahan mahasiswa di kelas.
3. SKS Lulus: Jumlah SKS perkuliahan yang berhasil dituntaskan.
4. Skor TPA: Nilai tes potensi akademik saat penerimaan mahasiswa baru.
5. Jam Belajar Mandiri: Rata-rata durasi belajar mandiri mahasiswa per minggu.

3. Kategori Output Hasil Prediksi

1. Tepat Waktu (Low Risk): Mahasiswa dengan indikator akademik memadai untuk lulus tepat waktu.
2. Waspada (Moderate Risk): Mahasiswa dengan performa rata-rata yang memerlukan evaluasi bimbingan.
3. Berisiko Terlambat (High Risk): Mahasiswa berisiko mengalami kendala studi yang memerlukan penanganan khusus.
