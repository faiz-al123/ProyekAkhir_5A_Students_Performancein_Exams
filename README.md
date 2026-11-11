# Students Performance Dataset - EDA & Data Preprocessing

## 📌 Deskripsi Project

Project ini bertujuan untuk melakukan **Exploratory Data Analysis (EDA)** dan **Data Preprocessing** pada dataset Students Performance. Analisis dilakukan untuk memahami karakteristik data siswa, menemukan pola hubungan antarvariabel, serta mempersiapkan dataset agar dapat digunakan dalam proses Machine Learning.

Dataset berisi informasi mengenai karakteristik siswa, latar belakang pendidikan orang tua, jenis makan siang, keikutsertaan dalam kursus persiapan ujian, serta nilai akademik siswa pada mata pelajaran matematika, membaca, dan menulis.

## 🎯 Tujuan Project

1. Memahami struktur dan karakteristik dataset.
2. Mengidentifikasi missing values dan data duplikat.
3. Menganalisis distribusi data kategorikal dan numerik.
4. Mengidentifikasi kemungkinan outlier.
5. Menganalisis korelasi antarvariabel.
6. Melakukan feature engineering.
7. Melakukan encoding pada data kategorikal.
8. Melakukan standardisasi data numerik.
9. Mempersiapkan dataset untuk kebutuhan Machine Learning.

## 📂 Dataset

Dataset yang digunakan adalah **StudentsPerformance.csv**.

Dataset memiliki 1.000 baris data dan 8 kolom.

### Atribut Dataset

| No | Atribut | Keterangan | Tipe Data |
|---|---|---|---|
| 1 | gender | Jenis kelamin siswa | Kategorikal |
| 2 | race/ethnicity | Kelompok etnis siswa | Kategorikal |
| 3 | parental level of education | Tingkat pendidikan orang tua | Kategorikal |
| 4 | lunch | Jenis makan siang siswa | Kategorikal |
| 5 | test preparation course | Keikutsertaan kursus persiapan ujian | Kategorikal |
| 6 | math score | Nilai matematika | Numerik |
| 7 | reading score | Nilai membaca | Numerik |
| 8 | writing score | Nilai menulis | Numerik |

## 🛠️ Tools dan Library

Project ini menggunakan beberapa tools dan library Python:

- **Google Colab** – Environment untuk menjalankan kode Python.
- **Pandas** – Manipulasi dan analisis data.
- **NumPy** – Operasi numerik.
- **Matplotlib** – Visualisasi data.
- **Seaborn** – Visualisasi statistik.
- **Scikit-learn** – Preprocessing dan persiapan Machine Learning.

## 🔍 Exploratory Data Analysis (EDA)

Tahapan EDA yang dilakukan meliputi:

1. **Data Understanding**
   - Melihat lima data pertama dan terakhir.
   - Memeriksa informasi dataset.
   - Melihat tipe data dan dimensi dataset.
   - Menghitung statistik deskriptif.

2. **Missing Values Analysis**
   - Memeriksa jumlah missing values.
   - Menghitung persentase missing values.
   - Membuat visualisasi missing values.

3. **Duplicate Data Analysis**
   - Memeriksa jumlah data duplikat.
   - Mengidentifikasi baris yang memiliki nilai identik.

4. **Univariate Analysis**
   - Menganalisis distribusi atribut kategorikal.
   - Menganalisis distribusi nilai matematika, membaca, dan menulis.

5. **Outlier Analysis**
   - Menggunakan boxplot untuk mengidentifikasi kemungkinan outlier.

6. **Bivariate Analysis**
   - Menganalisis korelasi antar nilai akademik.
   - Membandingkan rata-rata nilai berdasarkan gender.
   - Membandingkan rata-rata nilai berdasarkan keikutsertaan dalam test preparation course.

## ⚙️ Data Preprocessing

Tahapan preprocessing yang dilakukan:

1. **Copy Dataset**
   - Membuat salinan dataset untuk menjaga data asli.

2. **Remove Duplicate**
   - Menghapus baris data duplikat menggunakan `drop_duplicates()`.

3. **Handle Missing Values**
   - Mengisi missing values numerik menggunakan median.
   - Mengisi missing values kategorikal menggunakan modus.

4. **Outlier Detection**
   - Mengidentifikasi outlier menggunakan metode Interquartile Range (IQR).
   - Mempertahankan nilai ekstrem yang masih valid.

5. **Feature Engineering**
   - Membuat fitur `total_score`.
   - Membuat fitur `average_score`.

6. **Categorical Encoding**
   - Mengubah atribut kategorikal menggunakan One-Hot Encoding.

7. **Feature Scaling**
   - Melakukan standardisasi menggunakan StandardScaler.

8. **Train Test Split**
   - Membagi dataset menjadi 80% data training dan 20% data testing.

9. **Pipeline Preprocessing**
   - Menggunakan ColumnTransformer dan Pipeline untuk menghindari data leakage pada proses pemodelan.

## 📊 Hasil Pemeriksaan Awal Dataset

Berdasarkan pemeriksaan awal, diperoleh hasil sebagai berikut:

| Pemeriksaan | Hasil |
|---|---|
| Jumlah baris | 1.000 |
| Jumlah kolom | 8 |
| Missing values | 0 |
| Data duplikat | 0 |
| Atribut numerik | 3 |
| Atribut kategorikal | 5 |

**Catatan:** Dataset tidak memiliki missing values maupun data duplikat. Oleh karena itu, proses penghapusan duplikat tidak mengurangi jumlah baris data.

## 🚀 Cara Menjalankan Project

1. Buka Google Colab melalui https://colab.research.google.com/
2. Upload notebook project.
3. Upload file `StudentsPerformance.csv`.
4. Jalankan setiap cell secara berurutan mulai dari import library hingga preprocessing.
5. Periksa hasil visualisasi EDA.
6. Jalankan tahapan preprocessing.
7. Simpan hasil preprocessing dalam format CSV.

## 📁 Struktur Project

```text
StudentsPerformance-EDA-Preprocessing/
│
├── StudentsPerformance.csv
│
├── StudentsPerformance_Preprocessed.csv
│
├── EDA_Preprocessing.ipynb
│
└── README.md
```

## 📝 Kesimpulan

Melalui project ini, dilakukan analisis eksplorasi dan preprocessing terhadap dataset Students Performance untuk memahami karakteristik data serta mempersiapkannya sebelum digunakan dalam pemodelan Machine Learning.

Tahapan EDA membantu mengidentifikasi pola distribusi, hubungan antarvariabel, dan kemungkinan outlier. Sementara itu, preprocessing dilakukan untuk memastikan data memiliki format dan kualitas yang sesuai untuk kebutuhan analisis lanjutan.

Project ini diharapkan dapat menjadi dasar untuk analisis lebih lanjut mengenai faktor-faktor yang berhubungan dengan performa akademik siswa.
