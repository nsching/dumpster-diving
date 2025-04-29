# Dumpster Diving (RealWaste Dataset)

This project focuses on building machine learning models to detect and classify different types of waste from images. The goal is to make waste management more efficient, adaptable, and sustainable, especially in regions like Hawaii, where geographic isolation and environmental sensitivity make waste handling particularly challenging.

---

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Models](#models)
- [Installation](#installation)
- [Usage](#usage)
- [Acknowledgments](#acknowledgments)
- [Authors](#authors)

---

## Introduction

With the rapid increase in global waste generation, traditional manual sorting methods are proving inadequate due to being labor-intensive, inconsistent, and costly.  
Machine learning, particularly computer vision-based systems, offers a scalable and consistent alternative.

This project develops two models:
- **ResNet18 (pretrained and fine-tuned)**
- **Custom Convolutional Neural Network (CustomCNN)**

These models classify waste into categories like plastic, metal, glass, and organic materials, aiming to improve recycling rates, reduce landfill use, and optimize waste management systems.

---

## Dataset

The dataset used is the **RealWaste** dataset, collected under real landfill conditions.

- **Total images**: ~4,752
  - **Training**: 3,040 images
  - **Validation**: 761 images
  - **Testing**: 951 images
- **Classes**:
  - Cardboard
  - Food Organics
  - Glass
  - Metal
  - Miscellaneous Trash
  - Paper
  - Plastic
  - Textile Trash
  - Vegetation

Source:  
- Kaggle: [RealWaste Dataset](https://www.kaggle.com/datasets/joebeachcapital/realwaste/data)  
- Publication: [MDPI Paper](https://www.mdpi.com/2078-2489/14/12/633)

---

## Models

**1. ResNet18**  
- A pretrained deep CNN with residual connections.
- Fine-tuned on the RealWaste dataset for waste classification.

**2. CustomCNN**  
- Built from scratch with three convolutional layers, ReLU activations, max-pooling, and two dense layers.
- Tailored specifically for the RealWaste dataset to compare against a standard deep learning model.

**Preprocessing & Augmentation**:
- Resize and random crop to 224×224 pixels
- Pixel scaling (0–1) and normalization (mean and std per color channel)
- Random cropping and resizing for augmentation during training

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/dumpster-diving.git
   cd dumpster-diving

## Acknowledgments

I would like to express my sincere gratitude to the following individuals and resources that supported and inspired this project:

- **RealWaste Dataset Authors**: For providing a high-quality, real-world dataset for waste classification research.  
- **MDPI Publication**: For documenting the dataset creation and offering valuable insights into waste classification challenges.  
- **Kaggle Community**: For hosting and maintaining access to the RealWaste dataset.  
- **PyTorch Developers**: For providing the tools necessary to build and train deep learning models efficiently.  
- **Open-source Libraries**: Including NumPy, Matplotlib, and scikit-learn, which were critical for data handling, visualization, and evaluation.
- **Academic Instructors and Mentors**: Haopeng Zhang, for guidance and feedback throughout the project development process.

This project would not have been possible without these contributions and resources.

## Authors

- Jubin Choi
- Natalie Ching
- Myra Ortigosa
