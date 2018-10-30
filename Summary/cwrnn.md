# A Clockwork RNN

* [Paper](/Papers/CWRNN/CWRNN.pdf)
* [Unofficial Implementation](https://github.com/tomrunia/ClockworkRNN)

## Notes and Insights: 

* Instead of running all cells at a single clock rate, run them at different clock rates. Helps remember long term dependencies and improves representation capabilities. Only modules of particular frequencies operate at a given timestep.

* Differential frequency information is retained due to multiple freq. modules. Obvious expectation.

* All units within a module are interconnected. Reason? 

* On seq. generation, CW-RNNs clearly beat LSTMs.  


## Ideas:

* Hessian-Free RNN Training:  
It is reported that Hessian Free optimization can make RNNs remember long range dependencies although at the cost of computation. Understand and verify. [Martens & Sutskever](http://www.icml-2011.org/papers/532_icmlpaper.pdf)

* Experiment with varying time period rules:  
This paper uses T=2^i as the rule. Implement other rules. Paper suggests Fibonacci, Linear, Log. 

* Learnable time period rules:  
   1. Derive a differentiable function for choosing time periods and use backprop.
   2. Or use evolutionary algorithms instead.



