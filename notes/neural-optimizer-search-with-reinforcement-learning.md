# Notes on the paper: Neural Optimizer Search with Reinforcement Learning

Read the paper [here](https://arxiv.org/abs/1709.07417)

## Summary
The paper focused on using (reinforcement) learning to learn an optimal optimizer update rule. Our current neural network optimizers (e.g. sgd, adam, adagrad, rmsprop etc) are all hand crafted by human.
What if we can develop a machine learning system (in the paper, a neural network) that **learns** to produce an optimizer (update rule)?  (hence produce optimizer not **directly** created by humans)
The above question is the focus of this paper. This is a branch of the **Meta-Learning (learning to learn)** sub-field in Machine Learning.


## Notes
1. Authors focused on developing new update rule (optimizer update rule like sgd, adam, rmsprop etc) for neural networks.
2. They argued that the current advances optimizers uses heuristics and some borrowed ideas from convex function optimization even though deep neural networks are non-convex by nature.
3. Rather than develop a new optimizer update rule by hand, they focused on learning an optimizer update rule using a neural network
4. Related works focused on training algorithms to generate numerical updates for training model (i.e. generate the update values rather than the actual formula/update-rule that produced those values). This paper however focusedd on generating optimizer update rule
5. The system comprises of two neural networks. A Recurrent Neural Network (RNN) trained to generate optimizer update rule, and another neural network on which the generated update rule is evaluated. RNN generates update rules (as domain specific language - specified by the researchers) which is then used to train a  model (another neural network). The validation accuracy obtained from training the second model is kept and used to as **reward signal** for the RNN whcih is trained using **Reinforcement Learning (RL)**.
6. The Domain Specific Language (DSL) defined by the researchers are the building blocks used by the RNN to generate update rules. Check out **section 4.1** of the paper for the DSLs an their respective categories.
7. Techniques (tricks) used by researchers to speed up and accelerate training includes
  - **Reduce Training Computation Complexity**: the **second neural network** used to evaluate update rules (generated by the RNN) is **a small 2 layer convolutional neural network** trained for only 5 epochs. The authors stated this should provide enough signal whether the update rule will do well.
  - **Proximal Policy Optimization (PPO)**: this was used instead of REINFORCE for obtaining policy gradient for the RL training on the RNN.
  - **Distributed Training Scheme**: samples (update rule) generated by the RNN controller are added to a queue and run on a number of distributed works that are connected across a network. Through this setup, the researcher were able to testing multiple generated update rules in parallel.

## Update Rules Discovered in the Work
The researcher discovered interesting update rules that worked on the small convolutional network used to test the rules. However, they further narrowed down the list of update rules by using them to train [Wide ResNet](https://github.com/szagoruyko/wide-residual-networks) architecture for 300 epochs.
This narrowed things down to two main category (family) of update rules. They are;
  - Power Sign 
  - Add Sign

## Testing Discovered (Generated) Optimizers on Known Architectures for Specific Tasks
The researchers tested their discovered (generated) update rule on a variety of tasks. For each task, they used existing neural network architecture that is known to work well for that particular task (i.e. training the architecture using the generated optimizers).
(See the paper for information about the results on different tasks)

1. Image classification on CIFAR-10 dataset using [Wide ResNet](https://github.com/szagoruyko/wide-residual-networks) architecture
2. Image classification on ImageNet dataset using [NasNet-A](https://arxiv.org/abs/1707.07012)
3. Neural Machine Translation on WMT 2014 (English to German) dataset using [Google's Neural Machine Translation Architecture](https://arxiv.org/abs/1609.08144)
   If you prefer to read blogpost about the architecture, check [here](https://research.googleblog.com/2016/09/a-neural-network-for-machine.html)
4. Language Modelling on Penn TreeBank (PTB) dataset using a LSTM neural network architecture built by the researcher (while taking advantage of recent advances such as variational dropout, weight tying and so on). See section 6.5 of paper for architecture description.
