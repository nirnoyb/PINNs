This project implements a Physics-Informed Neural Network (PINN) to solve the steady-state 2D heat conduction equation without relying on labeled temperature data.
The network learns the underlying physics directly from the governing partial differential equation (PDE) and boundary conditions.

The goal is to solve the Laplace equation:
∇2T(x,y)=0
subject to fixed boundary temperatures.
Instead of using numerical solvers like Finite Difference Method (FDM), this project uses a neural network trained to satisfy the PDE across the spatial domain.

1. Network Architecture
Fully-connected feedforward neural network (PINN)
Activation: tanh
Weight initialization: Xavier Normal
Input: spatial coordinates (x, y)
Output: temperature 
𝑇
(
𝑥
,
𝑦
)
T(x,y)

2. Training Objective
The total loss combines:
PDE loss: ensures ∇²T ≈ 0 inside the domain
Boundary loss: enforces known temperature conditions along the boundaries
$$
\text{Loss}_{total} = \text{MSE}_{PDE} + \text{MSE}_{BC}
$$

3. Sampling
Interior points → random samples within the domain
Boundary points → evenly spaced samples along edges

After training, the model predicts a smooth temperature distribution that satisfies the boundary conditions and Laplace’s equation.
Typical output:
Contour plot of predicted temperature
Training loss vs. iterations

Nirnoy Barma
Chemical Engineering Student, Jadavpur University
