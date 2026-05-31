# Transfer Learning (VGG16)

## Overview
- **Transfer Learning**: Utilizing a model trained on a large dataset (like ImageNet) for a different but related task to save time and compute.
- **VGG16**: A classic deep CNN architecture available in `torchvision.models`.
- **Fine-Tuning vs Feature Extraction**:
  - *Feature Extraction*: Freeze all base layers, only train the final classification head.
  - *Fine-Tuning*: Unfreeze the entire network and train with a very small learning rate.

## Transfer Learning Process
```mermaid
graph TD
    subgraph Pre-trained VGG16
        CL[Conv Layers 1 to 13]
        FC[Original FC Layers]
    end
    
    subgraph Custom Model
        CL_F[Frozen Conv Layers 1 to 13]
        FC_N[New FC Layer: e.g. 10 classes]
    end
    
    CL -.-> CL_F
    CL_F --> FC_N
    
    style CL_F fill:#ddd,stroke:#333,stroke-dasharray: 5 5
    style FC_N fill:#bbf,stroke:#333
```

## Recommended Resources
- [Transfer Learning for Computer Vision Tutorial](https://pytorch.org/tutorials/beginner/transfer_learning_tutorial.html) - Official PyTorch tutorial on transfer learning.
- [VGG16 Architecture Explained](https://neurohive.io/en/popular-networks/vgg16/) - Detailed look at the VGG16 network.
