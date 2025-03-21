# Customer-Segmentation-Classification
## Overview
Proyek ini bertujuan untuk memprediksi segmentasi pelanggan di pasar baru berdasarkan strategi segmentasi yang telah diterapkan oleh sebuah perusahaan otomotif di pasar sebelumnya. Perusahaan telah berhasil mengelompokkan pelanggan ke dalam empat segmen (A, B, C, D) dan ingin menerapkan pendekatan yang sama untuk 2.627 calon pelanggan baru. Proyek ini akan membandingkan tiga algoritma klasifikasi untuk mencari model terbaik dalam mengklasifikasikan pelanggan.

## Dataset
Dataset yang digunakan dalam proyek ini diperoleh dari Kaggle dengan judul "Customer Segmentation Classification", dan berisi berbagai informasi tentang pelanggan, termasuk:

ID: Identifikasi unik pelanggan
Gender: Jenis kelamin pelanggan
Ever_Married: Status pernikahan pelanggan
Age: Usia pelanggan
Graduated: Apakah pelanggan merupakan lulusan perguruan tinggi
Profession: Profesi pelanggan
Work_Experience: Pengalaman kerja pelanggan dalam tahun
Spending_Score: Skor pengeluaran pelanggan
Family_Size: Jumlah anggota keluarga (termasuk pelanggan)
Var_1: Kategori pelanggan yang telah dianonimkan
Segmentation: Target variable, yaitu kategori segmen pelanggan (A, B, C, D)

## Pre Processing Data
Sebelum melakukan pemodelan, dataset perlu diproses agar siap digunakan. Langkah-langkah preprocessing dilakukan untuk meningkatkan kualitas data dan memastikan model dapat belajar dengan lebih baik.

Langkah pertama yang dilakukan adalah menghapus kolom yang tidak relevan agar analisis lebih fokus pada fitur yang benar-benar berpengaruh terhadap segmentasi pelanggan. Selanjutnya, missing values ditangani untuk memastikan tidak ada informasi yang hilang atau bias dalam data.

Karena distribusi kelas dalam dataset tidak seimbang, dilakukan penyesuaian agar distribusi lebih merata, sehingga model tidak cenderung lebih berpihak pada kelas mayoritas. Penanganan data tidak seimbang dilakukan dengan menggunakan SMOTE, sehingga setiap kategori data kini berjumlah sama, yaitu sebanyak 1814 data. Selain itu, fitur kategorikal dalam dataset dikonversi menggunakan Label Encoding dan One-Hot Encoding, agar dapat dipahami oleh model machine learning.

## Pemodelan
Dilakukan proses pemodelan menggunakan tiga algoritma machine learning yang berbeda. Model yang dipilih untuk klasifikasi ini adalah:

1. Support Vector Machine (SVM): Model ini bekerja dengan mencari hyperplane terbaik untuk memisahkan kelas dalam data.
2. K-Nearest Neighbors (KNN): Algoritma berbasis tetangga terdekat yang mengklasifikasikan pelanggan berdasarkan kesamaan dengan pelanggan lain.
3. Naïve Bayes: Model probabilistik yang menggunakan Teorema Bayes untuk menentukan kemungkinan suatu pelanggan termasuk dalam segmen tertentu.

## Hasil 
Setelah melakukan preprocessing dan menjalankan berbagai model, hasil klasifikasi menunjukkan bahwa performa model masih kurang optimal. Nilai F1-score yang diperoleh berada di bawah 50%, yang menunjukkan bahwa model belum dapat membedakan segmen pelanggan dengan baik. Walaupun pada visualisasi confussion matrix, model terlihat cukup baik dalam mengklasifikasikan dengan benar, namun jumlah kesalahan klasifikasi masih tergolong dalam angka yang cukup besar.

Hal ini bisa disebabkan oleh beberapa faktor, seperti kurangnya fitur yang benar-benar dapat membedakan segmen pelanggan atau kompleksitas hubungan antara fitur yang belum ditangkap dengan baik oleh model yang digunakan.

# Dashboard Analisis
Untuk memahami karakteristik pelanggan dan hasil segmentasi, digunakan dashboard interaktif untuk memudahkan stakeholder dalam memahami hasil analisis dan kondisi pasar secara mudah. Dashboard tersebut dibuat dengan menggunakan aplikasi Looker Studio, dan menampilkan informasi berupa karakteristik pelanggan berdasarkan kategori tertentu, termasuk hasil segmentasi.
