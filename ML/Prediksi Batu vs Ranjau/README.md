## 📊 Data Exploration: Understanding Mine vs Rock

Pada tahap ini, dilakukan analisis awal untuk memahami perbedaan karakteristik antara **ranjau (Mine)** dan **batu (Rock)** berdasarkan data sonar.

### 🔍 Kode yang digunakan

```python
sonar_data.groupby(60).mean()
```

### 🧠 Penjelasan

* Dataset terdiri dari:

  * **60 fitur numerik (0–59)** → representasi pantulan gelombang sonar
  * **1 label (kolom ke-60)**:

    * `M` = Mine (ranjau)
    * `R` = Rock (batu)

* Fungsi `groupby(60)` digunakan untuk:

  * Mengelompokkan data berdasarkan label (Mine vs Rock)

* Fungsi `.mean()` digunakan untuk:

  * Menghitung rata-rata setiap fitur dalam masing-masing kelompok

### 📈 Tujuan Analisis

Langkah ini bertujuan untuk:

* Melihat **pola rata-rata sinyal sonar** antara Mine dan Rock
* Mengidentifikasi fitur yang memiliki perbedaan signifikan
* Memberikan insight awal sebelum proses training model

### 🔑 Insight

* Nilai rata-rata yang berbeda antar kelas menunjukkan bahwa:

  * Ada pola tertentu yang bisa digunakan untuk klasifikasi
* Model machine learning nantinya akan memanfaatkan pola ini untuk membedakan objek

### 🚀 Kesimpulan

Analisis ini membantu memahami bahwa perbedaan antara Mine dan Rock tidak terlihat secara langsung, tetapi dapat diidentifikasi melalui pola statistik dari data sonar.
