# CNN using PyTorch

## Overview
- **Convolutional Neural Networks**: Specialized architectures for processing grid-like data such as images.
- **Layers**: Composed of Convolutional layers (`nn.Conv2d`), Pooling layers (`nn.MaxPool2d`), and Fully Connected layers (`nn.Linear`).
- **Feature Extraction**: The convolutional base automatically learns spatial hierarchies of features, from simple edges to complex shapes.

## CNN Architecture
```mermaid
graph LR
    I[Input Image] --> C1[Conv2d + ReLU]
    C1 --> P1[MaxPool2d]
    P1 --> C2[Conv2d + ReLU]
    C2 --> P2[MaxPool2d]
    P2 --> F[Flatten]
    F --> FC1[Linear + ReLU]
    FC1 --> FC2[Linear (Output)]
```

## Recommended Resources
- [Convolutional Neural Networks Tutorial (PyTorch)](https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html) - Training a CNN on CIFAR10.
- [A Comprehensive Guide to CNNs with PyTorch](https://towardsdatascience.com/a-comprehensive-guide-to-convolutional-neural-networks-the-eli5-way-3bd2b1164a53) - Great theoretical and practical breakdown.
