 ARCHITECTURE AND DESIGN CNN ARCHITECTURE 
CNNs are a class of Deep Neural Networks that can recognize and classify particular features from images and are widely used for analyzing visual images. Their applications range from image and video recognition, image classification, medical image analysis, computer vision and natural language processing. 
The term ‘Convolution” in CNN denotes the mathematical function of convolution which is a special kind of linear operation wherein two functions are multiplied to produce a third function which expresses how the shape of one function is modified by the other. 
Technically, deep learning CNN models to train and test, each input image will pass it through a series of convolution layers with filters (Kernels), Pooling, fully connected layers (FC) and apply Softmax function to classify an object with probabilistic values between 0 and 1. 4.1 Basic Architecture - 
There are two main parts to a CNN architecture 
● A convolution tool that separates and identifies the various features of the image for analysis in a process called as Feature Extraction 
● A fully connected layer that utilizes the output from the convolution process and predicts the class of the image based on the features extracted in previous stages. CNN Layers: 
The multiple occurrences of these layers shows how deep our network is, and this formation is known as the deep neural network. 
●Input: raw pixel values are provided as input. 
● Convolutional layer: Input layers translate the results of the neuron layer. There is a need to specify the filter to be used. Each filter can only be a 5*5 window that slides over input data and gets pixels with maximum intensities. 
● Rectified linear unit [ReLU] layer: provided activation function on the data taken as an image. In the case of back propagation, ReLU function is used which prevents the values of pixels from changing. 
●Pooling layer: Performs a down-sampling operation in volume along the dimensions (width, height). 
●Fully connected layer: score class is focused, and a maximum score of the input digits is found.
As we go deeper and deeper in the layers, the complexity is increased a lot. But it might be worth going as accuracy may increase but unfortunately, time consumption also increases. 
4.1.1 Convolutional Layer 
This layer is the first layer that is used to extract the various features from the input images. In this layer,the mathematical operation of convolution is performed between the input image and a filter of a particular size MxM. By sliding the filter over the input image, the dot product is taken between the filter and the parts of the input image with respect to the size of the filter (MxM). 

The output is termed as the Feature map which gives us information about the image such as the corners and edges. Later, this feature map is fed to other layers to learn several other features of the input image.
4.1.2 Pooling Layer 
In most cases, a Convolutional Layer is followed by a Pooling Layer. The primary aim of this layer is to decrease the size of the convolved feature map to reduce the computational costs. This is performed by decreasing the connections between layers and independently operates on each feature map. Depending upon the method used, there are several types of Pooling operations. 
In Max Pooling, the largest element is taken from the feature map. Average Pooling calculates the average of the elements in a predefined size Image section. The total sum of the elements in the predefined section is computed in Sum Pooling. The Pooling Layer usually serves as a bridge between the Convolutional Layer and the FC Layer.

4.1.3 Fully Connected Layer 
The Fully Connected (FC) layer consists of the weights and biases along with the neurons and is used to connect the neurons between two different layers. These layers are usually placed before the output layer and form the last few layers of a CNN Architecture. 
In this, the input image from the previous layers are flattened and fed to the FC layer. The flattened vector then undergoes few more FC layers where the mathematical functions operations usually take place. In this stage, the classification process begins to take place. 
4.1.4 Dropout 
Usually, when all the features are connected to the FC layer, it can cause 
overfitting in the training dataset. Overfitting occurs when a particular model works so well on the training data causing a negative impact in the model’s performance when used on new 
data.

5. METHODOLOGY 
5.1 Basic steps in constructing a Machine Learning model: 
5.1.1 - Data Collection 
● The quantity & quality of your data dictate how accurate our model is. ● The outcome of this step is generally a representation of data (Guo simplifies to specifying a table) which we will use for training 
● Using pre-collected data, by way of datasets from Kaggle, UCI, etc., still fits into this step 
5.1.2 - Data Preparation 
● Wrangle data and prepare it for training 
● Clean that which may require it (remove duplicates, correct errors, deal with missing values, normalization, data type conversions, etc.) 
● Randomize data, which erases the effects of the particular order in which w e collected and/or otherwise prepared our data 
● Visualize data to help detect relevant relationships between variables or class imbalances (bias alert!), or perform other exploratory analysis 
● Split into training and evaluation sets 
5.1.3 - Choose a Model 
● Different algorithms are for different tasks; choose the right one 
5.1.4 - Train the Model 
● The goal of training is to answer a question or make a prediction correctly as often as possible 
● Linear regression example: algorithm would need to learn values for m (or W) and b (x is input, y is output) 
● Each iteration of process is a training step
5.1.5 - Evaluate the Model 
● Uses some metric or combination of metrics to "measure" objective performance of model ● Test the model against previously unseen data 
● This unseen data is meant to be somewhat representative of model performance in the real world, but still helps tune the model (as opposed to test data, which does not) 
● Good train/eval split? 80/20, 70/30, or similar, depending on domain, data availability, dataset particulars, etc. 
5.1.6 - Parameter Tuning 
● This step refers to hyperparameter tuning, which is an "artform" as opposed to a science ● Tune model parameters for improved performance 
● Simple model hyperparameters may include: number of training steps, learning rate, initialization values and distribution, etc. 
5.1.7 - Make Predictions 
● Using further (test set) data which have, until this point, been withheld from the model (and for which class labels are known), are used to test the model; a better approximation of how the model will perform in the real world 
5.2 Methodologies for Handwritten Digit Recognition System 
We used MNIST as a primary dataset to train the model, and it consists of 70,000 handwritten raster images from 250 different sources out of which 60,000 are used for training, and the rest are used for training validation. Our proposed method mainly separated into stages, preprocessing, Model Construction, Training & Validation, Model Evaluation & Prediction. Since the loading dataset is necessary for any process, all the steps come after it.

