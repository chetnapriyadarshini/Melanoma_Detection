# Melanoma Detection Using Convolutional Neural Networks

A Jupyter Notebook implementing a multiclass image classification model using a custom Convolutional Neural Network (CNN) in TensorFlow, trained to detect melanoma and other oncological skin conditions from dermoscopic images.

---

## Table of Contents

- [Overview](#overview)
- [Background](#background)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Notebook Contents](#notebook-contents)
- [Technologies Used](#technologies-used)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Results and Conclusions](#results-and-conclusions)
- [References](#references)
- [Contact](#contact)

---

## Overview

Melanoma accounts for approximately 75% of skin cancer-related deaths, yet its prognosis improves dramatically with early detection. This project builds a deep learning-based diagnostic aid that classifies dermoscopic skin images into multiple oncological categories. The model is designed to assist dermatologists by automating the preliminary screening process, reducing the manual effort required in clinical diagnosis.

---

## Background

The International Skin Imaging Collaboration (ISIC) provides standardised dermoscopic image datasets that are widely used in computational dermatology research. This project uses the ISIC archive to train and evaluate a custom CNN classifier capable of distinguishing between malignant and benign skin lesions across multiple disease subtypes.

---

## Dataset

The dataset comprises **2,357 dermoscopic images** of malignant and benign oncological conditions, sourced from the ISIC archive. Images are distributed across multiple classes including melanoma, melanocytic nevi, basal cell carcinoma, actinic keratosis, benign keratosis, dermatofibroma, and vascular lesions. Melanoma and moles are slightly over-represented relative to other classes.

---

## Model Architecture

A custom CNN is constructed in TensorFlow/Keras, comprising convolutional layers with ReLU activations, max-pooling layers for spatial downsampling, batch normalisation, dropout for regularisation, and a softmax output layer for multiclass classification. The architecture avoids the use of pre-trained weights, training entirely from scratch on the ISIC dataset.

---

## Notebook Contents

| Section | Description |
|---|---|
| Data Loading & EDA | Loading images, visualising class distribution, and inspecting sample images |
| Baseline CNN (Model 1) | Training a simple CNN with image rescaling; analysis of overfitting |
| Data Augmentation (Model 2) | Applying random flips, rotations, and zoom to reduce the train–validation accuracy gap |
| Class Imbalance Correction | Using the Augmentor library to balance class frequencies |
| Final Model Training (Model 3) | Training on the rebalanced dataset and evaluating improvement |
| Performance Analysis | Accuracy and loss curves, confusion matrix, observations |

---

## Technologies Used

| Library | Version | Purpose |
|---|---|---|
| `tensorflow` | 2.17.0 | CNN model definition and training |
| `keras` | 3.4.1 | High-level neural network API |
| `augmentor` | 0.2.12 | Image augmentation and class rebalancing |
| `numpy` | 1.24.3 | Numerical operations |
| `pandas` | 2.0.3 | Data handling |
| `matplotlib` | 3.7.2 | Visualisation of training curves and sample images |
| `scikit-learn` | 1.3.0 | Evaluation metrics |
| `python` | 3.10.12 | Runtime environment |

---

## Setup and Installation

```bash
git clone https://github.com/chetnapriyadarshini/Melanoma_Detection.git
cd Melanoma_Detection
pip install tensorflow keras augmentor numpy pandas matplotlib scikit-learn
```

Download the ISIC dataset and place it in the expected directory structure before running the notebook. Refer to the notebook's data loading section for the required folder layout.

Launch the notebook:

```bash
jupyter notebook chetna_priyadarshini_nn.ipynb
```

---

## Usage

Run all notebook cells in sequence. The notebook is structured to progress from a baseline model to progressively improved iterations. Each modelling stage is accompanied by visualisations of training and validation metrics to facilitate analysis of model behaviour.

---

## Results and Conclusions

| Model | Key Observation |
|---|---|
| Baseline (Rescaling only) | Low accuracy; large gap between training and validation accuracy indicating overfitting |
| With Data Augmentation | Reduced train–validation gap; model generalises better |
| With Class Rebalancing | Improved accuracy; more balanced learning across minority classes |

The final model's accuracy remains moderate, reflecting the inherent difficulty of the classification task and the limited training data. Incorporating pre-trained architectures (e.g., EfficientNet, ResNet) via transfer learning is expected to yield substantial further improvement.

---

## References

- International Skin Imaging Collaboration (ISIC): https://www.isic-archive.com
- Esteva, A. et al. (2017). *Dermatologist-level classification of skin cancer with deep neural networks*. Nature, 542, 115–118.

---

## Contact

Created by [@chetnapriyadarshini](https://github.com/chetnapriyadarshini) — feel free to reach out with questions or suggestions.
