# 🧼 Denoising AutoEncoder for Pistachio Images
This project is part of a deep learning assignment where we were tasked to build an AutoEncoder architecture to reconstruct noisy images using a technique known as denoising. Since our dataset did not contain noisy samples, we simulated noise using Gaussian Noise to generate a more realistic scenario.

## 🎯 Project Objective
The main goal is to create a model that can:

Learn to remove noise from images

Reconstruct the clean version of a noisy input

Apply this approach to real-world data, such as cleaning noisy camera outputs 🧠📷

In real-life applications, camera sensors often introduce unwanted noise in captured images. This project simulates that scenario and builds a tool that learns to recover clean data.

## 🥜 Dataset: Pistachio Images
We use images of two varieties of pistachio:

🌰 Siirt

🌰 Kirmizi

All images are resized to 100x100 pixels and used as the basis for training and testing our models.

## 🛠️ Approaches Implemented
### 1️⃣ Regular AutoEncoder
A classic convolutional autoencoder built with an encoder–bottleneck–decoder architecture:

🔹 Encoder compresses the input image (100x100) into a dense latent representation (25x25), extracting essential features.
🔸 Decoder reconstructs the original image from the bottleneck, effectively learning to ignore the noise and produce a clean output.

Symmetrical 'hourglass' design, ideal for feature extraction and noise removal.
🧠 The model learns by minimizing reconstruction loss between the original clean image and the denoised output.

### 2️⃣ U-Net Architecture
A powerful model originally designed for biomedical segmentation, U-Net enhances denoising performance by using skip connections:

🔄 Skip connections allow the model to retain high-resolution information by passing it directly from encoder to decoder.
🧬 This helps preserve finer image details that might otherwise be lost in the bottleneck.

Especially effective for small datasets where preserving input fidelity is critical.

# Future Exploration:
- Increase the noise and make the dataset more variational to make the model to be more reliable