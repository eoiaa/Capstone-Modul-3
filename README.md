# Capstone Module 3 - Hotel Booking Demand Analysis

## Overview

Proyek ini bertujuan untuk menganalisis permintaan pemesanan hotel dengan menggunakan teknik machine learning. Model yang dibuat akan membantu dalam memprediksi apakah seorang customer akan membatalkan pemesanannya atau tidak, sehingga pihak hotel dapat mengoptimalkan strategi pemesanan dan mengurangi potensi kerugian akibat overbooking atau kamar yang tidak terjual.

## Dataset

Dataset yang digunakan berasal dari sumber pemesanan hotel yang mencakup berbagai fitur seperti:

- **Jenis deposit** (Non Refund, No Deposit, Refundable)
- **Jumlah special request** dari pelanggan
- **Segmentasi pelanggan**
- **Perubahan booking**
- **Durasi waiting list**
- **Jumlah parkir yang dibutuhkan**

## Model Machine Learning

Beberapa model yang diuji dalam proyek ini adalah:

- **Bagging Classifier** (Model terbaik sejauh ini dengan skor tertinggi)
- **GradientBoostingClassifier**
- **LGBMClassifier**
- **AdaBoostClassifier dengan DecisionTree sebagai estimator**

Karena dataset ini bersifat imbalanced (lebih banyak kelas 0 dibanding kelas 1), dilakukan penyesuaian dengan teknik seperti **SMOTE** dan **penyesuaian threshold berdasarkan F0.76** untuk meminimalkan False Positive (FP) dibandingkan False Negative (FN).

## Model Evaluation

Model dievaluasi dengan beberapa metrik, termasuk:

- **F0.76 Score** (F-score yang lebih menekankan penurunan FP dibanding FN)
- **SHAP Values** untuk interpretasi fitur yang paling berpengaruh dalam model
- **LIME** untuk memahami pengaruh tiap fitur dalam prediksi individu
- **Partial Dependence Plot (PDP)** untuk melihat hubungan antara fitur tertentu dengan hasil prediksi

## Business Impact Analysis

Dampak bisnis yang dianalisis dalam proyek ini mencakup:

- **False Positive (FP)**: Prediksi salah bahwa customer akan membatalkan, padahal tidak, yang berujung pada **overbooking** dan dapat menyebabkan kehilangan kepercayaan pelanggan.
- **False Negative (FN)**: Prediksi salah bahwa customer tidak akan membatalkan, padahal sebenarnya membatalkan, yang menyebabkan **kamar tidak terjual**.

## Installation

Untuk menjalankan proyek ini, pastikan memiliki dependensi berikut:

```bash
pip install numpy pandas scikit-learn lightgbm shap lime imbalanced-learn
```

## Usage

Jalankan notebook dengan perintah:

```bash
jupyter notebook Capstone_module3.ipynb
```

## Contributors

- **Nama Anda**

## License

Proyek ini menggunakan lisensi MIT.

