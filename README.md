# AI5100 Hackathon

**Note:** Unfortunately, the code used to generate the plots in this [presentation](https://github.com/dnshkmr7/ilsvrc-hackathon/blob/main/AI5100_%20Presentation.pdf) has been lost/deleted.

## Overview

This project focuses on multi-class classification, using a dataset containing 50 classes. The dataset is a subset of the ILSVRC dataset.

## Dataset

- Benchmarking image classification from 2016 to 2024.
- The task at hand is multi-class classification with 50 classes.

## Background

- We explored the best-performing models of ILSVRC.
- The two models considered were ResNet and Vision Transformer (ViT).
- Extensive research was conducted on ViT and ResNet codes.

## Research Process

1. **Starting with Vision Transformer (ViT):** 
   - Chosen as the best-performing state-of-the-art model.
2. **Fallback to ResNet50:**
   - If ViT doesn't work, ResNet was chosen as a more reliable model.

## Strategies and Attempts

### Vision Transformers (ViT)

- **Architecture:**
  - Patch size: 28
  - Dimensions: 1024
  - Depth: 8
  - Heads: 8
  - MLP Dimension: 2048
  - Dropout: 0.1
  - Embedding Dropout: 0.1
  - Dim head: 64
  - Batch size: 400
  - Learning rate: 0.0001
  - Epochs: 20

- **Results:**
  - Validation loss started at 3.04 and showed signs of overfitting, increasing to 3.34 by epoch 20.
  - Optimal hyperparameters were not achieved, leading to overfitting.

### Residual Networks (ResNet50)

- **Architecture:**
  - Batch size: 128
  - Learning rate: 0.01 (with LRScheduler and patience=3)
  - Epochs: 60
  - Patience: 3
  - Weight decay: 0.0001
  - Momentum: 0.9

- **Results:**
  - Validation loss improved, from 0.585 to 0.529 by the 30th epoch.
  - Accuracy improved to 84.2%, showing good learning and improved performance.

## Future Work

- Pre-training ResNet50 on the ImageNet dataset could improve generalization and performance.
- Trying out ResNet variants or other architectures like VGG could yield better results.
