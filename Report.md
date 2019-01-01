# Introduction
The goal of this project is to train agent such that it can collect only yellow bananas while not collecting the black bananas.

# Implemention

A simple dqn was implemented. We use a target network using a dqn network. A target network was used to stabilize the training process. The 
network target network was updated every iteration by mixing a small amount of weights with the target network during each learning step.


## Hyperparamters

Various hyper parameters were tried before settling on the following values
Hyperparameter | Value
--- | ---    
batch_size | 64
gamma | 0.99
Learning rate | 5e-4
tau | 1e-3
update_every | 4

## Network Structures

### Action value function

Layer | Dimension
--- | ---
Input | N x 37
Linear Layer,  Relu | N x 64
Linear Layer, Relu | N x 64
Linear Layer Output | N x 4

## Training Results
The goal was achieved in 289 episodes. The graph is embedded in the ipython notebook.


# Ideas for future work
1. Work with the image directly to learn the model. 
2. Experiment with double_dqn and duelling network.
