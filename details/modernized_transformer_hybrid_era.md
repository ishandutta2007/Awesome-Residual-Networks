# The Modernized Transformer-Hybrid Era (~2022–Present)

## Overview
With Vision Transformers (ViTs) showing superior scalability, researchers proposed modernizing convolutional networks to match them. ConvNeXt is a prime example of a modernized CNN that retains the simplicity of ResNets while adopting Transformer-style design choices.

## Modernization Steps
- Swapping standard bottleneck ratios for inverted bottlenecks.
- Expanding kernel sizes (from $3 \times 3$ to $7 \times 7$).
- Using Layer Normalization instead of Batch Normalization.
- Using GELU instead of ReLU.

## Diagram
```mermaid
graph TD
    Input[Input x] --> Conv[7x7 Depthwise Conv]
    Conv --> LN[Layer Norm]
    LN --> Linear1[1x1 Conv / Linear 1]
    Linear1 --> GELU[GELU]
    GELU --> Linear2[1x1 Conv / Linear 2]
    Input -->|Identity Shortcut| Add((+))
    Linear2 --> Add
    Add --> Output[Output]
```

## References
- Liu, Z., Mao, H., Wu, C. Y., Feichtenhofer, C., Darrell, T., & Xie, S. (2022). A ConvNet for the 2020s. arXiv preprint arXiv:2201.03545.

[← Back to README](../README.md)
