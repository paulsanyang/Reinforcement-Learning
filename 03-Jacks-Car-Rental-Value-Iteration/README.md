
# Jack's Car Rental — Value Iteration

## Overview

This project implements synchronous value iteration to solve
Jack's Car Rental, a classical reinforcement learning problem
formulated as a finite Markov Decision Process (MDP).

The objective is to determine an optimal overnight car transfer
policy between two rental locations that maximizes the expected
discounted revenue while accounting for rental demand, vehicle
returns, transfer costs, and inventory constraints.

## Problem Configuration

| Parameter | Location A | Location B |
|---|---:|---:|
| Maximum capacity | 20 | 20 |
| Mean rental requests | 3 | 4 |
| Mean car returns | 3 | 2 |

- Rental reward: 10 dollars per car
- Transfer cost: 2 dollars per car
- Maximum overnight transfers: 5 cars
- Discount factor: 0.9
- State space: 441 states
- Convergence tolerance: 0.01

Rental requests and returns are modelled as independent
Poisson random variables.


## Mathematical Framework

The problem is solved using the Bellman optimality equation:

```math
V^{*}(s)=\max_{a\in\mathcal{A}(s)}
\left[
r(s,a)+\gamma\sum_{s'}P(s'\mid s,a)V^{*}(s')
\right].
```

The independence of the two rental locations allows the
expected continuation values to be computed efficiently
through matrix multiplication:

```math
H=P_A V P_B^{\top}.
```

Convergence is monitored using the supremum norm:

```math
\delta_k=\lVert V_{k+1}-V_k\rVert_{\infty}.
```

Detailed mathematical derivations are provided in the notebook.

## Implementation

The implementation includes:

- Synchronous value iteration implemented from scratch.
- Exact inventory-capped Poisson distributions.
- Precomputed transition probabilities and expected rewards.
- Vectorized Bellman updates.
- Inventory and transfer capacity constraints.
- Separate environment and solver classes.
- Intermediate greedy policy matrices.
- Convergence monitoring and Bellman residual analysis.
- Numerical validation of transition probabilities and policies.

## Results and Visualizations

The notebook provides:

- Intermediate policy matrices every 10 iterations.
- A heatmap of the final greedy policy.
- A logarithmic convergence plot of the value function.
- Numerical convergence diagnostics.

Positive policy values represent transfers from location A
to location B, while negative values represent transfers
in the opposite direction.

## Dependencies

- Python
- NumPy
- SciPy
- Matplotlib
- Jupyter Notebook

Install the required packages:

```bash
pip install numpy scipy matplotlib notebook
```

## Usage

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open `jacks_car_rental_value_iteration.ipynb` and run all cells.
[Open](jacks_car_rental_value_iteration.ipynb)

The environment parameters and convergence tolerance can be
modified to investigate alternative problem configurations.

## Reference

Sutton, R. S., and Barto, A. G. (2018).
*Reinforcement Learning: An Introduction*, 2nd Edition.
MIT Press. Chapter 4, Dynamic Programming.

## Author

Paul Sanyang

[Academic Website](https://paulsanyang.github.io) |
[GitHub](https://github.com/paulsanyang)
