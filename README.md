# Reinforcement Learning (RL) Tutorial
Machine learning mainly consists of three methods: Supervised Learning, Unsupervised Learning and Reinforcement Learning. Supervised Learning provides mapping functionality between input and output using labelled dataset. Some of the supervised learning methods: Linear Regression, Support Vector Machines, Neural Networks, etc. Unsupervised Learning provides grouping and clustering functionality. Some of the supervised learning methods: K-Means, DBScan, etc. Reinforcement Learning is different from supervised and unsupervised learning. RL provides behaviour learning. 

**Keywords:** Dynamic Programming (Policy and Value Iteration), Monte Carlo, Temporal Difference (SARSA, QLearning), Approximation, Policy Gradient, DQN.

## What is RL?
"A reinforcement learning algorithm, or agent, learns by interacting with its environment. The agent receives rewards by performing correctly and penalties for performing incorrectly. The agent learns without intervention from a human by maximizing its reward and minimizing its penalty" [*](https://www.techopedia.com/definition/32055/reinforcement-learning). RL agents are used in different applications: Robotics, self driving cars, playing atari games, managing investment portfolio, control problems. I am believing that like many AI laboratories do, reinforcement learning with deep learning will be a core technology in the future.

There are many tutorials in the internet. This one summarizes all of the tutorials with demo of RL algorithms.

### Markov Decision Process:
- It consists of five tuples: status, actions, rewards, state transition probability, discount factor.
- Markov decision processes formally describe an environment for reinforcement learning.

#### Markov Property:
A state S<sub>t</sub> is Markov if and only if P[S<sub>t+1</sub>|S<sub>t</sub>] =P[S<sub>t+1</sub>|S<sub>1</sub>,...,S<sub>t</sub>]

![rl-agent-env](https://user-images.githubusercontent.com/10358317/49733000-71881000-fc91-11e8-89ab-503775f44d32.jpg) 
[Sutton & Barto Book: RL: An Introduction]



## RL Components:
### Rewards:
- A reward Rt is a scalar feedback signal.
- The agent’s job is to maximise cumulative reward
### State Transition Probability:
- p(s′,r|s,a).=  Pr{S<sub>t</sub>=s′,R<sub>t</sub>=r|S<sub>t-1</sub>=s,A<sub>t−1</sub>=a},
### Discount Factor:
- The discount γ∈[0,1] is the present value of future rewards.
### Return:
- The return G<sub>t</sub> is the total discounted reward from time-step t.
- ![return](https://user-images.githubusercontent.com/10358317/49737029-c9784400-fc9c-11e8-8e05-23e6d7bb9fd0.jpg)
[David Silver Lecture Notes]
### Value Function:
- Value function is a prediction of future reward. How good is each state and/or action.
- The value function v(s) gives the long-term value of state s
- V<sub>π</sub>(s) =E<sub>π</sub>[R<sub>t+1</sub>+γR<sub>t+2</sub>+γ<sup>2</sup>R<sub>t+3</sub>+...|S<sub>t</sub>=s]
- Value function has two parts: immediate reward and discounted value of successor state.
- ![value_function](https://user-images.githubusercontent.com/10358317/49737276-7eaafc00-fc9d-11e8-83ad-e21feec25c16.jpg)
[David Silver Lecture Notes]
### Policy (π): 
A policy is the agent’s behaviour. It is a map from state to action. 
- Deterministic policy: a=π(s).
- Stochastic policy: π(a|s) =P[A<sub>t</sub>=a|S<sub>t</sub>=s].
### State-Value Function:
![state-value](https://user-images.githubusercontent.com/10358317/49737548-3b9d5880-fc9e-11e8-8549-d868556f0569.jpg)
[David Silver Lecture Notes]
### Action-Value Function: 
![action- value](https://user-images.githubusercontent.com/10358317/49737562-448e2a00-fc9e-11e8-9e57-8c04649b9a99.jpg)
[David Silver Lecture Notes]

### Optimal Value Functions:
![optimal-value](https://user-images.githubusercontent.com/10358317/49737868-f3cb0100-fc9e-11e8-82f8-f718f2af6b51.jpg)
[David Silver Lecture Notes]

### Planning vs RL:
#### Planning:
- Rules of the game are known.
- A model of the environment is known.
- The agent performs computations with its mode.
- The agent improves its policy.
#### RL:
- The environment is initially unknown.
- The agent interacts with the environment.
- The agent improves its policy.

### Exploration and Exploitation:
- Reinforcement learning is like trial-and-error learning.
- The agent should discover a good policy.
- Exploration finds more information about the environment.
- Exploitation exploits known information to maximise reward

### Prediction & Control Problem:
- Prediction: evaluate the future (Given a policy).
- Control: optimise the future (Find the best policy).

## Grid World:

## Dynamic Programming Method: Full Model
### Policy Iteration:
### Iterative policy evaluation:
### Policy Improvement:

## Monte Carlo Method:
### Exploring Stars:
### Monte Carlo Prediction Problem:
### Monte Carlo Control Problem:
### Monte Carlo Epsilon Greedy:

## Temporal Difference Learning Method:
### TD(0) Learning
### SARSA:
### Q-Learning:

## Function Approximation:

## Open AI Gym:

## Policy Gradient:
- Model Free Algorithm.

## Actor-Critic:
- Model Free Algorithm.

## Deep Q Learning:

## Imitation Learning:

## Meta-Learning:

## Inverse RL: 

## Deep RL: 

## POMDPs (Partial Observable MDP): 
![pomdps](https://user-images.githubusercontent.com/10358317/49738014-5c19e280-fc9f-11e8-8ca6-fe8fbeb0a5df.jpg)
[David Silver Lecture Notes]


## Resources:
Free Lectures:
http://rail.eecs.berkeley.edu/deeprlcourse/

https://sites.google.com/view/deep-rl-bootcamp/lectures



Udemy:

Udacity:

## Papers:
- Q-Learning: V.  Mnih, K. Kavukcuoglu, D. Silver, A. Graves, I. Antonoglou, et al. “Playing Atari with Deep Reinforcement Learning”. (2013).
- Policy Gradient: J. Schulman, S. Levine, P. Moritz, M. I. Jordan, and P.  Abbeel. “Trust Region Policy Optimization”. (2015).
- Policy Gradient: V. Mnih, A. P. Badia, M. Mirza, A. Graves, T. P. Lillicrap, et al. “Asynchronous methods for deep reinforcement learning”. (2016).
- Robots-Guided policy search: S. Levine*, C. Finn*, T. Darrell, P. Abbeel. “End-to-end training of deep visuomotor policies”. (2015).
- Robots-Q-Learning: D. Kalashnikov et al. “QT-Opt: Scalable Deep Reinforcement Learning for Vision-Based Robotic Manipulation”. (2018)
- AlphaGo- Supervised learning + policy gradients + value functions + Monte Carlo tree search D. Silver, A. Huang, C. J.Maddison, A. Guez, L. Sifre, et al. “Mastering the game of Go with deep neural networks and tree search”. Nature (2016).


## References:
- Sutton & Barto Book: Reinforcement Learning: An Introduction
- David Silver Lecture Notes: (http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching.html)
