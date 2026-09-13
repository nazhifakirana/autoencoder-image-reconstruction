# Autoencoder Image Reconstruction

An Autoencoder-based image reconstruction project using overhead aerial imagery containing objects such as airplanes and cars.

## Overview

This project explores the use of an Autoencoder to learn compact representations of overhead images and reconstruct them from their encoded representations.

Different Autoencoder architectures and training configurations were experimented with to improve reconstruction quality. The models were evaluated using the **Structural Similarity Index Measure (SSIM)**.

## Dataset

The project uses **overhead aerial imagery** containing objects such as:

- Airplanes
- Cars

The images are used as input to the Autoencoder to learn compressed representations and reconstruct the original visual information.

## Objectives

- Learn compact representations from overhead aerial images
- Reconstruct images from their encoded representations
- Experiment with different Autoencoder architectures
- Perform hyperparameter tuning
- Compare reconstruction quality using SSIM
- Select the best-performing model

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
