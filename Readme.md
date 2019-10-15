# Readme

##  Navigation - Deep Reinforcement Learning

### Udacity - Nanodegree Program - Deep Reinforcement Learning

### 1. Introduction

The code contained in the ```Navigation.ipynb``` file trains an agent to collect yellow bananas and to avoid blue bananas through a deep learning network. The Unity Banana Collectors Agents Environment is used.

The simulation contains a single agent that navigates a large environment.  At each time step, it has four actions at its disposal:
- `0` - walk forward 
- `1` - walk backward
- `2` - turn left
- `3` - turn right

The state space has `37` dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  A reward of `+1` is provided for collecting a yellow banana, and a reward of `-1` is provided for collecting a blue banana. 

The training is performed on ```n_episodes = 20000``` and is interrupted if the mean average score is equal or greater than 13.0 

### 2. Getting Started

The following packages are necessary to run the code:
- ```UnityEnvironment```. The executable file of the environment is available at https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip.
- ```numpy```
- ```torch```
- ```matplotlib```

The following files are necessary to run the code:
- ```model.py```
- ```dqn_agent.py```

### 3. Instructions

In order to run the code, execute the steps provided on the ```Navigation.ipynb``` notebook
