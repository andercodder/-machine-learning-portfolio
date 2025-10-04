# Deep Reinforcement Learning for Sequential Optimization

**Course**: CS5079 – Applied Artificial Intelligence, University of Aberdeen (2025)

---

## 📋 Overview

This project implements a Deep Q-Network (DQN) agent to solve the FrozenLake environment, demonstrating reinforcement learning principles for sequential decision-making. The agent learns optimal navigation strategies through trial and error, balancing exploration and exploitation.

**Real-World Applications:**
- **Trading Strategies**: Sequential decision-making in financial markets
- **Portfolio Optimization**: Dynamic asset allocation
- **Resource Management**: Optimal scheduling and allocation
- **Autonomous Systems**: Navigation and path planning
- **Energy Trading**: Bid/offer strategies in volatile markets

---

## 🎯 Objectives

1. Implement Deep Q-Network (DQN) from scratch using PyTorch
2. Solve FrozenLake-v1 environment (10x10 grid, stochastic transitions)
3. Implement ε-greedy exploration strategy with decay
4. Use experience replay for stable learning
5. Employ target network for improved convergence
6. Analyze exploration-exploitation tradeoff

---

## 🎮 Environment: FrozenLake-v1

**Description**: Navigate a frozen lake from start (S) to goal (G) while avoiding holes (H).

**Characteristics:**
- **State Space**: 100 states (10x10 grid)
- **Action Space**: 4 discrete actions (LEFT, DOWN, RIGHT, UP)
- **Stochastic Dynamics**: Actions have probabilistic outcomes (slippery ice)
- **Sparse Rewards**: +1 for reaching goal, 0 otherwise
- **Episode Termination**: Reaching goal or falling in hole

**Challenges:**
- Large state space for tabular methods
- Stochastic transitions (intended action may not execute)
- Sparse reward signal (credit assignment problem)
- Exploration required to discover goal

---

## 🧠 Deep Q-Network (DQN) Architecture

### Neural Network Design

**Input**: One-hot encoded state (100 dimensions)  
**Hidden Layers**: Fully connected layers with ReLU activation  
**Output**: Q-values for each action (4 dimensions)

```
State (100) → FC Layer → ReLU → FC Layer → ReLU → Q-values (4)
```

### Key Components

#### 1. **Experience Replay**
- **Buffer Size**: Stores past experiences (state, action, reward, next_state, done)
- **Random Sampling**: Breaks correlation between consecutive samples
- **Batch Training**: Improves sample efficiency and stability

#### 2. **Target Network**
- **Fixed Q-targets**: Separate network for computing target Q-values
- **Periodic Updates**: Target network updated every N steps
- **Stability**: Reduces oscillations in training

#### 3. **ε-Greedy Exploration**
- **Initial ε**: 1.0 (pure exploration)
- **Final ε**: 0.1 (mostly exploitation)
- **Decay Strategy**: Linear or exponential decay
- **Balance**: Explores early, exploits learned policy later

---

## 🔧 Implementation Details

### Hyperparameters

| Parameter | Value | Purpose |
|-----------|-------|---------|
| Learning Rate | 0.001 | Neural network optimization |
| Discount Factor (γ) | 0.99 | Future reward importance |
| Batch Size | 64 | Training batch size |
| Replay Buffer | 10,000 | Experience storage capacity |
| Target Update | 100 steps | Target network sync frequency |
| ε Decay | 1.0 → 0.1 | Exploration schedule |

### Training Process

1. **Initialize**: Create Q-network and target network
2. **Interact**: Agent takes actions in environment
3. **Store**: Save experiences in replay buffer
4. **Sample**: Random batch from replay buffer
5. **Compute**: Calculate Q-targets using target network
6. **Update**: Train Q-network via gradient descent
7. **Sync**: Periodically update target network
8. **Decay**: Reduce ε over time

---

## 📈 Key Results

### Learning Performance
- **Convergence**: Agent learns successful navigation strategy
- **Success Rate**: Improved significantly over training episodes
- **Exploration**: ε-decay enables transition from exploration to exploitation
- **Stability**: Experience replay and target network prevent catastrophic forgetting

### Insights

1. **Experience replay** is crucial for stable learning in RL
2. **Target networks** reduce Q-value overestimation
3. **ε-greedy strategy** effectively balances exploration/exploitation
4. **Stochastic environments** require robust policies
5. **Neural networks** enable generalization across states

### Visualizations
- Training reward curves
- Success rate over episodes
- ε-decay schedule
- Q-value evolution
- Agent behavior videos

---

## 🛠️ Technologies Used

**Core Libraries:**
- **PyTorch**: Neural network implementation
- **OpenAI Gym**: RL environment interface
- **NumPy**: Numerical computations
- **Matplotlib**: Training visualization

**Key Algorithms:**
- Deep Q-Network (DQN)
- Experience Replay
- Target Network
- ε-Greedy Exploration

---

## 📁 Project Structure

```
03_Reinforcement_Learning_Optimization/
├── README.md
├── dqn_frozenlake.ipynb           # Complete DQN implementation
├── requirements.txt               # Python dependencies
├── images/                        # Training curves and results
└── dqn_frozenlake.pth            # Trained model weights
```

---

## 💡 Key Takeaways

### Reinforcement Learning Principles
1. **Trial and error**: Agent learns from interaction, not labeled data
2. **Delayed rewards**: Credit assignment across multiple time steps
3. **Exploration-exploitation**: Balance discovering new strategies vs. using known good ones
4. **Function approximation**: Neural networks enable scaling to large state spaces

### Production Considerations
1. **Hyperparameter sensitivity**: Careful tuning required for convergence
2. **Sample efficiency**: Experience replay improves data utilization
3. **Stability**: Target networks and replay buffer prevent divergence
4. **Deployment**: Trained policy can be deployed for real-time decision-making

---

## 🔮 Future Enhancements

### Algorithm Improvements
- **Double DQN**: Reduce Q-value overestimation
- **Dueling DQN**: Separate value and advantage functions
- **Prioritized Experience Replay**: Sample important transitions more frequently
- **Rainbow DQN**: Combine multiple DQN improvements

### Advanced Applications
- **Continuous Action Spaces**: Extend to DDPG, TD3, SAC
- **Multi-Agent RL**: Competitive/cooperative scenarios
- **Hierarchical RL**: Learn sub-policies for complex tasks
- **Transfer Learning**: Adapt learned policies to new environments

### Real-World Deployment
- **Trading Bots**: Apply to financial market decision-making
- **Resource Allocation**: Dynamic scheduling and optimization
- **Robotics**: Physical navigation and manipulation
- **Energy Management**: Optimal control of energy systems

---

## 🌍 Industry Relevance

This project demonstrates skills valuable for:

✅ **Sequential Decision-Making**: Core skill for trading and optimization  
✅ **Uncertainty Handling**: Stochastic environments mirror real-world complexity  
✅ **Neural Networks**: Deep learning for function approximation  
✅ **Algorithm Implementation**: Building RL systems from scratch  
✅ **Experimentation**: Systematic hyperparameter tuning and evaluation

---

## 📚 References

- Mnih, V., et al. (2015). Human-level control through deep reinforcement learning. Nature
- Sutton, R. S., & Barto, A. G. (2018). Reinforcement Learning: An Introduction
- Van Hasselt, H., et al. (2016). Deep Reinforcement Learning with Double Q-learning

---

## 📝 Academic Context

This project was completed as part of CS5079 (Applied Artificial Intelligence) coursework at the University of Aberdeen, demonstrating advanced reinforcement learning techniques and neural network implementation.

---

[← Back to Portfolio](../README.md)