5.2.1 Import the libraries: 
Libraries required are Keras, Tensor flow, Numpy, Pillow, Tkinkter. 
1. Keras: 
Keras is a powerful and easy-to-use free open source Python library for developing and evaluating deep learning models. It wraps the efficient numerical computation libraries Theano and TensorFlow and allows you to define and train neural network models in just a few lines of code. It uses libraries such as Python, C#, C++ or standalone machine learning toolkits. Theano and TensorFlow are very powerful libraries but difficult to understand for creating neural networks. Keras is based on a minimal structure that provides a clean and easy way to create deep learning models based on TensorFlow or Theano. Keras is designed to quickly define deep learning models. Well, Keras is an optimal choice for deep learning applications. 
2. TensorFlow: 
TensorFlow is a Python library for fast numerical computing created and released by Google. It is a foundation library that can be used to create Deep Learning models directly or by using wrapper libraries that simplify the process built on top of TensorFlow. TensorFlow tutorial is designed for both beginners and professionals. Our tutorial provides all the basic and advanced concepts of machine learning and deep learning concepts such as deep neural network, image processing and sentiment analysis.TensorFlow is one of the famous deep learning frameworks, developed by Google Team. 
3. Numpy: 
NumPy is a Python library used for working with arrays. It also has functions for working in the domain of linear algebra, Fourier transform, and matrices. Numpy, which stands for Numerical Python, is a library consisting of multidimensional array objects and a collection of routines for processing those arrays. 
4. Pillow: 
Pillow is a free and open source library for the Python programming language that allows you to easily create & manipulate digital images. Pillow is built on top of PIL (Python Image Library). PIL is one of the important modules for image processing in Python. However, the PIL module has not been supported since 2011 and doesn’t support python 3.
5. Tkinter: 
Tkinter is the standard GUI library for Python. Python when combined with Tkinter provides a fast and an easy way to create GUI applications. Tkinter provides a powerful object-oriented interface to the Tk GUI toolkit. 
5.3 Loading The Data Set: 
5.3.1 MNIST Data Set: 
Modified National Institute of Standards and Technology (MNIST) is a large set of computer vision dataset which is extensively used for training and testing different systems. It was created from the two special datasets of National Institute of Standards and Technology (NIST) which holds binary images of handwritten digits. The training set contains handwritten digits from 250 people, among them 50% training dataset was employees from the Census Bureau and the rest of it was from high school students. However, it is often attributed as the first datasets among other datasets to prove the effectiveness of the neural networks. 

The database contains 60,000 images used for training as well as few of them can be used for cross-validation purposes and 10,000 images used for testing. All the digits are grayscale and positioned in a fixed size where the intensity lies at the center of the image with 28×28 pixels. Since all the images are 28×28 pixels, it forms an array which can be flattened into 28*28=784 dimensional vector. Each component of the vector is a binary value which describes the intensity of the pixel.

5.6 Model Construction 
Now, comes the fun part where we finally get to use the meticulously prepared data for model building. Depending on the data type (qualitative or quantitative) of the target variable (commonly referred to as the Y variable) we are either going to be building a classification (if Y is qualitative) or regression (if Y is quantitative) model. 
5.6.1 Learning Algorithms 
Machine learning algorithms could be broadly categorized to one of three types: 1. Supervised learning 
In supervised learning, each example is a pair consisting of an input object (typically a vector) and a desired output value (also called the supervisory signal). A supervised learning algorithm analyzes the training data and produces an inferred function, which can be used for mapping new examples. An optimal scenario will allow for the algorithm to correctly determine the class labels for unseen instances. 
It is a machine learning task that establishes the mathematical relationship between input X and output Y variables. Such X, Y pair constitutes the labeled data that are used for model building in an effort to learn how to predict the output from the input. Supervised learning problems can be 
further grouped into regression and classification problems.
● Classification: A classification problem is when the output variable is a category, such as “red”or “blue” or “disease” and “no disease”. 
● Regression: A regression problem is when the output variable is a real value, such as “dollars” or “weight”. 
2. Unsupervised learning 
is a machine learning task that makes use of only the input X variables.Such X variables are unlabeled data that the learning algorithm uses in modeling the inherent structure of the data. Unsupervised learning problems can be further grouped into clustering and association problems. 
● Clustering: A clustering problem is where you want to discover the inherent groupings in the data, such as grouping customers by purchasing behavior. 
● Association: An association rule learning problem is where you want to discover rules that describe large portions of your data, such as people that buy X also tend to buy Y. 
3. Reinforcement learning 
Reinforcement learning is an area of Machine Learning. It is about taking suitable action to maximize reward in a particular situation. It is employed by various software and machines to find the best possible behavior or path it should take in a specific situation. 
Reinforcement learning differs from supervised learning in a way that in supervised learning the training data has the answer key with it so the model is trained with the correct answer itself whereas in reinforcement learning, there is no answer but the reinforcement the agent decides what to do to perform the given task. 
In the absence of a training dataset, it is bound to learn from its experience. It is a machine learning task that decides on the next course of action and it does this by learning through trial and error in an effort to maximize the reward. 
● Input: The input should be an initial state from which the model will start ● Output: There are many possible output as there are variety of solution to a particular problem 
● Training: The training is based upon the input, The model will return a state and the user will decide to reward or punish the model based on its output. The model continues to learn. The best solution is decided based on the maximum reward.

