# Autoencoder Image Reconstruction

Proyek rekonstruksi citra berbasis **Autoencoder** menggunakan citra udara (*overhead aerial imagery*) yang memuat objek seperti pesawat dan mobil.

## Overview

Proyek ini mengeksplorasi penggunaan Autoencoder untuk mempelajari representasi kompak (*latent representation*) dari citra udara dan merekonstruksi kembali citra tersebut dari representasi terkodekan.

Beberapa arsitektur Autoencoder dan konfigurasi training diuji-cobakan untuk meningkatkan kualitas rekonstruksi. Model dievaluasi menggunakan **Structural Similarity Index Measure (SSIM)**.

## Dataset

Proyek ini menggunakan **citra udara (overhead aerial imagery)** yang memuat objek seperti:

- Pesawat (airplanes)
- Mobil (cars)

Citra-citra tersebut digunakan sebagai input Autoencoder untuk mempelajari representasi terkompresi dan merekonstruksi kembali informasi visual aslinya.

> **Catatan:** Tambahkan detail dataset di sini, misalnya sumber dataset, jumlah gambar, resolusi, format file, dan tautan unduhan (jika publik).

## Objectives

- Mempelajari representasi kompak dari citra udara
- Merekonstruksi citra dari representasi terkodekan (encoded)
- Bereksperimen dengan berbagai arsitektur Autoencoder
- Melakukan hyperparameter tuning
- Membandingkan kualitas rekonstruksi menggunakan SSIM
- Memilih model dengan performa terbaik

## Methodology

```text
Overhead Image
      ↓
   Encoder
      ↓
Latent Representation
      ↓
   Decoder
      ↓
Reconstructed Image
```

Alur kerja umum:

1. **Preprocessing** — normalisasi, resize, dan augmentasi citra input.
2. **Encoding** — encoder memetakan citra ke ruang laten berdimensi lebih rendah.
3. **Decoding** — decoder merekonstruksi citra dari representasi laten.
4. **Evaluasi** — kualitas rekonstruksi diukur menggunakan SSIM (dan opsional metrik lain seperti MSE/PSNR).
5. **Perbandingan model** — beberapa arsitektur/konfigurasi dibandingkan untuk memilih model terbaik.

## Project Structure

```text
.
├── data/                # Dataset citra udara (train/val/test)
├── notebooks/           # Notebook eksperimen dan eksplorasi
├── src/                 # Kode sumber (model, training, evaluasi)
│   ├── models.py
│   ├── train.py
│   └── evaluate.py
├── results/             # Hasil rekonstruksi & log eksperimen
├── requirements.txt
└── README.md
```

> Sesuaikan struktur di atas dengan struktur folder proyek yang sebenarnya.

## Requirements

```text
python>=3.9
torch
torchvision
numpy
matplotlib
scikit-image
```

Instalasi dependensi:

```bash
pip install -r requirements.txt
```

## Usage

```bash
# Training model
python src/train.py --config configs/default.yaml

# Evaluasi model (SSIM)
python src/evaluate.py --checkpoint results/best_model.pth
```

> Sesuaikan perintah di atas dengan skrip dan argumen yang benar-benar tersedia di proyekmu.

## Results

| Model / Configuration | SSIM | Keterangan |
|------------------------|------|------------|
| Baseline Autoencoder   | -    | -          |
| Deep Autoencoder       | -    | -          |
| Convolutional AE       | -    | -          |

> Isi tabel dengan hasil eksperimen aktual dan tambahkan contoh gambar asli vs hasil rekonstruksi jika memungkinkan.

## Future Work

- Eksplorasi arsitektur Variational Autoencoder (VAE)
- Menambah variasi dan jumlah data untuk generalisasi lebih baik
- Menguji metrik evaluasi tambahan (PSNR, LPIPS)

## License

Tambahkan informasi lisensi proyek di sini.
