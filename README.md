# Iris Recognition with Triplet Loss

## Description

This project implements an iris-recognition system using a deep embedding network trained with triplet loss. We use **EfficientNet-B0** (adapted for single-channel iris images) to extract **128-dimensional embeddings**, and train with a margin-based triplet loss. After training, we sweep a distance threshold for verification and report accuracy and ROC-AUC.

---

## Approach

- **Backbone:** EfficientNet-B0 modified for single-channel input  
- **Embedding size:** 128  
- **Loss:** Margin-based triplet loss  

The triplet loss enforces the following constraint:  
d(anchor, positive) + margin < d(anchor, negative)

## Training

- **Epochs:** 20
- **Batch size:** 32
- **Margin:** 1.0
- **Optimizer:** Adam (learning rate = 1e-4)

## Results
- **Verification accuracy:** 0.813 at threshold 0.2474
- **ROC-AUC:** 0.894

