# The Deep Degradation Era (Plain VGG Style, Pre-2015)

## Overview
Before the introduction of residual networks, convolutional neural networks (like VGG) were scaled up simply by stacking layers sequentially. This era faced a fundamental limitation: stacking layers beyond ~20 resulted in higher training and testing error, a phenomenon known as degradation.

## The Degradation Problem
As the network depth increases, accuracy saturates and then degrades rapidly. This is not caused by overfitting, as training error increases as well. It is largely due to the vanishing/exploding gradients which hamper convergence from the beginning.

## Diagram
Below is a diagram illustrating the sequential stacking of layers in plain networks compared to residual learning:

```mermaid
graph TD
    Input[Input x] --> Layer1[Weight Layer 1]
    Layer1 --> Activation1[ReLU]
    Activation1 --> Layer2[Weight Layer 2]
    Layer2 --> Output[Output H(x)]
```

## References
- Simonyan, K., & Zisserman, A. (2014). Very Deep Convolutional Networks for Large-Scale Image Recognition. arXiv preprint arXiv:1409.1556.

[← Back to README](../README.md)
