# Project 3: Collaboration and Competition

### Introduction

This project is designed to train an agent using deep reinforcement learning through deep Q network.two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1.  If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01.  Thus, the goal of each agent is to keep the ball in play. The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation.  Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping. The task is episodic, and in order to solve the environment, the agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents).

### Implementation

DQN algorithm, experience replay, action noise, noise amplifier, DDPG (Deep Deterministic Policy Gradient), actor critic methods were used to solve this problem. The code base architect outline is from [DDPG-Bipedal Udacity project repo](https://github.com/udacity/deep-reinforcement-learning/tree/master/ddpg-bipedal).
The agents share critic but work with its own local actor. Using a decaying noise to explore first then exploit.

### Hyperparameters
Tested different combinations, values below will allow the agent to solve the problem faster.

Hyperparameter | Value
--- | ---
Buffer size | 1e6    
Batch size | 256
Gamma | 0.99
τ | 1e-3
LR-actor | 1e-4
LR-actor | 1e-3

### DQN structure

Both the actor and critic nerual network contains 2 fully connected layer with 256 and 128 inputs, the relu and tanh activation functions are used. The state space is 33 and action space is 4.

The basic structure is from model.py in  [DDPG-Bipedal Udacity project repo](https://github.com/udacity/deep-reinforcement-learning/tree/master/ddpg-bipedal).

### Results
Below is the number of episodes needed to solve the environment for DDPG actor critic

### Ideas for future improvements
1. Add a LSTM layer to the network because each state could be moving to different directions

2. Add transfer learning and share experience, nerual weights and bias

3. A3c, PPO and D4PG could be implemented

4. Add dropout layer to prevent agent from overfitting

5. Play against itself