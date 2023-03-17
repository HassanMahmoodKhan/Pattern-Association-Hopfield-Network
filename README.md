# Pattern-Association-Hopfield-Network
An association problem with the task of recognition, using several patterns. The proposed solution employs a discrete-time Hopfield network to recognize patterns given certain initial conditions.
A Hopfield Network is a type of recurrent artificial neural network that is designed for associative memory and pattern recognition tasks. It is a dynamical system that evolves in continuous or discrete time towards an asymptotically stable state, also known as an attractor.
## Data Generation
There are 8 clean patterns as represented in the problem statement, with each having dimensions of 12x10. The patterns are of grey-scale representation, and have been populated using bipolar values i.e., 1 & -1.

![Clean Patterns](https://user-images.githubusercontent.com/97694796/226001030-d43e47c6-9cbd-4de0-a519-0fb30e8222e1.png)

In addition, I have generated noisy patterns associated with each clean pattern by introducing random noise. This is achieved by reversing values of 25% of pixels i.e., 30 pixels per pattern.

![Noisy Patterns](https://user-images.githubusercontent.com/97694796/226001171-05eef2e5-726a-4369-ad62-e2a843bff42e.png)

## Network Learning
There are two learning modes for the Hopfield Network: Synchronous and Asynchronous.

### Synchronous Learning
Under synchronous learning, the transition from one state to another is done simultaneously. So, for a given time all elements of the input vector V are updated simultaneously considering the most recent values of changes.

### Asynchronous Learning
Under asynchronous learning, the transition from one state to another is done independently. For a given time, only a single neuron (randomly chosen) is allowed to update its output and only one element of the input vector V is updated considering the most recent values of changes.

## Evaluation
Four evaluation runs have been conducted:
1) Clean Pattern Recall (Synchronous)
2) Noisy Pattern Recall (Synchrnous)
3) Clean Pattern Recall (Asynchronous)
4) Noisy Pattern Recall (Asynchrnous)
