# Prediksi-Minat-Nasabah-terhadap-Produk-Deposito-Berjangka-menggunakan-Model-Machine-Learning

## Latar Belakang:
Dalam sektor perbankan, mengetahui nasabah yang potensial membeli produk seperti deposito berjangka sangat krusial. Dengan data historis, model klasifikasi dibangun untuk membantu pengambilan keputusan berbasis data.

Langkah-langkah Proyek:
1. Import Library:
   - Digunakan berbagai library Python seperti pandas, numpy, scikit-learn, xgboost, lightgbm, catboost, dan matplotlib/seaborn.
2. Data Understanding:
   - Data pelatihan berisi 22.916 baris dan 22 kolom.
   - Tidak terdapat missing values dan data duplikat.
   - Terdapat nilai khusus 999 pada kolom hari_sejak_kontak_sebelumnya yang diartikan sebagai "belum pernah dihubungi".
3. Exploratory Data Analysis (EDA):
   - Visualisasi dilakukan untuk mendeteksi outlier dan distribusi data.
   - Korelasi antar fitur dianalisis untuk mendeteksi multikolinearitas.
4. Preprocessing:
   - Numerik: Dilakukan normalisasi menggunakan MinMaxScaler.
   - Kategorikal:
     Kolom dengan sedikit kategori → Label Encoding.
     Kolom dengan banyak kategori → One-Hot Encoding.
   - Hapus fitur yang tidak relevan.
   - Pastikan struktur kolom konsisten antara data latih dan validasi.
5. Modeling:
   - Dicoba beberapa algoritma: Logistic Regression, Random Forest, Decision Tree, XGBoost, LightGBM, CatBoost.
   - Dilakukan tuning hyperparameter terutama pada model XGBoost karena hasil awalnya paling menjanjikan.
6. Ensemble Learning:
   - Digunakan teknik Stacking untuk menggabungkan model-model terbaik.
   - Model Stacking terdiri dari: XGBoost, LightGBM, CatBoost, dan Random Forest sebagai base models.
7. Evaluasi Model:
   - Metrik yang digunakan: Accuracy, Precision, Recall, F1-score, dan ROC AUC.
   - Model Stacking memberikan hasil terbaik dengan:
     ROC AUC: 0.801
     Accuracy: 0.9003
8. Prediksi dan Output:
   - Output prediksi berupa dua kolom: customer_number dan berlangganan_deposito, sesuai format yang ditentukan oleh lomba.
   - Probabilitas prediksi berada di rentang 0–1.
9. Penutup:
    - Proyek ini disusun untuk mengikuti lomba data science tingkat nasional, dengan pendekatan berbasis machine learning untuk memprediksi perilaku nasabah terhadap produk        deposito. Model ensemble yang digunakan terbukti memberikan performa terbaik dalam klasifikasi biner.
