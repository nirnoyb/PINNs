This project implements a Physics-Informed Neural Network (PINN) to solve the steady-state 2D heat conduction equation without relying on labeled temperature data.
The network learns the underlying physics directly from the governing partial differential equation (PDE) and boundary conditions.

The goal is to solve the Laplace equation:

∇
2
𝑇
(
𝑥
,
𝑦
)
=
0
∇
2
T(x,y)=0

subject to fixed boundary temperatures.
Instead of using numerical solvers like Finite Difference Method (FDM), this project uses a neural network trained to satisfy the PDE across the spatial domain
