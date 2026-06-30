# Neural Ordinary Differential Equations (Neural ODEs)

## Overview
Neural ODEs represent a continuous-time generalization of residual networks. Instead of specifying a discrete sequence of hidden layers:
$$h_{t+1} = h_t + f(h_t, \theta_t)$$
Neural ODEs define the continuous state dynamics using an ODE solver:
$$\frac{dh(t)}{dt} = f(h(t), t, \theta)$$

## Key Benefits
- **O(1) memory cost:** Allows backpropagating through the ODE solver without storing intermediate activations.
- **Adaptive computation:** Solver adjusts step size dynamically based on the input complexity.

## Diagram
```mermaid
graph TD
    Input[Input h(0)] --> Solver[ODE Solver / Integrator]
    Solver --> Dynamics[d h(t) / dt = f(h(t), t, theta)]
    Dynamics --> Solver
    Solver --> Output[Output h(T)]
```

## References
- Chen, R. T. Q., Rubanova, Y., Bettencourt, J., & Duvenaud, D. (2018). Neural Ordinary Differential Equations. arXiv preprint arXiv:1806.07366.

[← Back to README](../README.md)
