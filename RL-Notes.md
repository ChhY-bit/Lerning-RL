# Notes for Reinforcement Learning

## 0. 预备

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

## 基本概念
**1. 状态(state)**
能反映当前智能体的信息，用$x\in\mathbb{X}^{n}$表示，$\mathbb{X}$是状态空间。

**2. 动作(action)**
智能体在某个状态下，可以采取的行为，用$u\in\mathbb{U^{p}}$表示，$\mathbb{U^{p}}$是具有维度$p$的动作空间。

**3. 奖励(reward)**
智能体处于某个状态并执行某个动作时，由环境给予的反馈信息，用$r\in\mathbb{R}$表示。

**4. 回报(return)**
在$N$个时刻后，智能体所得到的奖励$ \boldsymbol{r} = \left[r_1,r_2,\cdots,r_N\right]$之和，用$J(\boldsymbol{r}):\mathbb{R}^N \to \mathbb{R}$表示。

**5. 策略(policy)**
描述智能体在一定状态下如何采取动作，用$u=\pi(x)$表示，$\pi(\cdot)$是策略函数。

**6. 环境(environment)**
定义了智能体交互、演变等规则，例如状态转移函数$x_{k+1} = f(x_k,u_k,k)$、奖励函数$r_k = g(x_k,u_k,k)$。

**强化学习的目的：** 寻找合适的策略$\pi(\cdot)$，使回报达到最优。