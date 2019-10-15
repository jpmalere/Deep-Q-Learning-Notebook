# Report 

## Project - Navigation

### Deep Reinforcement Learning - Udacity Nanodegree program

### 1. Introduction

The ```Navigation.ipynb``` notebook implements a deep neural network that converts the states of the agent to the corresponding actions that maximizes the expected total future reward on the Unity banana environment.

The Deep Q-Learning algorithm is similar to the one for a discrete state-action space, with the exception that the Q table is not discrete but a non-linear function approximated through a neural network. 

For each episode there are two possible actions:
- Sample: The next action is choosen based on a epsilon-greedy policy and experience tuples (S, A, R, S') are stored for the learning phase;
- Learning: After a number of episodes, the learning phase occurs. The target is set from the experience tuples and the weights from the neural network are updated. 

The Deep Q-learning algorithm can be found at Reference [1] - Algorithm 1 description. 


### 2. Implementation

The ```Navigation.ipynb``` implements and describes the deep Q-learning algorithm for the banana collector Unity environment. 

The agent implementation is performed with two auxiliary files:
- ```model.py```: contains the class QNetwork where a neural network is implemented. A two hidden layer with 128 neurons each is coded. The first hidden layer is composed by a linear function with a relu activation. The second hidden layer is composed of linear functions.
- ```dqn_agent.py```: implements the class Agent with the ```step```, ```act```, ```learn``` and ```soft_update``` methods. The ```step``` method evokes the ```learn``` function when necessary or just save the experiences in a buffer. The ```learn``` function updates the neural network weights in order to minimize the loss function. The ```act``` function chooses the action based on the neural network or based on a epsilon-greedy policy. The ```soft_update```function updates the neural network weights.

The criteria for choosing the number of layers and the number of neurons was from the less complex to the more complex models. The initial considered number of layers was two and the hidden layer number of neurons was 64. After training the number of neurons was increased to 128, with a greater performance in terms of episodes to reach the stopping criteria (average score >= 13). The number of neurons was increased again to 256 per layer, but the performance didn't increase and the processing time was greater compared to the 128 neurons network. Given that the required performance was achieved (500 episodes for an average score greater than 13) the two hidden layers with 128 neurons each was selected for the project.


### 3. Discussion and future works

The deep Q-learning algorithm was able to train an agent to collect the right type of bananas on the simulated environment and fulfilled the specified requirement (average score equal or greater than 13 for 100 episodes). For future works the following improvements could be tested:
- Prioritized experience replay;
- Dueling Deep Q-Networks.

### 4. References¶

[1] Mnih V., Kavukcuoglu K, Silver D. Rusu A. A., Veness J., et al, "Human-level control through deep reinforcement
learning", Nature, doi:10.1038/nature14236
