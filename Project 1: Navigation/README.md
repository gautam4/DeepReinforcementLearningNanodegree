# Project 1: Navigation
## Introduction
This project uses a modified version of the UnityML-Agents Bananas environment. This environment involves an agent navigating around
in a world with blue and yellow bananas. The blue bananas provide a reward of -1.0, while the yellow bananas provide a reward of +1.0. 
The goal of the agent is to maximize the number of yellow bananas collected. 

The agent is limited to moving forward or backward or turning left or right. The state space
consists of the velocity of the agent and a representation of the objects in the direction the agent is
facing in. The task is episodic with the environment considered solved when the agent averages a
score of at least +13 over 100 consecutive episodes.

## Getting Started

The following steps are taken from the Udacity Deep-Reinforcement-Learning-Nanodegree/p1_navigation repository. 
The original list of instructions can be found at the link below.
Source: https://github.com/udacity/deep-reinforcement-learning/blob/master/p1_navigation/README.md
1. Download the environment from one of the links below. You need only select the environment that matches your operating system:

* Linux: click here
* Mac OSX: click here
* Windows (32-bit): click here
* Windows (64-bit): click here
  * (For Windows users) Check out this link if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

(For AWS) If you'd like to train the agent on AWS (and have not enabled a virtual screen), then please use this link to obtain the "headless" version of the environment. You will not be able to watch the agent without enabling a virtual screen, but you will be able to train the agent. (To watch the agent, you should follow the instructions to enable a virtual screen, and then download the environment for the Linux operating system above.)

2. Place the file in the DRLND GitHub repository, in the p3_collab-compet/ folder, and unzip (or decompress) the file.

Note: Running the Jupyter notebook included in thisProject 1: Navigation repository will not display the agent as it is training.

## Instructions
### To observe an agent in training
 The entirety of the solution is written in the Navigation.ipynb jupyter notebook. 
 Open the Notebook and run the initial setup cells 1,2,3,and 4.
 To observe a random agent, run cell 5.
 For a DQN algorithm based solution, run cell 6,7,11 and 12
 * Cell 6: Defines the QNetwork
 * Cell 7: Defines NavAgent and ReplayBuffer
      * NavAgent is the DQN agent 
      * ReplayBuffer is the memory buffer
 * Cell 11: Initializes and creates a NavAgent with the environment parameters
 * Cell 12: Trains the NavAgent in the environment while keeping track of the score.
 
 ### To observe a trained agent
 Load the network weights included in this repository and observe the resulting score of the NavAgent
