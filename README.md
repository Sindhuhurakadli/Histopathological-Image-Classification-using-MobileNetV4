# Histopathological-Image-Classification-using-MobileNetV4

**This project classifies breast cancer histopathology images using MobileNetV4, achieving 90.87% accuracy. It is lightweight, efficient, and deployable on edge devices, enabling real-time, resource-friendly cancer detection in low-resource settings.**


# 🔬 Histopathological Image Classification using MobileNetV4

## 📌 Project Overview

This project focuses on **breast cancer classification** from **histopathological cell images** using **MobileNetV4**, a state-of-the-art lightweight deep learning model. Breast cancer is one of the leading causes of mortality among women worldwide, and early, accurate diagnosis plays a critical role in treatment and survival.

Traditional diagnosis via **manual histopathological analysis** is accurate but **time-consuming**, subjective, and requires expert pathologists. Our project introduces an **AI-driven pipeline** that leverages **deep learning, transfer learning, and data augmentation** to classify breast tissue samples into **benign (non-cancerous)** or **malignant (cancerous)**.

The uniqueness of this work lies in its optimization for **edge devices** (mobile/embedded systems), enabling **real-time cancer detection without cloud dependency** — particularly useful in **resource-constrained environments** such as rural clinics.


### Dataset

* We used the [**Breast Histopathology Images dataset**](https://www.kaggle.com/datasets/paultimothymooney/breast-histopathology-images) from Kaggle.  
* Contains **277,524 image patches**:  
  * **198,738 benign** samples  
  * **78,786 malignant** samples  
* Dataset split: **80% training (222,019 images)** and **20% validation**.  



### Model Architecture: MobileNetV4

* Built on **lightweight CNN architecture** optimized for mobile/edge devices.
* Core features:

  * **Depthwise Separable Convolutions** → reduces computation cost.
  * **Universal Inverted Bottleneck (UIB)** → enhanced flexibility and multi-scale feature extraction.
  * **Layer scaling & modular blocks** → balances accuracy with efficiency.
* **Optimizer**: Adam (learning rate = 0.001).
* **Activation Function**: ReLU.


## 📊 Results

* Achieved **90.87% accuracy** in classifying benign vs malignant cases.
* Outperforms many traditional ML methods while maintaining **low FLOPs (192.19 MFLOPs)** and just **2.5M parameters** — making it highly efficient.
* Comparison with other architectures:

| Model           | Params | FLOPs | Accuracy   |
| --------------- | ------ | ----- | ---------- |
| **MobileNetV4** | 2.5M   | 192M  | **90.87%** |
| ResNet50        | 25.6M  | 4.1B  | 94.8%      |
| DenseNet-161    | 28.7M  | 7.8B  | 91.57%     |
| EfficientNet-B0 | 5.3M   | 390M  | 93.0%      |

👉 While ResNet/EfficientNet achieve slightly higher accuracy, **MobileNetV4 is far more computationally efficient**, making it ideal for **real-world deployment on mobile/edge devices**.


