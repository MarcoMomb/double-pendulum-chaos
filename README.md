# Double Pendulum Chaos Study

## Overview
This project explores the **chaotic behavior of a double pendulum**, demonstrating how two nearly identical initial conditions diverge over time. Through numerical simulation and visualization, the project highlights the **sensitivity to initial conditions**, a hallmark of chaotic systems.

The notebook provides:  
- Visualization of **double pendulum motion** with rods, bobs, and angular velocity arrows.  
- **Phase space trajectories** (θ vs ω) with time-gradient coloring.  
- **Poincaré sections** for 2D slices of the 4D phase space (θ₂ vs ω₂ at θ₁ = 0).  
- **Lyapunov exponent estimation** to quantify chaos.  
- Comparison of numerical solvers (`odeint` vs `solve_ivp`) with respect to energy conservation.

## Features

### Initial Conditions Visualization
- Two sets of initial conditions are plotted with rods, bobs, and angular velocity arrows.  
- Provides intuitive understanding of starting positions and velocities.

### Solver Comparison
- Compares `odeint` (fixed-step) and `solve_ivp` (adaptive-step) solvers.  
- Plots **total mechanical energy** and **deviation from mean** to choose a reliable solver for long simulations.

### Chaotic Motion Animation
- Animates two double pendulums with slightly different initial conditions.  
- Fading trails highlight the divergence of trajectories over time.  
- Implemented with `matplotlib.animation.FuncAnimation`.

### Phase Space Trajectories
- θ vs ω plots for each mass, showing the evolution of the system.  
- Time-gradient coloring illustrates the progression of motion.  
- Demonstrates how nearby initial conditions lead to rapidly diverging paths.

### Poincaré Section
- Samples the 4D phase space at θ₁ = 0 (upwards crossing) to create a 2D slice (θ₂ vs ω₂).  
- Scatter plots with time-gradient coloring visualize chaotic divergence.  
- Initial points are highlighted to show the start of trajectories.

### Lyapunov Exponent Estimation
- Calculates **normalized phase-space distance** Δ(t) between two trajectories.  
- Smooths Δ(t) to reduce noise and automatically selects the **exponential growth region**.  
- Linear fit of log Δ(t) gives the **largest Lyapunov exponent (λ)**, quantitatively measuring chaos.

## Installation

Requires Python ≥ 3.8 and the following packages:

pip install numpy matplotlib scipy ipython
