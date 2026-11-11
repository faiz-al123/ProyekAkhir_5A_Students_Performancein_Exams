# Analisis Performa Siswa

Proyek ini melakukan eksplorasi data (Exploratory Data Analysis/EDA) dan preprocessing pada dataset **StudentsPerformance.csv** untuk memahami karakteristik nilai siswa serta menyiapkan data agar dapat digunakan pada analisis atau pemodelan lebih lanjut.

## Anggota Kelompok

| No. | Nama | NIM |
|---|---|---|
| 1 | Nazwa Hummaimah Shiddqin | 2488010039 |
| 2 | Faiz Alfaresi | 2488010012 |
| 3 | Ahmad Aly | 2488010069 |

## Paket dan Teknologi

Proyek dijalankan menggunakan Python, terutama melalui Google Colab.

Paket yang digunakan:
- `pandas` — membaca, mengelola, dan memanipulasi data.
- `numpy` — operasi numerik.
- `matplotlib` — membuat visualisasi data.
- `seaborn` — membuat visualisasi statistik.
- `scikit-learn` — standardisasi fitur numerik menggunakan `StandardScaler` pada tahap preprocessing.

Paket dapat dipasang dengan perintah berikut jika belum tersedia:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Metode

### 1. Exploratory Data Analysis (EDA)

EDA dilakukan untuk memahami struktur dan karakteristik dataset sebelum preprocessing, meliputi:
- Melihat beberapa baris awal dan akhir dataset.
- Memeriksa jumlah baris, kolom, tipe data, dan statistik deskriptif.
- Memeriksa nilai kosong dan data duplikat.
- Menganalisis distribusi fitur kategorikal menggunakan tabel frekuensi dan count plot.
- Menganalisis distribusi nilai matematika, membaca, dan menulis menggunakan histogram.
- Mengidentifikasi sebaran dan kemungkinan pencilan nilai menggunakan boxplot.
- Melihat hubungan antarvariabel numerik melalui heatmap korelasi.
- Membandingkan rata-rata nilai berdasarkan gender dan keikutsertaan dalam test preparation course.

### 2. Preprocessing Data

Tahap preprocessing menyiapkan data untuk analisis lanjutan, meliputi:
- Menyalin dataset mentah agar data asli tetap tersedia.
- Merapikan spasi pada nama kolom dan nilai kategorikal.
- Menghapus data duplikat jika ditemukan.
- Memeriksa agar nilai pada kolom skor berada pada rentang 0–100.
- Membuat fitur baru `average_score` dari rata-rata nilai matematika, membaca, dan menulis.
- Mengubah fitur kategorikal menjadi fitur numerik menggunakan One-Hot Encoding.
- Melakukan standardisasi pada kolom nilai numerik menggunakan `StandardScaler`.

Catatan: jika data akan digunakan untuk machine learning, pembagian data train dan test sebaiknya dilakukan sebelum melakukan fitting scaler. `StandardScaler` harus di-fit hanya pada data train untuk menghindari data leakage.

## Tautan Aplikasi

**Tautan aplikasi**:
1. Eksplorasi: https://colab.research.google.com/drive/1iHwjzjUvUB46e_ccla8TZWQ3ZfOtJut_?usp=sharing
2. Preprocessing: https://colab.research.google.com/drive/1l3sqqJb7Iw3yyWZmmvb_-2GFsmDyJoB1

## Dataset

Dataset yang digunakan adalah `StudentsPerformance.csv`, yang memuat informasi kategorikal siswa serta nilai pada tiga mata pelajaran: matematika, membaca, dan menulis.

Pastikan nama file dan lokasi dataset sesuai dengan yang digunakan pada kode notebook.
