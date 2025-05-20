# Saudi_Arabia_Used_Car_Analysis


## 1. Gambaran Proyek

Proyek ini bertujuan untuk menganalisis data pasar mobil bekas di Arab Saudi guna menghasilkan wawasan bisnis, meningkatkan pengambilan keputusan, dan mengidentifikasi tren harga yang signifikan. Fokus utama dari proyek ini adalah memprediksi harga mobil bekas berdasarkan berbagai fitur seperti merek, model, tahun pembuatan, jarak tempuh, dan jenis transmisi. Proyek ini ditujukan untuk membantu pembeli, penjual, dan Syarah.com dalam menetapkan harga secara data-driven.

### Tujuan Utama:
- Membangun model prediksi harga mobil bekas berbasis machine learning untuk pasar Arab Saudi, guna menghasilkan estimasi harga yang akurat dan dapat diandalkan.
- Mengidentifikasi dan menganalisis fitur-fitur paling berpengaruh terhadap harga mobil, seperti tahun produksi, kilometer, merk, ukuran mesin, dan lainnya.
- Menyediakan sistem estimasi harga otomatis yang dapat diintegrasikan ke platform Syara.com, sehingga membantu:
    + Penjual menetapkan harga jual yang kompetitif
    + Pembeli memiliki acuan harga wajar
    + Perusahaan mengoptimalkan efisiensi operasional dan margin keuntungan

## 2. Sumber Data

- `data_saudi_used_cars.csv` – Berisi data penjualan mobil bekas di Arab Saudi dengan berbagai fitur seperti merek, model, tahun, jarak tempuh, bahan bakar, transmisi, dan harga.

## 3. Teknologi yang Digunakan

- **Bahasa Pemrograman**: Python (Pandas, NumPy)
- **Pemodelan**: Linear Regression, Ridge Regression, Lasso Regression, Decision Tree, Random Forest, XGBoost, K-Nearest Neighbors, Gradient Boosting Regression
- **Pra-pemrosesan**: OneHotEncoding, BinaryEncoding, Robust Scaler
- **Visualisasi**: Matplotlib, Seaborn, SHAP
- **Evaluasi Model**: MAE, MAPE, Skor R²
- **Optimasi**: GridSearchCV
- **Lainnya**: Jupyter Notebook, Scikit-learn, Yellowbrick, Joblib

## 4. Struktur Proyek
├── README.md

├── data

│   └── raw <- data_saudi_used_cars.csv
│

├── models <- Model yang telah disimpan menggunakan joblib
│

├── notebooks <- Saudi_Arabia_Used_Car.ipynb
│

├── reports <- Visualisasi, SHAP plots, kurva pembelajaran

│   └── figures

## 5. Ringkasan Temuan

### 5.1 Insight Bisnis

- Merek, tahun produksi, dan jarak tempuh merupakan faktor utama yang memengaruhi harga mobil bekas.
- Model XGBoost menunjukkan performa terbaik dibandingkan model dasar lainnya dalam hal akurasi prediksi harga dengan nilai MAPE 24.8%
- Berdasarkan simulasi, tanpa model prediksi, rata-rata selisih harga jual dengan harga wajar dapat menyebabkan kerugian atau kehilangan margin hingga jutaan rupiah per unit.
- Simulasi menunjukkan bahwa jika rata-rata deviasi harga tanpa model sebesar ±15%, maka dengan model prediksi, potensi deviasi dapat ditekan ke bawah 8–10%, sehingga perusahaan lebih kompetitif.

### 5.2 Rekomendasi Tindakan

1. Implementasikan model ini sebagai **alat bantu estimasi harga otomatis** di platform **Syarah.com** untuk memudahkan pengguna dalam menentukan harga jual dan beli.
2. Gunakan model ini untuk **validasi harga otomatis** di listing mobil, dan beri notifikasi jika harga yang diinput terlalu menyimpang dari estimasi.
3. **Update model secara berkala** dengan data terbaru agar tetap relevan dan responsif terhadap tren pasar.
4. Tambahkan fitur baru ke dalam model untuk meningkatkan prediktivitas, seperti:
   - Riwayat servis kendaraan
   - Lokasi geografis kendaraan
   - Warna, jenis bahan bakar, rating kendaraan
   - Popularitas model di pasar lokal
  
### 5.3 Limitasi Model
1. Model belum mempertimbangkan kondisi visual kendaraan secara langsung (misal: bekas kecelakaan atau interior rusak).
2. Penghapusan outlier ekstrem, meskipun meningkatkan performa model, berpotensi menghilangkan mobil dengan harga tinggi yang valid (seperti mobil mewah, mobil langka, atau edisi kolektor).
3. Model memiliki kecenderungan **undervaluing mobil mewah** karena distribusi data cenderung bias terhadap harga menengah dan rendah.
4. Tidak mempertimbangkan faktor eksternal seperti musim, promo dealer, atau fluktuasi ekonomi makro.
5. Model dilatih pada snapshot data, bukan data real-time, sehingga ada keterbatasan dalam memprediksi perubahan harga jangka pendek.

## 6. Kontak

**Nama**: Kirana Azhura

**Email**: kiranaazhuraa08@gmail.com

**LinkedIn**: [Kirana Azhura](https://www.linkedin.com/in/kirana-azhura-8a3b65337/)

