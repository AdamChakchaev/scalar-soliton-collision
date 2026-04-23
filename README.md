# 3D Scalar Soliton Collision Simulation

This repository contains the numerical simulation code accompanying the paper **"Unitary Black Hole Evolution from Kinetically Regularized Singularities"** by Adam Chakchaev.

## Overview
The provided Python script performs a 3D numerical evolution of a scalar field to simulate the dynamical collision of highly concentrated scalar solitons. Specifically, it implements the kinetic ultraviolet (UV) regularization scheme utilizing the modulation factor $Z(p)=(1+\beta p^{2})^{-1}$. 

As discussed in Section VIII.B of the paper, this kinetic modulation dampens steep kinetic gradients and activates a dynamical freeze-out that bounds the maximum amplitude of the field, preventing target-space singularities during strong-field interactions.

## Numerical Setup
The simulation is evolved on a 3D spatial grid ($N=200^3$ points) in a flat Minkowski background. The numerical scheme relies on:
* **Time Integration:** 4th-order Runge-Kutta (RK4) method.
* **Spatial Derivatives:** 4th-order finite differences.
* **Boundary Conditions:** Sommerfeld absorbing boundaries.
* **Physical Parameters:** $\mu=0.5$, $\lambda_c=0.01$, and $\beta=0.05$.

## Output
Running the script directly reproduces **Figure 4** from the manuscript. It generates a multi-panel plot showing the equatorial slice ($z=0$) of the collision, highlighting the iso-amplitude contours and the local kinetic gradients ($\nabla p$) during the initial, merger, and oscillation phases.
