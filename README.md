Citrus Classification using Decision Tree Classifier

Tujuan :
Membuat model klasifikasi untuk membedakan antara buah jeruk (orange) dan anggur (grapefruit) berdasarkan fitur seperti diameter, berat, dan nilai RGB warna kulit buah.

Dataset :
Dataset yang digunakan: [Citrus: Oranges vs Grapefruits](https://www.kaggle.com/datasets/joshmcadams/oranges-vs-grapefruit)

Struktur kolom dalam file `citrus.csv`:
- `name` → label buah (`orange` atau `grapefruit`)
- `diameter` → diameter buah
- `weight` → berat buah
- `red`, `green`, `blue` → nilai RGB warna kulit buah

Tools & Library :
- Python 3.x
- Pandas
- Scikit-learn
- Matplotlib

Tahapan dan Langkah-Langkah :

1. Import Library
Mengimpor library Python yang dibutuhkan untuk membaca data, membangun model, dan evaluasi.

2. Load Dataset
Membaca file `citrus.csv` menggunakan `pandas.read_csv()`.

3. Eksplorasi Data
- Menampilkan contoh data menggunakan `df.head()`
- Mengecek tipe data dan nilai kosong
- Mengecek distribusi buah berdasarkan kolom `name`

4. Encoding Label
Mengubah label buah menjadi nilai numerik:
- `orange → 1`
- `grapefruit → 0`

5. Pisahkan Fitur dan Target
- Fitur (`X`): `diameter`, `weight`, `red`, `green`, `blue`
- Target (`y`): hasil encoding dari kolom `name`

6. Split Dataset
Membagi dataset menjadi data latih dan data uji dengan perbandingan 80:20 menggunakan `train_test_split`.

7. Model Training
Membuat dan melatih model Decision Tree menggunakan `DecisionTreeClassifier`.

8. Prediksi
Melakukan prediksi terhadap data uji menggunakan model yang telah dilatih.

9. Evaluasi Model
Menggunakan metrik:
- Confusion Matrix
- Accuracy
- Precision, Recall, dan F1-score (`classification_report`)

10. Visualisasi Model
Menampilkan struktur pohon keputusan dengan `plot_tree()` untuk melihat alur logika dari model yang dibangun.

Output yang Diharapkan
- Statistik evaluasi model dalam bentuk teks (classification report)
- Visualisasi struktur pohon keputusan

Hasil Akhir
Setelah model dijalankan, pengguna dapat mengetahui jenis buah berdasarkan fitur-fitur input dengan akurasi yang diukur secara objektif menggunakan metrik klasifikasi.

Catatan
- Pastikan hanya dua label yang digunakan: `orange` dan `grapefruit`
- Model ini menggunakan data warna dan ukuran buah sebagai dasar prediksi