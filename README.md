# Uts-Data-Mining-Klasifikasi-memprediksi-kualitas-anggur

1. Data

Data terdiri dari 857 sampel training dan 286 sampel testing, dengan 11 variabel yang menggambarkan kandungan kimia wine. Kualitas wine menjadi target prediksi dengan nilai 3 sampai 8. Sebagian besar data berada pada kualitas 5 dan 6, sedangkan kualitas lainnya memiliki jumlah data lebih sedikit. Hal ini menunjukkan bahwa data tidak seimbang.

2. Persiapan dan Pembersihan Data

Pada tahap pembersihan, tidak ditemukan nilai kosong maupun data duplikat. Pencilan tetap dipertahankan karena dianggap masih wajar dan bukan kesalahan data. Normalisasi dilakukan pada model yang membutuhkan skala data yang sama, seperti KNN, SVM, dan Logistic Regression.

3. Analisis Hubungan Variabel

Hasil analisis menunjukkan bahwa alcohol memiliki hubungan positif dengan kualitas wine, artinya semakin tinggi kadar alkohol, kualitas wine cenderung meningkat. Sebaliknya, volatile acidity memiliki hubungan negatif, sehingga semakin tinggi kadarnya, kualitas wine cenderung menurun. Sementara itu, variabel lainnya memiliki hubungan yang lebih rendah.

4. Pembuatan Model

Dilakukan perbandingan terhadap tujuh model Machine Learning. Hasilnya menunjukkan bahwa Extra Trees memiliki akurasi CV tertinggi sebesar 63,4%, diikuti Random Forest sebesar 62,9%. Meskipun Extra Trees sedikit lebih tinggi, Random Forest dipilih sebagai model akhir karena lebih mudah dijelaskan dan dapat menunjukkan variabel yang paling berpengaruh. Setelah dilakukan pencarian parameter terbaik, akurasi CV meningkat menjadi sekitar 64,1%.

5. Evaluasi Model

Hasil pengujian Random Forest memperoleh akurasi sebesar 61,05%. Artinya, sekitar 6 dari 10 prediksi berhasil sesuai dengan nilai sebenarnya. Selain itu, sekitar 99,4% prediksi memiliki selisih maksimal satu tingkat dari kualitas sebenarnya. Model paling baik memprediksi kualitas 5 dan 6, tetapi masih kesulitan memprediksi kualitas 3, 4, dan 8 karena jumlah datanya sedikit.

6. Variabel Paling Berpengaruh

Berdasarkan hasil feature importance, variabel yang paling berpengaruh dalam memprediksi kualitas wine adalah volatile acidity dengan nilai 0,145, diikuti sulphates sebesar 0,123 dan alcohol sebesar 0,115. Hal ini menunjukkan bahwa ketiga variabel tersebut memiliki kontribusi terbesar dalam proses prediksi model.

7. Prediksi Data Testing

Setelah model selesai dibuat, Random Forest dilatih kembali menggunakan seluruh 857 data training untuk memprediksi 286 data testing. Hasil prediksi paling banyak berada pada kualitas 5 sebanyak 133 sampel dan kualitas 6 sebanyak 126 sampel. Sementara itu, kualitas 7 sebanyak 26 sampel dan kualitas 8 sebanyak 1 sampel. Tidak terdapat prediksi pada kualitas 3 dan 4.

Kesimpulan: Secara keseluruhan, Random Forest mampu memprediksi kualitas wine dengan akurasi 61,05%. Variabel yang paling berpengaruh adalah volatile acidity, sulphates, dan alcohol. Namun, model masih memiliki keterbatasan dalam memprediksi kelas yang jumlah datanya sedikit. Oleh karena itu, diperlukan penambahan data dan teknik penyeimbangan kelas agar hasil prediksi menjadi lebih baik.
