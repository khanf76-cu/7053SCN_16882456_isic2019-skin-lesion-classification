# 7053SCN ISIC 2019 Skin Lesion Classification 

# 7053SCN ISIC 2019 Skin Lesion Classification

## Overview
A stacked ensemble deep learning pipeline for multi-class skin lesion classification
using the ISIC 2019 dataset. The pipeline progresses through multiple model architectures,
culminating in a stacked MLP meta-learner ensemble achieving a final test balanced
accuracy of **0.9079** and macro F1 of **0.8399**.

## Models and Performance

| Block | Model | Balanced Accuracy |
|-------|-------|-------------------|
| Block 2 | ResNet50 Baseline | 0.6531 |
| Block 3D | EfficientNet-B4 | 0.7408 |
| Block 4 | ViT-B/16 | 0.8258 |
| Block 5 | PatchLSTM | — |
| Block 6 | Stacked MLP Ensemble | **0.9079** |

## Dataset
This project uses the ISIC 2019 Skin Lesion Classification dataset containing
25,331 dermoscopic images across 8 diagnostic categories:

- MEL — Melanoma
- NV — Melanocytic Nevus
- BCC — Basal Cell Carcinoma
- AK — Actinic Keratosis
- BKL — Benign Keratosis
- DF — Dermatofibroma
- VASC — Vascular Lesion
- SCC — Squamous Cell Carcinoma

Download from:
https://www.kaggle.com/datasets/salviohexia/isic-2019-skin-lesion-images-for-classification

## Requirements
```txt
Python 3.8+
PyTorch
torchvision
timm
scikit-learn
numpy
matplotlib
seaborn
tensorboard
