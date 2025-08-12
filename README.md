# Transformation of Frequency Domain to Time Domain

Proyek ini mendemonstrasikan proses transformasi sinyal digital **dari domain waktu ke domain frekuensi** menggunakan **Fast Fourier Transform (FFT)** dan mengembalikannya ke domain waktu menggunakan **Inverse Fast Fourier Transform (IFFT)**.  
Kode ini menyediakan **visualisasi dari setiap langkah**, mulai dari sinyal asli, spektrum frekuensi, hingga sinyal yang direkonstruksi.

---

## ✨ Fitur Utama
- **Pemuatan Sinyal Audio**: Memuat file audio dalam format `.wav`.
- **Visualisasi Sinyal Waktu**: Menampilkan grafik sinyal audio di domain waktu (*Amplitudo vs. Waktu*).
- **Analisis Frekuensi**: Menggunakan FFT untuk menghitung dan memvisualisasikan spektrum frekuensi sinyal.
- **Identifikasi Frekuensi Dominan**: Menemukan frekuensi dengan magnitudo tertinggi dalam spektrum.
- **Rekonstruksi Sinyal**: Menggunakan IFFT untuk mengubah kembali spektrum frekuensi menjadi sinyal domain waktu.
- **Perbandingan**: Memvisualisasikan perbedaan antara sinyal asli dan sinyal yang direkonstruksi untuk validasi.

---

## 🔍 Analisis dan Refleksi

### Proses Eksperimen
1. **Pengambilan dan Pemuatan Sinyal Suara**  
   - Memuat sinyal `.wav` dengan `scipy.io.wavfile.read`.  
   - Normalisasi amplitudo untuk konsistensi nilai.

2. **Analisis Spektrum Frekuensi (FFT)**  
   - Mengubah sinyal dari domain waktu ke domain frekuensi dengan `numpy.fft.fft`.  
   - Spektrum magnitudo menunjukkan komponen frekuensi dominan (puncak grafik).

3. **Identifikasi Frekuensi Dominan**  
   - Mencari puncak tertinggi pada spektrum frekuensi positif.

4. **Rekonstruksi Sinyal Waktu (IFFT)**  
   - Mengubah kembali ke domain waktu dengan `numpy.fft.ifft`.  
   - Mengambil bagian riil dari hasil sebagai sinyal rekonstruksi.

5. **Visualisasi dan Perbandingan**  
   - Menampilkan grafik sinyal asli, rekonstruksi, dan selisihnya.  
   - Hasil menunjukkan perbedaan mendekati nol, menandakan rekonstruksi akurat.

---

## ⚙️ Persyaratan Sistem
- **Python** 3.x  
- **Jupyter Notebook** atau **Jupyter Lab**  
- Pustaka:
  - `numpy`
  - `matplotlib`
  - `scipy`
  - `IPython`

---

## 🚀 Cara Menggunakan
1. Pastikan semua pustaka yang diperlukan sudah terinstal:
   ```bash
   pip install numpy matplotlib scipy ipython
2. Unggah file transformation-of-frequency-domain-to-time-domain.ipynb ke lingkungan Jupyter.
3. Jalankan setiap sel secara berurutan untuk melihat seluruh proses transformasi.
