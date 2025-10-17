# PPO from Scratch (PyTorch + Gym)

This repository contains a simple and clear implementation of the **Proximal Policy Optimization (PPO)** algorithm using **PyTorch** and **Gymnasium**.  
It trains a reinforcement learning agent to solve environments such as **CartPole-v1**.

---

## Features

- Full PPO implementation (Actor-Critic architecture)
- Generalized Advantage Estimation (GAE)
- Learning rate annealing
- Entropy regularization
- Gradient clipping
- TensorBoard logging
- Optional video capture (`videos/` folder)
- Optional tracking with **Weights & Biases**

---

## Requirements

Install the dependencies:

```bash
pip install torch gymnasium[box2d] numpy tensorboard wandb
