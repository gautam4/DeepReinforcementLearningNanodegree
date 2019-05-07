# Project 2: Continuous Control
## Introduction

The environment used for this project is a version of the Unity ML Agents Reacher
environment. The agent in this environment is a double jointed robotic arm that is tasked with moving
itself into a specific position as if it were reaching for that position. The agent receives a reward of
+0.1 for each timestep that the arm is in the target position. The goal of the agent is to maintain itself
in this position for as many timesteps as possible.

The state space is the position, rotation, velocity, and angular velocities of the arm, totaling 33
variables. The action space is the torque vectors for the two joints, totaling an action size of 4, on the
arm each variable with a range from -1 to 1. There are two versions of this environment. In the first
version, there is one robotic arm that solves the environment when it averages a score of 30 or
greater over 100 episodes. In the second version, there are 20 different agents each with a copy of the
environment. This environment involves distributed training and works best for specific algorithms.
The version used for this project was the single agent version that solves the environment when the
average score exceeds 30 over a 100 episodes.

## Getting Started

The following steps are taken from the Udacity Deep-Reinforcement-Learning-Nanodegree/p2_continuous-control repository. 
The original list of instructions and links to the environment files can be found at the link below. 
Source: https://github.com/udacity/deep-reinforcement-learning/blob/master/p2_continuous-control/README.md

  1. Download the environment from one of the links below. You need only select the environment that matches your operating system:

       * Version 1: One (1) Agent

            * Linux: click here
            * Mac OSX: click here
            * Windows (32-bit): click here
            * Windows (64-bit): click here
 
 (For AWS) If you'd like to train the agent on AWS (and have not enabled a virtual screen), then please use this link (version 1) or 
this link (version 2) to obtain the "headless" version of the environment. You will not be able to watch the agent without enabling a 
virtual screen, but you will be able to train the agent. (To watch the agent, you should follow the instructions to enable a virtual 
screen, and then download the environment for the Linux operating system above.)

  2. Place the file in the DRLND GitHub repository, in the p2_continuous-control/ folder, and unzip (or decompress) the file.

#### Additional Steps
 * Adjust the line in cell 2 of the Jupyter notebook to match the location of the downloaded environment file depending on the system setup 
 that the notebook is run on.
 * Note: Running the Jupyter notebook included in this Project 2: Continuous Control repository will not display the agent as it is training.
 
 ## Instructions
 
 ### To observe an agent in training
 
 The entirety of the solution is written in the Continuous_Control.ipynb jupyter notebook. Open the Notebook and run the initial 
 setup cells 1,2,3,and 4. To observe a random agent, run cell 5. For a DDPG algorithm based solution, run cell 6,7,and 10

* Cell 6: Defines the Actor and Critic Network
* Cell 7: Defines DDPGAgent, OUNoise, and ReplayBuffer
    * DDPGAgent is the DDPG agent
    * OUNoise is a an Ornstein-Uhlenbeck noise process
    * ReplayBuffer is the memory buffer
* Cell 10: Initializes and creates a DDPGAgent with the environment parameters. 
           Trains the DDPGAgent in the environment while keeping track of the score.

### To observe a trained agent
* Load the network weights included in this repository and observe the resulting score of the NavAgent. Each weights file is names to match 
with the network it corresponds to.
    * Example
      * continuousControlcheckpoint_actor_target.pth = actor target network weights
 
 ## Project Results/Discussion
 * The project results, including a plot of score results and a detailed explanation of the algorithm theory and implementation, are included in the Report_ContinuousControl.pdf
