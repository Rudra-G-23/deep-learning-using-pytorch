# RNN using PyTorch

## Overview
- **Recurrent Neural Networks**: Designed to process sequential data (time series, text) by maintaining a hidden state that captures information from previous time steps.
- **`nn.RNN`**: PyTorch provides the base RNN module, taking inputs shaped `(sequence_length, batch_size, input_size)`.
- **Vanishing Gradients**: Standard RNNs struggle with long sequences due to vanishing or exploding gradients.

## Unrolled RNN Architecture
```mermaid
graph LR
    X0[x_0] --> H0((h_0))
    X1[x_1] --> H1((h_1))
    X2[x_2] --> H2((h_2))
    
    H_init((h_init)) --> H0
    H0 --> H1
    H1 --> H2
    
    H0 --> Y0[y_0]
    H1 --> Y1[y_1]
    H2 --> Y2[y_2]
```

## Recommended Resources
- [NLP From Scratch: Classifying Names with a Character-Level RNN](https://pytorch.org/tutorials/intermediate/char_rnn_classification_tutorial.html) - PyTorch intermediate tutorial.
- [Understanding Recurrent Neural Networks](https://towardsdatascience.com/understanding-rnn-and-lstm-f7cdf6dfc14e) - High-level conceptual overview.
