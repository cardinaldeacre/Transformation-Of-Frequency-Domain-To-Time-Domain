# Transformation of Frequency Domain to Time Domain
Proyek ini mendemonstrasikan proses transformasi sinyal digital dari domain waktu ke domain frekuensi menggunakan Fast Fourier Transform (FFT) dan mengembalikannya ke domain waktu menggunakan Inverse Fast Fourier Transform (IFFT). Kode ini menyediakan visualisasi dari setiap langkah, mulai dari sinyal asli, spektrum frekuensi, hingga sinyal yang direkonstruksi.

## Fitur Utama
Pemuatan Sinyal Audio: Memuat file audio dalam format WAV.

Visualisasi Sinyal Waktu: Menampilkan grafik sinyal audio di domain waktu (Amplitudo vs. Waktu).

Analisis Frekuensi: Menggunakan FFT untuk menghitung dan memvisualisasikan spektrum frekuensi sinyal, menunjukkan komponen-komponen nada yang dominan.

Identifikasi Frekuensi Dominan: Menemukan frekuensi dengan magnitudo tertinggi dalam spektrum.

Rekonstruksi Sinyal: Menggunakan IFFT untuk mengubah kembali spektrum frekuensi menjadi sinyal domain waktu yang hampir identik dengan sinyal asli.

Perbandingan: Memvisualisasikan perbedaan antara sinyal asli dan sinyal yang direkonstruksi untuk validasi akurasi transformasi.

## Analisis dan Refleksi
Proses Eksperimen:

Pengambilan dan Pemuatan Sinyal Suara: Sinyal suara dari file .wav dimuat menggunakan scipy.io.wavfile.read dan dinormalisasi untuk menjaga konsistensi amplitudo.

Analisis Spektrum Frekuensi (FFT): Sinyal diubah dari domain waktu ke domain frekuensi dengan numpy.fft.fft. Spektrum magnitudo yang dihasilkan menunjukkan komponen frekuensi dominan, seperti yang terlihat pada puncak-puncak grafik.

Identifikasi Frekuensi Dominan: Frekuensi dominan diidentifikasi dengan mencari puncak tertinggi dalam spektrum frekuensi positif.

Rekonstruksi Sinyal Waktu (IFFT): Hasil FFT digunakan untuk merekonstruksi sinyal kembali ke domain waktu dengan numpy.fft.ifft. Bagian riil dari hasilnya diambil sebagai sinyal yang direkonstruksi.

Visualisasi dan Perbandingan: Grafik sinyal asli, sinyal yang direkonstruksi, dan grafik perbedaannya menunjukkan bahwa proses transformasi berjalan dengan baik, di mana sinyal rekonstruksi sangat mirip dengan aslinya, dan perbedaannya mendekati nol.

Persyaratan Sistem
Python 3.x

Jupyter Notebook atau Jupyter Lab

Pustaka numpy, matplotlib, scipy, dan IPython.

Cara Menggunakan
* Pastikan semua pustaka yang diperlukan telah terinstal.
* Unggah file transformation-of-frequency-domain-to-time-domain.ipynb ke lingkungan Jupyter Anda.
* Jalankan setiap sel di notebook secara berurutan untuk melihat setiap tahapan dari proses transformasi.
