# Differential Neural Computers:

* Differentiable Neural Computers : [Paper]( /Papers/DNC/Graves.pdf) 
[Math Appendix](/Papers/DNC/Appendix.pdf) 
* A detailed analysis of the math involved by **Juan Antonio Pérez-Ortiz** [here](https://jaspock.github.io/funicular/dnc.html)


## Insights:  

* __Differentiability:__  
An often used strategy in ML is to pose the task as an optimisation problem and employ gradient-based methods to solve it. Here, the concept of discrete memory-reads and writes is posed as accesses using differentiable attention-mechanisms to make the model trainable with gradient-based techniques.

* Memory and computation need not be separated as in modern computers. NNs aren't scalable dynamically on-the-go as memory resides in the connections.

* The effectiveness of DNCs is in part because on the tasks that we employ them in. Feeding them suitable tasks that leverage the presence of external memory gives them the edge over conventional sequence models.

* __Attention Mechanisms:__    
  * Context Lookup:  
The key vector is decided by a similarity metric. Pattern completion occurs. Models associative memory. Relation with Hopfield and other associated networks?

  * Temporal Links:  
  Stores temporal memory write patterns. A linear transformation can yield next or previous memory access label. Ability to remember input sequences enables learning of an entirely different subset of algorithms.

  * Memory Allocation:  
  Maintain a 'usage' score for each memory location to reuse memory based on number of reads and writes to that location.

* Temporal link matrix seems a task oriented addition to solve temporal tasks. 

## Ideas:

* __Implement a microprocessor with DNC:__  
A toy task. Try to implement a microprocessor that takes in instructions and inputs and operates on them. Train them for individual oncodes and demonstrate programmability with heavier tasks.

* __Sparse DNCs:__  
Use sparse DNCs to train more difficult tasks. Demonstrate capablility over conventional model. 

* __Devise Suitable Tasks:__  


## ToDo:
- [x] Add links and references
- [ ] Condense insights from the Methods section.

    
