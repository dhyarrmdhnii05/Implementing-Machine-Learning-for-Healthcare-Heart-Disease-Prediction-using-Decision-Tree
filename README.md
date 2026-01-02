# Heart Disease Prediction using Decision Tree 🩺

Proyek ini bertujuan untuk membangun model klasifikasi Machine Learning untuk mendeteksi risiko penyakit jantung berdasarkan data klinis pasien. Proyek ini disusun sebagai bagian dari tugas akhir mata kuliah Kecerdasan Buatan (Artificial Intelligence).

## 📊 Dataset Overview
Dataset yang digunakan adalah **Heart Disease UCI Dataset** yang diperoleh dari platform Kaggle. Dataset ini berisi data medis pasien yang mencakup informasi demografis dan hasil pemeriksaan klinis.

* **Sumber Dataset:** [Kaggle - Heart Disease UCI](https://www.kaggle.com/datasets/mragpavank/heart-diseaseuci)
* **Fitur Utama:** Usia, jenis kelamin, tekanan darah, kadar kolesterol, tipe nyeri dada (`cp`), jumlah pembuluh darah besar (`ca`), dan indikator kesehatan lainnya.

## 🛠️ Tech Stack
* **Bahasa Pemrograman:** Python
* **Lingkungan Pengembangan:** Google Colab
* **Libraries:** NumPy, Pandas, Scikit-Learn, Matplotlib

## 📈 Model Interpretation (Decision Tree)
Model ini menggunakan algoritma **Decision Tree** karena kemampuannya dalam memberikan logika keputusan yang transparan (interpretability).

### Visualisasi Model
<p align="center">
  <img width="600" src="https://github.com/user-attachments/assets/c1fa9756-f47a-4ac9-978b-76e67c47db8a" alt="Decision Tree Visualization" />
</p>

### Key Insights:
1.  **Node Akar (Root Node):** Fitur `cp` (Chest Pain Type) adalah pemisah utama. Ini menunjukkan bahwa jenis nyeri dada adalah faktor paling berpengaruh dalam menentukan risiko penyakit jantung pada dataset ini.
2.  **Cabang Kiri (cp ≤ 0.5):** Dipengaruhi lebih lanjut oleh fitur `ca` (jumlah pembuluh darah besar) dan `exang` (angina akibat olahraga).
3.  **Cabang Kanan (cp > 0.5):** Dipengaruhi oleh `oldpeak` (depresi ST) dan `slope`. Fitur `slope` menjadi pembeda yang sangat kuat pada kelompok dengan `oldpeak` tinggi.

## 🧪 Performance Evaluation
Model dievaluasi menggunakan *testing data* dengan rasio 80:20 (61 sampel).

### Metrics Result
| Metric | Class 0 (Healthy) | Class 1 (Heart Disease) | Overall |
| :--- | :---: | :---: | :---: |
| **Precision** | 0.80 | 0.84 | - |
| **Recall** | 0.83 | 0.81 | - |
| **F1-Score** | 0.81 | 0.83 | - |
| **Accuracy** | - | - | **82%** |

### Confusion Matrix
<p align="center">
  <img width="400" src="https://github.com/user-attachments/assets/93b7a597-1fe3-4c82-b85c-8b1cb7a721b8" alt="Confusion Matrix" />
</p>

**Interpretasi Confusion Matrix:**
* **True Negative:** 24 pasien sehat diprediksi dengan benar.
* **True Positive:** 26 pasien sakit diprediksi dengan benar.
* **False Positive:** 5 pasien sehat diprediksi sakit.
* **False Negative:** 6 pasien sakit diprediksi sehat.

## 📝 Conclusion
Model Decision Tree menunjukkan performa yang stabil dengan akurasi **82%**. Keseimbangan antara *precision* dan *recall* (F1-score 0.81-0.83) menunjukkan model ini cukup handal dalam membedakan kedua kelas. Fokus pengembangan selanjutnya adalah menekan nilai *False Negative* untuk meminimalisir risiko pasien sakit yang tidak terdeteksi.![Uploading Screenshot 2026-01-03 010554.png…]()
