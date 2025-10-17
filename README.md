# PPO from Scratch (PyTorch + Gym) 

[![Python](https://img.shields.io/badge/python-3.9%2B-blue)](https://www.python.org/) 
[![PyTorch](https://img.shields.io/badge/pytorch-1.13-red)](https://pytorch.org/) 
[![Gymnasium](https://img.shields.io/badge/gymnasium-0.29-green)](https://gymnasium.farama.org/) 
[![TensorBoard](https://img.shields.io/badge/tensorboard-enabled-orange)](https://www.tensorflow.org/tensorboard) 
[![Weights & Biases](https://img.shields.io/badge/wandb-optional-yellow)](https://wandb.ai/)

A **simple and clear implementation** of **Proximal Policy Optimization (PPO)** using **PyTorch** and **Gymnasium**.  
Trains an RL agent to solve environments like **CartPole-v1**.

---

## Features 

- Actor-Critic PPO implementation  
- Generalized Advantage Estimation (GAE)  
- Learning rate annealing  
- Entropy regularization  
- Gradient clipping  
- TensorBoard logging  
- Optional video capture (`videos/`)  
- Optional tracking with **Weights & Biases**

---

## Requirements 

Install dependencies:

```bash
pip install torch gymnasium[box2d] numpy tensorboard wandb
Usage 
<details> <summary>Run Training</summary>
Run with default parameters:

bash
Copier le code
python ppo.py
Customize training:

bash
Copier le code
python ppo.py \
  --gym-id CartPole-v1 \
  --total-timesteps 50000 \
  --num-envs 4 \
  --learning-rate 3e-4 \
  --capture-video True
</details> <details> <summary>Logging & Monitoring</summary>
TensorBoard:

bash
Copier le code
tensorboard --logdir runs
Weights & Biases (Optional):

bash
Copier le code
python ppo.py --track True --wandb-project-name ppo-implementation-details
</details> <details> <summary>Video Recording</summary>
Record the agent’s performance:

bash
Copier le code
python ppo.py --capture-video True
Videos will be saved in the videos/ directory.

</details>
📁 Project Structure
graphql
Copier le code
.
├── ppo.py      # Main PPO training script
├── runs/       # TensorBoard logs
└── videos/     # (optional) Recorded videos
About PPO 
Proximal Policy Optimization (PPO) is a policy gradient algorithm designed for stable and efficient reinforcement learning.
It prevents large policy updates using a clipping function in the objective function.

Key Concepts:

Clipped surrogate objective

Actor-Critic structure

Generalized Advantage Estimation (GAE)

Value function clipping


Developed by Aya Fitouri
Based on PPO principles for learning reinforcement learning fundamentals.