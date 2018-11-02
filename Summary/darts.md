# Differentiable Architecture Search:

## Method:  

* **Search Space**:  
 Each cell is a acyclic directed graph with N nodes. Each edge between nodes represents an operation between nodes. The operations are chosen from a certain fixed set of operations.

* **Continuous Relaxation And Optimization**:  
    1. The optimal operation for an edge is parametrized by **a**. The decision is based on a softmax evaluation of the **a** vector.
    2. The problem is cast as an bilevel optimization task. The goal of the task is to find weights **w** and **a** for the minimum validation loss where the weights parametrize the minimum train loss for that **a**.

* **Approximation**:  
    1. The optimization is approximated with an iterative algorithm that defines a Stackelberg game. Weights are updated by descent on the train loss. **a** is updated by decsent on the validation loss with the updated weights.
    2. The gradient of the validation loss over **a** is evaluated using finite differences.

* **Deriving Architectures**:  
    1. Retain the strongest connections with nodes.
    2. Choose the best operation using softmax on **a**.

This paper tries to learn the basic cell structure only. The network architecture might have several of these cells put together in predetermined ways suited to the problems at hand. For exapmle, they could model a CNN-like or an RNN-like architecture depending on the task at hand.

## Insights:  

* The thousand-fold reduction in compute-time is commendable. Shows the power of directed optimization over discrete searches.

* **Advantages over dominant approaches**:  
  1. Evolution or RL based methods are very computationally intensive.
  2. DARTS searches over a richer search space over other algorithms.

* The nested optimization is also reminiscent of gradient-based hyperparameter search methods. Vector **a** instead of a scalar hyperparameter .
	
* The approximation is the key link holding together this work. Otherwise, the weights would have to be reused for every single value of **a**.

* No convergence guarantees currently delivered on the setup. Although, practically, it is possible to do so.

* An interesting observation made in the paper is that random architectures are competitive for both types of tasks. This reflects the importance of the search space design.


## Ideas:

* **Implement DARTS**:  
  Use a simpler task to fit in CPU.
* Further Speedups?  

