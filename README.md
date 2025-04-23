# Autoencoder CIFAR-10 (Input dan Output Citra Berbeda)

Proyek ini adalah implementasi sederhana dari model Autoencoder menggunakan dataset CIFAR-10, di mana **citra input berwarna** dan **citra target (output) adalah versi grayscale** dari citra tersebut. Model dilatih untuk mengubah citra berwarna menjadi versi hitam-putih.

## 🧠 Arsitektur Model

Model autoencoder terdiri dari:

- **Encoder**:
  - Conv2d (3 → 64) + ReLU
  - Conv2d (64 → 128) + ReLU
- **Decoder**:
  - ConvTranspose2d (128 → 64) + ReLU
  - ConvTranspose2d (64 → 3) + Sigmoid

## 🧾 Dataset

- Dataset: CIFAR-10 (10 kelas gambar kecil ukuran 32x32)
- Di-resize menjadi 128x128 pixel
- Input: Gambar berwarna
- Output: Gambar grayscale (dikonversi ke RGB 3-channel agar bisa dibandingkan)

## ⚙️ Training

- Optimizer: Adam
- Loss Function: Mean Squared Error (MSE)
- Epochs: 20
- Batch Size: 8

## 📉 Grafik Loss

![Training Loss](results/loss_plot.png)

## 🖼️ Contoh Hasil

Berikut beberapa hasil prediksi dari model:

| Input (RGB) | Target (Grayscale) | Output (Predicted) |
|-------------|--------------------|---------------------|
| ![](results/input_0.png) | ![](results/target_0.png) | ![](results/output_0.png) |
| ![](results/input_1.png) | ![](results/target_1.png) | ![](results/output_1.png) |
| ![](results/input_2.png) | ![](results/target_2.png) | ![](results/output_2.png) |

## 📁 Struktur Folder

