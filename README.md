# Vivek_Foundations-of-AI-code-for-the-Final-Report

This repository contains the implementation of the Q-learning algorithm applied to the FrozenLake environment as part of the CS5100 Foundations of Artificial Intelligence capstone project.

The project demonstrates how a reinforcement learning agent learns an optimal policy through interaction with a stochastic environment using trial-and-error and reward feedback.

## Overview

The implementation uses tabular Q-learning to train an agent to navigate the FrozenLake grid. The agent learns to reach the goal state while avoiding holes, using an epsilon-greedy exploration strategy.


## Code Structure Explanation

### 1. Import Libraries
The required libraries such as NumPy, Gymnasium, and Matplotlib are imported. These are used for numerical computation, environment simulation, and visualization.


### 2. Environment Setup
The FrozenLake environment is initialized with stochastic transitions (`is_slippery=True`). The number of states and actions are extracted to define the Q-table.


### 3. Q-table Initialization
A Q-table is created and initialized with zeros. This represents the agent's initial knowledge, where all state-action values are unknown.


### 4. Hyperparameters
Key parameters are defined:
- Learning rate (α): controls how quickly values are updated  
- Discount factor (γ): determines importance of future rewards  
- Epsilon (ε): controls exploration vs exploitation  


### 5. Training Loop
The agent is trained over multiple episodes:
- Actions are selected using an epsilon-greedy strategy  
- The environment returns the next state and reward  
- The Q-table is updated using the Q-learning update rule  


### 6. Exploration Decay
The exploration rate (ε) decreases over time, allowing the agent to explore initially and exploit learned knowledge later.


### 7. Performance Tracking
Two metrics are tracked:
- Reward per episode  
- Success rate (whether the goal was reached)


### 8. Visualization
Graphs are generated to show:
- Reward vs Episodes  
- Success Rate vs Episodes  

These help analyze learning progression and convergence behavior.


### 9. Testing Phase
After training, the agent is tested without exploration (pure exploitation) to evaluate performance over multiple episodes.


### 10. Final Outputs
The final Q-table and learned policy are printed. The policy shows the best action to take in each state.


## 11. Results

The agent demonstrates improved performance over time, with increasing reward and success rate, indicating convergence toward an effective policy.


