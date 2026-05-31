# LSTM using PyTorch

## Overview
- **Long Short-Term Memory (LSTM)**: A specialized RNN architecture that uses "gates" to control the flow of information, solving the vanishing gradient problem.
- **Cell State & Hidden State**: LSTMs maintain two states across time steps. The cell state acts as a conveyor belt carrying long-term memory.
- **Gates**: Forget gate (what to discard), Input gate (what new info to store), and Output gate (what to output based on the cell state).

## LSTM Cell Structure
```mermaid
graph TD
    subgraph LSTM Cell
        F[Forget Gate]
        I[Input Gate]
        C_tilde[Candidate Cell State]
        O[Output Gate]
        
        C_prev((C_{t-1})) --> C_t((C_t))
        F -->|*| C_t
        I -->|*| C_t
        C_tilde -->|*| C_t
    end
    
    x_t --> F
    h_prev --> F
    
    C_t -->|tanh| O
    O -->|*| h_t
```

## Recommended Resources
- [Understanding LSTM Networks by Colah](https://colah.github.io/posts/2015-08-Understanding-LSTMs/) - The definitive blog post on understanding how LSTMs work.
- [Sequence Models and Long-Short Term Memory Networks](https://pytorch.org/tutorials/beginner/nlp/sequence_models_tutorial.html) - PyTorch LSTM documentation and tutorial.
