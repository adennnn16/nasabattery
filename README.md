# Battery Capacity Degradation Prediction

Repository ini berisi implementasi *Data Science Pipeline* dan analisis komparatif model Machine Learning (*Random Forest*, *Gradient Boosting*, dan *LSTM*) untuk memprediksi penurunan kapasitas baterai (*State of Health*) berbasis dataset siklus baterai NASA.

## 📊 Ringkasan Hasil Evaluasi

| Model | RMSE (Ah) | MAE (Ah) | $R^2$ Score |
| :--- | :---: | :---: | :---: |
| **Gradient Boosting Regressor (Terbaik)** | **0.0955** | **0.0475** | **0.9129** |
| Random Forest Regressor | 0.1143 | 0.0408 | 0.8752 |
| LSTM Deep Learning | 0.2160 | 0.1154 | 0.5543 |

## 🛠️ Data Science Pipeline
1. **Data Cleansing:** Memverifikasi integritas dataset (1.415 baris, 0 missing values).
2. **Feature Engineering:** Ekstraksi *Health Indicators* (`vol_rolling_mean` & `temp_rolling_mean` 3-siklus).
3. **Data Splitting & Scaling:** Pembagian *Train-Test* 80:20 & standarisasi skala menggunakan `StandardScaler`.
4. **Modelling & Benchmark:** Membandingkan metode Ensemble (Bagging vs Boosting) dan Deep Learning (LSTM).

## 🚀 Cara Menjalankan Kode
1. Clone repository:
   ```bash
   git clone [https://github.com/USERNAME_KAMU/battery-degradation-prediction.git](https://github.com/USERNAME_KAMU/battery-degradation-prediction.git)
   cd battery-degradation-prediction
