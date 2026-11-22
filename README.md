# Reinforcement Learning

## Overview

This repository contains a collection of computational projects exploring fundamental concepts and algorithms in **Reinforcement Learning (RL)**. The projects combine mathematical formulations, stochastic modeling, numerical simulations, and algorithmic implementations to investigate sequential decision-making under uncertainty.

Using **Python and R**, the implementations examine exploration–exploitation strategies, Markov decision processes, Monte Carlo methods, importance sampling, and dynamic programming techniques for optimal policy computation.

Each project includes mathematical explanations, implementation details, and computational results.

## Projects

### 1. Multi-Armed Bandits and Markov Chains

**Language:** R | **Environment:** RStudio, R Markdown

This project investigates the exploration–exploitation trade-off through the \(k\)-armed bandit problem and examines the long-run behavior of discrete-time Markov chains.

**Key topics:**
- Implementation of the \(\epsilon\)-greedy action-selection algorithm.
- Simulation of 10-armed bandits across 2,000 independent runs.
- Comparison of exploration probabilities ε = 0, 0.01, 0.1.
- Analysis of average rewards and optimal action selection.
- Simulation of a three-state Markov chain and computation of its stationary distribution.

[View Project 1](01-Multi-Armed-Bandits-and-Markov-Chains%20Simulations/)

### 2. Markov Decision Processes, Monte Carlo Methods, and Importance Sampling

**Language:** Python | **Environment:** Jupyter Notebook

This project explores mathematical and computational methods for evaluating policies, estimating value functions, and making optimal decisions in stochastic environments.

**Key topics:**
- Markov Decision Processes and optimal decision-making.
- Iterative computation of value functions and policies.
- Monte Carlo estimation using sampled returns.
- Policy improvement and exploration.
- Importance sampling for estimating expectations under alternative probability distributions.

[View Project 2](02-MDP-Monte-Carlo-and-Importance-Sampling/)

### 3. Jack's Car Rental: Value Iteration and Optimal Policy Computation

**Language:** Python | **Environment:** Jupyter Notebook

This project investigates Jack's Car Rental Problem, a classical reinforcement learning problem involving inventory management and sequential decision-making under uncertainty.

The objective is to determine an optimal policy for transferring cars between two rental locations to maximize expected long-term rewards.

**Key topics:**
- Modeling rental requests and returns using Poisson distributions.
- Formulation of a Markov Decision Process.
- Expected reward computation.
- Implementation of value iteration.
- Computation of policies for transferring cars between rental locations.

[View Project 3](03-Jacks-Car-Rental-Value-Iteration/)

## Tools and Technologies

- **Programming:** Python, R
- **Development environments:** Jupyter Notebook, RStudio
- **Scientific computing:** NumPy, SciPy
- **Documentation:** Markdown, R Markdown, LaTeX
- **Version control:** Git and GitHub

## References

Sutton, R. S., & Barto, A. G. (2018). *Reinforcement Learning: An Introduction* (2nd ed.). MIT Press.

## Author

**Paul Sanyang**

Background in Mathematics, Probability Theory, and Machine Learning.

Research interests include stochastic processes, reinforcement learning, mathematical modeling, and machine learning.
