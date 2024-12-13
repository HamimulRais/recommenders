# Machine Learning - Seefud

## Deskripsi Proyek
Proyek ini bertujuan untuk membangun **sistem rekomendasi** menggunakan dataset berikut:
1. **`product3.csv`**: Berisi data produk.
2. **`user3.csv`**: Berisi data interaksi antara pengguna dan produk. Kolom `InteractionType` dengan nilai **`1`** menandakan bahwa pengguna telah melakukan interaksi dengan produk tertentu.

## Build Model
- **String Encoding**: Menggunakan `StringLookup` untuk mengubah ID pengguna dan produk menjadi indeks numerik.
- **Pembangunan Model**: Menggunakan TensorFlow untuk membuat model rekomendasi berdasarkan embedding pengguna dan produk.
- **Konversi Model**: Model direpresentasikan dalam format yang dapat digunakan untuk implementasi lebih lanjut (misalnya, TensorFlow SavedModel atau TFLite).
- **Penyajian Rekomendasi**: Memberikan rekomendasi produk berdasarkan pola interaksi yang telah ada.

## Persiapan Lingkungan
Instal semua dependensi:
   ```bash
   pip install numpy pandas tensorflow
   ```

Lalu anda dapat mengakses capstone3.ipynb untuk membangun model hingga menyimpan dan convert model. 

