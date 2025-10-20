<h1>Title: Physics-Informed Neural Network for 2D Steady-State Heat Conduction</h1>h1>


<h2>This project implements a Physics-Informed Neural Network (PINN) to solve the steady-state 2D heat conduction equation without relying on labeled temperature data.
The network learns the underlying physics directly from the governing partial differential equation (PDE) and boundary conditions.</h2>

The goal is to solve the Laplace equation:

∇2T(x,y)=0

subject to fixed boundary temperatures.

Instead of using numerical solvers like Finite Difference Method (FDM), this project uses a neural network trained to satisfy the PDE across the spatial domain.

1. Network Architecture
Fully-connected feedforward neural network (PINN)

Activation: tanh

Weight initialization: Xavier Normal

Input: spatial coordinates (x, y)

Output: temperature T(x,y)


3. Training Objective
   
The total loss combines:

PDE loss: ensures ∇²T ≈ 0 inside the domain

Boundary loss: enforces known temperature conditions along the boundaries

Total Loss=MSE(PDE) ​+ MSE(BC)​

4. Sampling
   
Interior points → random samples within the domain

Boundary points → evenly spaced samples along edges

After training, the model predicts a smooth temperature distribution that satisfies the boundary conditions and Laplace’s equation.

Typical output:

Contour plot of predicted temperature

Training loss vs. iterations

Nirnoy Barma

Chemical Engineering Student, Jadavpur University
