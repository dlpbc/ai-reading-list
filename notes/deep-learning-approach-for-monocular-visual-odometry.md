## Note
The paper investigated the application of deep convolutional neural network architecture in predicting odometry for a moving agent/robot. Odometry entails using data from motion sensors predicting/measuring change in position of an agent over time (e.g. robot, self driving cars etc). **Visual Odometry**, you simply use camera input (like video) as your motion sensing device. The paper focused on monocular visual odometry, which is based on a single camera sensor as input.

### Architecture used
**(AlexNet)[https://en.wikipedia.org/wiki/AlexNet]**

### Data Set
The authors employed the KITTI Vision benchmark dataset only considering video sequences from a single camera (monocular vision). 

The authors generated each training example as consecutive image pairs from video frames (i.e. at time step t, the generated example will be **Image<sub>t</sub>** and **Image<sub>t+1</sub>** in the video) 

### Train/Test Data Arrangement
The authors experimented with different structures of train and test data. First, they experiment with training network whereby the train and test data was generated from a combined source of 11 videos (with different train/test split 50:50 and 80:20). Hence the test data contains scenes that's also in the train data (train and test data contained overlapping scenes). They called this testing with **known environment**. Secondly, they experiment with training a network whereby the train and test data was generated from seperate videos (7 videos for train data, 4 videos for test data). Hence the test data contains scenes that are completely different from scenes in the train data (train and test data cotaiend disjoint scenes). They called this **testing with unknown environment**. 

The authors also experimented with a variant of the **testing unknown environment** experiment. In addition to the training example (image pairs), they added results from hardcoded feature detector (FAST - Feature from Accelerated Segement Test) as prior to the network. That is, for each image from video, the authors append the feature detector results to its Image RGB data, hence each image (in image pair training example) has 4 dimensional instead of 3. 

### Model Type
The task was modeled as a regression problem, to predict delta_x, delta_z and delta_theta.

#### Results
The experiment involving test with known environment performed far better than testing with unknown environment. Furthermore, in the knwon environment experiment, the 80:20 train/test split performed better than the 50:50 train/test split.

The experiment with the variant of testing unknown environment also performed poorly.

#### Future Work
In analysising the result form known environment experiment, the authors noted that the deviation of the prediction from ground truth (label) increased over time. With respect to this, the authors posited the following as future work:
- adding recurent connection: from my perspective, this makes sense to experiment with as video data can be modeled as a sequence of frames (i.e. sequential data, hence recurrence)
- using generative networks to predict the next scene: from my perspective, this should be common sense reason from video frame that Yann Lecun is looking into.
