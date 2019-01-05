# Notes on the paper: Efficient reinforcement learning through evolving neural network topologies
### Also known as Neuroevolution of Augmenting Topologies (NEAT)

Read the paper [here](http://www.cs.utexas.edu/~ai-lab/pubs/stanley.gecco02_1.pdf)

## Summary
NeuroEvolution is a field that focus on evolving neural systems (i.e. neural networks). In this field, you have a bunch of neural networks that forms a population, and the goal is to evolve (optimise) the population using evolution strategy towards a training objective. It consist of two main approach, which are;
- evolving weights of a fixed topology/structure (architecture as it is now called in present time)
- evolving weights and the topology of the network itself. 

Before this work, the first approach recorded more successes and gains. This work focused on second approach

In terms of representation, each genome contains bunch of genes which can be one of two class; a node gene (i.e. neural network neuron) and a connection gene (contains information about connection between two neurons and other information such as innovation number).

The researchers came up with technique to successfully perform crossover/mating between parent while preserving the structure through preservation of historical original of each gene in the genome/chromosome. To preserve this historical information, each connection gene is assigned an innovation number that is unique to every gene added to the system. 

Asides the regular mutation of weights which involves pertubation, mutation of topology (architecture) in this work was carried out by; 
- addition of new connection gene to a network.
- addition of new node gene to a network.

The major contribution of this work was the development of a NeuroEvolution system that can evolve both structure (architecture) and weights of the neural network with improved performance gain (e.g. speed and strength) over other methods at that time.

Candidate solutions that are innovative (i.e. bigger topologies, or very different) may be initially less fit  survive for generations because other well established candidates may be fitter. This can be a problem if the innovative candidate is one of the optimal solutions that we seek. To provent this, speciation techniques is used to divide the population into smaller groups (called species). A specie should contain candidates that are similar in structure / innovation. Furthermore, with the concept species, candidates compete locally within their specie rather than globally.

Finally, you can also learn more about Neuroevolution in general and NEAT by checking out this [blog post](http://blog.otoro.net/2016/05/07/backprop-neat/)
