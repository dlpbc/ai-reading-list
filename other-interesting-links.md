# Other Interesting AI related links in the web
# Intro/Overview

### Machine Learning Terminology Explained
https://sigmoidal.io/machine-learning-terms/?url  
Note: Good intro into terminologies in AI such as NLP, CV, Neural Networks etc.

### Machine Learning Glossary
https://developers.google.com/machine-learning/glossary/

### A Glance at Reinforcement Learning
http://adgefficiency.com/glance-reinforcement-learning/  
Note: Good intro to RL for people who already have knowledge about supervised learning, but little or no knowledge of RL.

## Machine Learning Flash Cards
https://machinelearningflashcards.com/  
Note: flash cards for machine learning (full collection requires payment)

# Challenges

### NVIDIA AI City Challenge
https://www.aicitychallenge.org/  
Proposal Submission Deadline: *10th January, 2018*  
Note: This challenge is a workshop and competition for CVPR 2018.

### Visual Question Answering (VQA) Challenge
http://www.visualqa.org/challenge.html  
Note: Challenge to build an AI system that can answer a natural language question about an image.  
[Pytorch implementation](https://github.com/hengyuan-hu/bottom-up-attention-vqa) of the winning entry of 2017 VQA challenge.

### NIPS 2017 Reproducibility Challenge
https://nurture.ai/nips-challenge/  
Submission deadline: *31st January, 2018*

### ICLR 2018 Reproducibility Challenge
http://www.cs.mcgill.ca/~jpineau/ICLR2018-ReproducibilityChallenge.html  
Final submission/deadline: *December 15 2017*

### Cornell Natural Language Visual Reasoning (NLVR) Challenge
http://lic.nlp.cornell.edu/nlvr/  

## Visual Decathlon Challenge
http://www.robots.ox.ac.uk/~vgg/decathlon/  
Submission deadline: *20th July, 2017*  
Note: The goal of the challenge was to solve silmutaneously image classification problem from 10 different visual domains (datasets). It was setup as part of Pascal in Detail Workshop Challenge, CVPR 2017.


# Datasets and Enviroments
### Dataset - SLAC (MIT/Facbook Research)
http://slac.csail.mit.edu/  
Note: Sparsely Labeled ACtion (SLAC) dataset consist of 200 classes of 520K untrimmed videos and 1.75 Million clip annotations (clips trimmed from the 520K videos). It is large scale dataset for video action recognition and localisation. Just like the **Moments in Time Dataset**, it is similar to other video action recognition datasets such as [Kinetics](https://deepmind.com/research/open-source/open-source-datasets/kinetics/), [UCF-101](http://crcv.ucf.edu/data/UCF101.php), [HMDB-51](http://serre-lab.clps.brown.edu/resource/hmdb-a-large-human-motion-database/#Downloads) etc.

### Dataset - Moments in Time (MIT/IBM Research)
http://moments.csail.mit.edu/  
Note: a large scale dataset for video action recognition and understanding from MIT/IBM research. This dataset is similar to other video action recognition datasets such as [Kinetics](https://deepmind.com/research/open-source/open-source-datasets/kinetics/), [UCF-101](http://crcv.ucf.edu/data/UCF101.php), [HMDB-51](http://serre-lab.clps.brown.edu/resource/hmdb-a-large-human-motion-database/#Downloads) etc. However, it differs by focusing on creating labels that are *basic* rather than *specific* to a given example. The *basic* labels form a building block that can be used to richly describe a scene. It is made up of 1 million video clip, each clip having a 3 seconds. Check out this [IBM blogpost](https://www.ibm.com/blogs/research/2017/12/ai-video-understanding/) for more information.

### Environment - a Household Multimodal Environment (HoME) for AI agents
https://home-platform.github.io/  
Note: HoMe is a simulated platform where AI agents/bots can learn from vision, audio, simulated physics, and interaction with objects and other agents. Another platform similar to this one is the [OpenAI Gym](https://gym.openai.com/envs/). Work done in this area mostly focus on creating algorithms that can learn to act/behave appropriately in the environment (simulated 3D world, like a video game)

### Environment - CARLA
https://github.com/carla-simulator/carla
Note: Open-source simulator for autonomous driving research.
   
# Courses / Lectures

### Statistical Computing for Scientists and Engineers
https://www.zabaras.com/statisticalcomputing  
Note: The course covers techniques/tools/methods used in Bayesian Machine Learning.

### University of Toronto Fall 2017 - CSC2541: Scalable and Flexible Models of Uncertainty
https://csc2541-f17.github.io/  
Note: University of Toronto's course on Bayesian Neural Networks

### CMU Fall 2017 - Neural Nets for NLP
https://www.youtube.com/watch?v=Sss2EA4hhBQ&list=PL8PYTP1V4I8ABXzdqtOpB_eqBlVAz_xPT  
Note: Carnegie Mellon University lectures on Neural Networks for Natural Language Processing (NLP)

### Stanford University Fall 2017 - Theories of Deep Learning?
https://stats385.github.io/  (external course website)  
https://www.researchgate.net/project/Theories-of-Deep-Learning (contains links to lecture videos)

### Fast.ai Linear Algebra course for coders
http://www.fast.ai/2017/07/17/num-lin-alg/  
https://github.com/fastai/numerical-linear-algebra
  
  
  
# Blog Posts
### A Year in Computer Vision (published 2017)
http://www.themtank.org/a-year-in-computer-vision  
Note: An overview of recent advances (focused on 2016) in different areas (tasks) of computer vision.

### Notable Deep Net Architectures Developed for Object Classification and Other Related Tasks
https://adeshpande3.github.io/adeshpande3.github.io/The-9-Deep-Learning-Papers-You-Need-To-Know-About.html

### How to Unit test Machine Learning Code
https://medium.com/@keeper6928/how-to-unit-test-machine-learning-code-57cf6fd81765

### Teaching Cars To See — Advanced Lane Detection Using Computer Vision
https://medium.com/towards-data-science/teaching-cars-to-see-advanced-lane-detection-using-computer-vision-87a01de0424f
  
  
  
# Projects

### Initial Release of Mozilla’s Open Source Speech Recognition Model and Voice Dataset
blog post: https://mzl.la/2i2SPGX  
Source code for software (model): https://github.com/dlpbc/DeepSpeech  
Open source dataset: https://voice.mozilla.org/data  
Contribute: https://voice.mozilla.org/  
Note: You can contribute to the project by donating your voice, via recording of yourself reading a text sentence (provided by mozilla). Alternatively, you can also contribute by cross checking that the label (text sentence) assigned (by the software) to a pre-recorded audio clip is correct.

### Google Vizier (A service for black box optimisation)
A tool that helps find configuration/hyparameters settings for your neural network training.  
Unfortunately, it's only available to google cloud compute users and internally for google staff.  
  
However, there's an open source implementation of this tool. (I haven't tried it out)  
**open source implementation**: https://github.com/tobegit3hub/advisor
  
  
  
# Others

### Gentler introduction to Variational Auto Encoder (VAE)
https://www.dropbox.com/s/v6ua3d9yt44vgb3/cover_and_thesis.pdf?dl=0

### Simple Introduction to Deep Learning Techniques (CNNs, RNNs, VAE) using tensorflow
https://github.com/pkmital/tensorflow_tutorials
Note: Tensorflow implementation of algorithms from simpler ones (such as logistic regression) to more complex ones (such as variational autoencoders)

#### GitXiv
http://www.gitxiv.com/  
Note: research-papers + source-code-hosting (for corresponding research) + discussions.

#### ReScience Journal
http://rescience.github.io/  
Note: A peer-reviewed journal that promotes/encourages reproducible and replicatable research.
