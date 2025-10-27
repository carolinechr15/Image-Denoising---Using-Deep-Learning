# 🧠 Image Denoising using Deep Learning

## 📋 Overview
This project focuses on building a **deep learning model** that can clean or restore images corrupted by noise.  
In real-world scenarios, images often contain unwanted noise due to various factors such as lighting conditions, camera quality, or transmission errors.  
To address this issue, this project applies **image denoising** techniques using a **convolutional autoencoder**, allowing the model to learn how to reconstruct clean images from noisy inputs.

---

## 🖼️ Dataset: Kirmizi Image Dataset
The dataset used in this project is the **Kirmizi image dataset**, which consists of clean and high-quality images.  
Since the dataset does not contain noisy samples, synthetic noise is added to the clean images to simulate real-world noisy data.  

The dataset can be accessed from:  
🔗 [Kirmizi Image Dataset on Google Drive](https://drive.google.com/drive/folders/1R60S-Z9RDXICO3L2dmtTETkaGKMyNJet?usp=drive_link)

### 🧩 Noise Generation Process
To create the noisy dataset, Gaussian noise is added to each clean image using the following parameters:
- **Mean (μ)** = 0.0  
- **Standard Deviation (σ)** = 0.1  

## 🎯 Goals
The main goals of this project are:
1. To build a **deep learning model** capable of removing Gaussian noise from images.  
2. To train the model using pairs of clean and noisy images.  
3. To evaluate the model’s ability to **reconstruct clean images** that are visually and numerically close to the original.

To achieve this, a **Convolutional Autoencoder (CAE)** architecture is implemented:
- **Encoder:** compresses the noisy image into a lower-dimensional latent space.  
- **Decoder:** reconstructs a denoised version from the latent features.

---

## ⚙️ Model Architecture
The **Convolutional Autoencoder** consists of:
- Multiple convolutional layers with ReLU activation
- MaxPooling layers for downsampling
- UpSampling layers for reconstruction
- Output layer with sigmoid activation to map pixel values between [0, 1]

## 🧪 Results & Conclusion
After training the model using the `DL_2.ipynb` notebook, the following results were observed:
- The model successfully learns to remove Gaussian noise and recover clean details from corrupted images.
- Visual comparison shows that the **denoised images** are much cleaner and closer to the original clean data.
- Quantitative metrics such as **PSNR (Peak Signal-to-Noise Ratio)** and **MSE (Mean Squared Error)** demonstrate significant improvement over the noisy input images.
