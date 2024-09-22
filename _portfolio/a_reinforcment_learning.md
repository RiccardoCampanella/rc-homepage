---

title: "(RL) Exploration of Reinforcement Learning Algorithms"
excerpt: "Implementing Epsilon-Greedy, Semi-Grad SARSA, and Q-Learning for solving multi-armed bandit and episodic MDP tasks"
tags: [ReinforcementLearning, EpsilonGreedy, SemiGradientSARSA, QLearning, MultiArmedBandit, FunctionApproximation, OnPolicy, OffPolicy, ExplorationExploitation, OpenAIGym]
collection: portfolio

---

## Project Overview

This project focuses on implementing and comparing reinforcement learning (RL) algorithms. Specifically, it explores solving multi-armed bandit problems using an epsilon-greedy algorithm and designing agents for episodic MDP tasks using Semi-gradient SARSA and Q-learning with function approximation. 

### Part 1: Multi-Armed Bandit Problem (Epsilon-Greedy Algorithm)

The multi-armed bandit problem is a classic RL challenge where an agent must choose between multiple options (bandits) to maximize rewards while balancing exploration and exploitation. The epsilon-greedy algorithm is employed here to find the optimal action.

#### Key Components

1. **Problem Setup**:
   - A k-armed bandit problem is modeled based on the OpenAI Gym framework.
   - The goal is to maximize rewards by selecting the best arm, balancing exploration (trying different actions) and exploitation (choosing the known best action).

2. **Epsilon-Greedy Algorithm**:
   - Implemented to explore the balance between exploration and exploitation.
   - Hyperparameter tuning: Exploration is controlled by the epsilon parameter, which is varied to find the optimal setting.

#### Table: Exploration vs Exploitation in Epsilon-Greedy

| Parameter       | Role            | Impact on Performance          |
|-----------------|-----------------|--------------------------------|
| Epsilon (ε)     | Exploration Rate| Higher values encourage exploration, lower values lead to exploitation. |
| Reward Function | Decision Metric | Measures the success of selected actions. |
| Action Selection| Optimal Choice  | A balance between random and reward-maximizing actions. |

---

### Part 2: Reinforcement Learning with Function Approximation (Semi-Grad SARSA & Q-Learning)

The second part of the project involves designing agents to complete an episodic MDP task. The agent navigates a maze and must learn to find a goal at the center by choosing one of four possible actions: moving left, right, up, or down. 

#### Key Components

1. **Problem Setup**:
   - An agent is trained to navigate using an OpenAI Gym environment.
   - The agent must learn to reach the goal as quickly as possible using function approximation.

2. **Algorithms**:
   - **Semi-Gradient SARSA**: An on-policy RL method where the agent learns the action-value function by directly interacting with the environment.
   - **Q-Learning**: An off-policy RL method where the agent learns the optimal action-value function by considering future actions.

#### Comparison of SARSA vs Q-Learning

| Aspect                  | Semi-Grad SARSA                         | Q-Learning                         |
|-------------------------|-----------------------------------------|------------------------------------|
| Policy                   | On-policy                              | Off-policy                        |
| Update Method            | Updates based on actions taken         | Updates based on best future action|
| Function Approximation   | Linear                                 | Linear                            |
| Exploration vs Exploitation | Balanced during action selection     | Prioritizes optimal policy estimation |

#### Hyperparameters and Tuning:
- **Discount Factor (γ)**: Controls the trade-off between immediate and future rewards.
- **Step Size (α)**: Governs the learning rate for adjusting the value estimates.

---

## Resources

- **Code Repository**: 

[GitHub - Epsilon-greedy Alhgorithm](https://github.com/RiccardoCampanella/Reinforcement_Learning/tree/main/Mutli-armed_Bandit_Algorithm)

[GitHub - Semi-grad SARSA and QLearning Algorithms](https://github.com/RiccardoCampanella/Reinforcement_Learning/tree/main/Robot_in_a_Maze)

- **Course**: Advanced Machine Learning

--- 
