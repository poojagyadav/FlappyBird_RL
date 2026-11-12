
# FlappyBird RL - Deep Q-Network (DQN)

A Reinforcement Learning project that trains an AI agent to play Flappy Bird using **Deep Q-Network (DQN)**.

The agent learns through trial and error by observing game states, taking actions, and receiving rewards.

## Features

- Deep Q-Network (DQN) implementation.
- Experience Replay for stable learning.
- Epsilon-greedy action selection.
- Automated training and testing.
- Configurable training parameters.

## Tech Stack

- **Python** – Main programming language.
- **PyTorch** – Used to build and train the Deep Q-Network, predict Q-values, calculate training loss, and update neural network weights through backpropagation.
- **Gymnasium** – Provides the reinforcement learning environment interface.
- **Flappy Bird Gymnasium** – Provides the Flappy Bird game environment.
- **NumPy** – Numerical computations.
- **PyYAML** – Managing training configurations.

## 📁 Project Structure

```text
FlappyBird_RL/
│
├── runs/                  # Generated automatically during training
├── agent.py               # Agent and execution
├── dqn.py                 # DQN model
├── experience_replay.py   # Replay memory
├── game_flappy_bird.py    # Game environment
├── parameters.yaml        # Training parameters
├── .gitignore
└── README.md
```

**Note:** The `runs/` folder is automatically created when training starts. It stores training logs and experiment outputs.

## ⚙️ Installation

Install the required dependencies:

```bash
pip install torch numpy pyyaml gymnasium flappy-bird-gymnasium
```

## ▶️ Run the Project

### 1. Training

Run the following command to train the AI agent:

```bash
python agent.py flappybirdv0 --train
```

The agent learns to play Flappy Bird, and the `runs/` folder is generated automatically.

### 2. Testing

After training, run the following command:

```bash
python agent.py flappybirdv0
```

The agent uses the trained model to play the game.

**Note:** Training must be completed before testing to ensure a trained model is available.

## Environment

This project uses the [Flappy Bird Gymnasium](https://github.com/markub3327/flappy-bird-gymnasium) environment.

### Available Actions

| Action | Description |
|:---:|---|
| 0 | Do nothing |
| 1 | Flap |

### Reward System

| Event | Reward |
|---|:---:|
| Staying alive | +0.1 |
| Successfully passing a pipe | +1.0 |
| Dying | -1.0 |
| Touching the top of the screen | -0.5 |

## Conclusion

This project was developed as a **learning initiative to understand Deep Reinforcement Learning and the working of Deep Q-Networks (DQN)**.

Through this project, I explored how an AI agent learns through trial and error, uses rewards and penalties to make decisions, and gradually improves its performance.

It provided hands-on experience with PyTorch, Gymnasium, neural networks, Experience Replay, and reinforcement learning concepts.

**The main goal of this project was to gain practical knowledge and build a better understanding of how Reinforcement Learning works.**

---

**Project:** FlappyBird RL  
**Purpose:** Learning and Exploring Reinforcement Learning  
**Algorithm:** Deep Q-Network (DQN)  
**Domain:** Deep Learning & Reinforcement Learning
