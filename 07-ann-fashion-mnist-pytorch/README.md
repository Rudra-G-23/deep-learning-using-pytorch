# ANN Fashion MNIST with PyTorch

## Overview
- **Artificial Neural Networks (ANN)**: Building a Multi-Layer Perceptron (MLP) for image classification.
- **Fashion MNIST**: A dataset of Zalando's article images consisting of a training set of 60,000 examples and a test set of 10,000 examples, formatted as 28x28 grayscale images.
- **Flattening**: The 2D images must be flattened into 1D vectors before being passed through the linear layers of the ANN.

## MLP Architecture
```mermaid
graph TD
    I[Input Image 28x28] --> F[Flatten Layer 784]
    F --> H1[Hidden Layer 1 (ReLU)]
    H1 --> H2[Hidden Layer 2 (ReLU)]
    H2 --> O[Output Layer 10 (Logits)]
    O --> P[CrossEntropyLoss]
```

## Recommended Resources
- [Fashion MNIST Dataset Docs](https://pytorch.org/vision/stable/generated/torchvision.datasets.FashionMNIST.html) - PyTorch Vision dataset documentation.
- [Building an Image Classifier using PyTorch](https://www.analyticsvidhya.com/blog/2019/10/building-image-classification-models-cnn-pytorch/) - Practical tutorial.
