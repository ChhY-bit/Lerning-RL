# Notes for Reinforcement Learning

## 0. 预备

### 0.1 强化学习方法的分类

**按模型（环境）：** 
Model-Free: 直接交互、等待现实反馈
Model-Based: 能够理解环境的方法（模型、世界），具有模拟、想象的能力
**按学习依据：**
基于概率：连续动作，如Policy Gradient
基于价值：离散动作，如Q-Learning、Sarsa
二者结合：**Actor-Critic**
**按更新方式：**
回合更新：完成后才更新策略，如Policy Gradient、Monte-Carlo Laerning
单步更新：每一步都更新策略，如Q-Learning、Sarsa、改进Policy Gradient
**按学习方式：**
在线学习：学习者亲自参与，如Sarsa
离线学习：学习者不参与，通过数据集学习，如Q-Learning、D

### 0.2 