
## Unread/Unwatched
#### [Meta Learning] - article, meta-learning  
https://www.cifar.ca/assets/machines-learn-new-ways-of-learning/  
*Short Note:*

#### [Synthetic Gradients] - blog post, speeding-up-training-nn  
http://iamtrask.github.io/2017/03/21/synthetic-gradients/  
*Short Note: rather than actually compute gradient via backprop, each NN layer approximates their gradient by learning.*

#### [About SGD] - blogpost  
https://medium.com/intuitionmachine/the-peculiar-behavior-of-deep-learning-loss-surfaces-330cb741ec17  
*Short Note: *

#### [CMU Fall 2017 NLP Course] - video, nlp-lectures  
https://www.youtube.com/watch?v=Sss2EA4hhBQ&list=PL8PYTP1V4I8ABXzdqtOpB_eqBlVAz_xPT  
*Short Note: Carnegie Mellon University lectures on Neural Networks for Natural Language Processing (NLP)*

#### [Building your own neural machine translation system] - blogpost, nmt, seq2seq  
https://research.googleblog.com/2017/07/building-your-own-neural-machine.html  
*Short Note:*

#### [Unsupervised Neural Machine Translation] - nmt, research-paper
https://arxiv.org/abs/1710.11041  
*Short Note:*


## Read/Watched
#### [Learning Through Interaction: Generalisation in Robot RL] - video (highly technical)  
https://www.youtube.com/watch?v=Ko8IBbYjdq8  
*Short Note: Presenter presents a talk on the future of generalisation from two aspects. (a) Generalise to new tasks previously unseen (using visual video prediction) (b) Incorportate experiences from previous tasks into new tasks (few shot/transfer learning)*

#### [Understanding why Deep Nets work - Information bottleneck] - article, video (highly technical)  
https://www.quantamagazine.org/new-theory-cracks-open-the-black-box-of-deep-learning-20170921/  
https://www.youtube.com/watch?v=bLqJHjXihK8  
*Short Note: An hypothesis/theory of why/how (deep) neural nets works well. The basic idea is that the network learns to forget irrelevant parts of the training sample. Hence, only relevant information (features) of the training samples are squeezed through (the metaphorical bottleneck) as you propagate forward from layer to layer in a neural net.*  
**Update: (some part of) this theory is being refuted by a paper in the upcoming ICLR 2018 still on [open review](https://openreview.net/forum?id=ry_WPG-A-).** *I'll try to keep an eye on this paper.*


#### [Neural Optimizer search] - research-paper, meta-learning  
https://arxiv.org/abs/1709.07417  
*Short Note: neural optimizer. authors learnt new optimizers from cifar-10 dataset and claim that they generalise to other tasks. [View detailed note](https://github.com/dlpbc/ai-reading-list/blob/master/notes/neural-optimizer-search-with-reinforcement-learning.md)*

#### [Today’s Weak AI Lacks Intelligence by Numenta] - blogpost
https://medium.com/@Numenta/todays-weak-ai-lacks-intelligence-49869b4c61ae  
*Short Note: They (Numenta) argue that we need to upgrade ANNs. Neurons in ANN were modeled after our neuroscience understanding of the brain in the 1970s. There have been advances in neuroscience about our understanding of biological neurons and they believe this should be infused into our artificial models of the brain. See [here](https://github.com/dlpbc/ai-reading-list/blob/master/notes/weak-ai-lacks-intelligence-by-numenta.md) for complete note.*

#### [Does AI needs more innate machinery] - video, debate
https://www.youtube.com/watch?v=vdWPQ6iAkT4  
*Short Note: An interesting debate between 2 AI researchers from different backgrounds (Gary Marcus, a cognitive science and Yann lecun, a neural net researcher). Gary wants AI to infuse more innate machinery (such as object respresentation, causality, spatiotemporal contiguity and so on) and cites **translation invariance** as a success story of infusing innate machinery into AI as seen in convolutional nets. Yann believes more innate machinery is required but only a little amount of it. Yann considers learning algorithm advances are need more than innate machinery*

#### [DeepVO: A Deep Learning approach for Monocular Visual Odometry] - research-paper
https://arxiv.org/abs/1611.06069  
*Short Note: The paper entailed applying deep conv net architecture to predicting odometry for a moving agent (e.g. self driving car) using monocular vision (single camera as sensor). Train/Test data was derived from video data. The authors experimented with different structures of train and test data. First, image scene in training data also appeared in test data (overlapping scenes).They called this testing with known environment. Secondly, image scene in training data did not appear in test data and vice versa. They called this testing with unknown environment. The experiment involving test with known environment performed far better than testing with unknown environment. For future work, the authors posited add recurrent connections and the use of generative modeling to predict the next scene. [View detailed note](https://github.com/dlpbc/ai-reading-list/blob/master/notes/deep-learning-approach-for-monocular-visual-odometry.md)*

#### [Fully-Parallel Text Generation for Neural Machine Translation] - blogpost, nmt
https://einstein.ai/research/non-autoregressive-neural-machine-translation  
*Short Note: Authors introduced the idea of generating **parallel output** for neural machine translation tasks rather than generating one output word at a time. They achieved this feat using technique called **fertility predictor** (developed in the 1990s). The idea of the technique is produce a sequence of number in the **encoder part of the network**, whereby each input word in the exam    ple sequence is assigned a number. The number assigned to each word determines how much space will be allocated to it in the **decoder part of the network** (**intuition:** some words in english might require more than just a corresponding word to translate it in german). Armed with this knowledge (of space allocation), the decoder part of the network can then generate translations in parallel. The researchers employed this technique on an existing architecture called **Transformer** ([blog post](https://research.googleblog.com/2017/08/transformer-novel-neural-network.html), [research paper](https://arxiv.org/abs/1706.03762)) and obtained result comparable to state-of-the-art results in some translation dataset, while speeding up (approximately 15x) the time taken to translate language. The research paper for this blog post can be found [here](https://arxiv.org/abs/1711.02281). This blog post describes/summarizes the paper.*
