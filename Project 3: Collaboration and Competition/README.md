# Project 3: Collaboration and Competition
## Introduction

The environment used for this project is a modified version of the UnityML Agents Tennis
environment. The environment involves two agents playing tennis opposite each other. Each agent can
move their racket forward or backward and up or down in a continuous manner. The goal of the
agents is to keep the ball from going out for as long as possible.

Each agent receives a reward of +0.1 if they hit the ball over the net. Each agent receives a
reward of -0.01 if it hits the ball out of bounds or misses hitting the ball back. The state space is the
position and velocity of the ball and the racket and has a size of 24. The agent’s action space has a size
of 2. Each agent receives its own local observation, indicating that each agent can be trained
somewhat independently of the other. The environment is considered solved when the agents’
average a score of +0.5 over 100 episodes.

Since there are two agents, the reward calculation is different than a simple sum. Each agent’s
rewards are determined per episode without discounting and the maximum of the two scores is
considered the score for that episode.

## Getting Started 

The following steps are taken from the Udacity Deep-Reinforcement-Learning-Nanodegree/p3_collab-compet repository. The original list of instructions and links to the environment 
files can be found at the link below. 
Source: https://github.com/udacity/deep-reinforcement-learning/blob/master/p3_collab-compet/README.md

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
 * Note: Running the Jupyter notebook included in this Project 3: Collaboration and Competition repository will not display the 
 agent as it is training.
 
 ## Instructions
 
 ### To observe an agent in training
 
 The entirety of the solution is written in the Tennis(1).ipynb jupyter notebook. Open the Notebook and run the initial 
 setup cells 1,2,3,and 4. To observe a random agent, run cell 5. For a DDPG algorithm based solution, run cell 6,7,and 8

* Cell 6: Defines the Actor and Critic Network
* Cell 7: Defines DDPGAgent, OUNoise, and ReplayBuffer
    * DDPGAgent is the DDPG agent
    * OUNoise is a an Ornstein-Uhlenbeck noise process
    * ReplayBuffer is the memory buffer
* Cell 8: Initializes and creates two agents with the environment parameters. 
          Trains the two DDPGAgents in the environment while keeping track of the score.

### To observe a trained agent
* Load the network weights included in this repository and observe the resulting score of the NavAgent. Each weights file is names to match 
with the network it corresponds to. Since both agents share an actor network, the actor network weights are not identified as agent 1 or agent 2
    * Example
      * Tennis_Model_checkpoint_actor_target = actor target network weights
      * Tennis_Model_Agent2checkpoint_critic_local = Agent 2 critic local network weights
 
 ## Project Results/Discussion
 * The project results, including a plot of score results and a detailed explanation of the algorithm theory and implementation, are 
 included in the Report_CollaborationAndCompetition.pdf

 
