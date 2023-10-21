# Deep learning for image understanding 
Folder with a sequence of standalone 
projects to study ML/DL techniques to 
analyze images. 
The work is based on the Deep Learning
course followed at Sorbonne Université during the academic year 2022/2023. 

## Structure
Each folder contains a description of the theories behind the project and the results obtained, along to the google colab notebook. 


## Project 1 - Image Descriptor and Classification
Here my paper analyzing the work on this first projct: [go to paper HW-1](./1-Image-Descriptors-Classification/HW1.pdf)

The first project is focused on the study and understanding of how images are coded and classified when using ML/DL techniques. 
The most widely used descriptors are SIFT and the BoW
techniques. SIFT is a feature extraction method invariant 
to scale and orientation of picture, so that different 
angles and scales depicting the same 
figure are classified within the same class. 
The Bag of Words technique allows us to summarize the 
local SIFT descriptors of an image into a global descriptor, 
with the help of a visual dictionary. 

### 1_ab Image Descriptors: SIFT and BoW 
Brief description [Sift_and_BoW](./1-Image-Descriptors-Classification/1-Sift-and-BoW/description.md) 


### 1_c Image Classification: SVM
Brief description [SVM](./1-Image-Descriptors-Classification/2-SVM-Image-Classification/description.md) 


## Project 2 - Neural Networks and Convolutional NN
Here my paper analyzing the work on this second projct: [go to paper HW-2](./2-CNN/HW2.pdf). 

In this projects we explore Neural Networks and Convolutional 
Neural Networks. 
In order to appreciate their work, we initially 
manually calculate the steps followed by the NN, 
and then gradually introduce PyTorch libraries. 

### 2_ab Intro to Neural Networks
Brief description [NN](./2-CNN/2-ab/description.md). 

### 2_cd Intro to Convolutional NN
Brief description [CNN](./2-CNN/2-CNN/description.md).

## Project 3 - CNNs and GANs
Here my paper analyzing the work on this third projct: [go to paper HW-3](./3-CNN-and-GAN/HW3.pdf). 

### 3_a Trasfer Learning through feature extraction from a CNN
Brief description [Transfer Learning](./3-CNN-and-GAN/1-transfer-learning/description.md).  

### 3_b Visualizing CNN logic
Brief description [Visualizing CNN logic](./3-CNN-and-GAN/2-visualization/description.md).  

### 3_c Domain adaptation
Brief description [Domain Adaptation](./3-CNN-and-GAN/3-domain-adaptation/description.md) : 

### 3_d GANs
Brief description [GANs](./3-CNN-and-GAN/4-GAN/description.md) : 


## Project 4 - Machine Learning Analysis
Here my paper analyzing the work on this fourth projct: [Go to paper HW-4](./4-ML-analysis/HW4.pdf). 

### 4_a Robustness analysis
Brief description [Robustness Analysis](./4-ML-analysis/1-robustness-analysis/description.md).

### 4_b Bayesian Regression Model
Brief description [BRM](./4-ML-analysis/2-BRM/description.md).

### 4_c Uncertainty applications
Brief description [Uncertainty applications](./4-ML-analysis/3-uncertainty/description.md).



## Structure
Each folder contains a brief description of the project and the google colab notebook.
For each group of folders falling under the same number, which means that the topics encountered are linked to one another, there's a .pdf paper containing 
questions and answers circa various analysis and theoretical aspects linked to the projects.

## Project 1
Here my paper analyzing the work on this first projct: [go to paper HW-1](https://github.com/giuliaprosio/deep-learning-for-image-undestanding/blob/main/HW1.pdf)
### 1_ab Sift and BoW image descriptors

Brief description [1_ab](https://github.com/giuliaprosio/deep-learning-for-image-undestanding/tree/main/1-ab) :
Image Descriptors with SIFT and Bag of Words
The purpose of the practical work 1-ab was to produce an algorithm able to classify images using
visual descriptors.

In order to do so we proceeded by steps, the first being the realization of a SIFT descriptor for each
16x16 pixel patch of each picture contained in the dataset 12-Scenes.
The first tool presented throughout the Practical Work was the Scale-Invariant Feature Transform
(SIFT) - which is a local descriptor widely used in Image Classification as it is a feature extraction
method that is invariant to scale and orientation of the images and robust to fluctuations of illumina-
tion, noise and minor viewpoint changes in the images.

Among the key-points in the computation of the SIFT descriptor the first one is to calculate the gra-
dient of each pixel composing the patch selected.

After having then computed the weighted gradient using a Gaussian mask and discretizing the orien-
tation of the gradient to 8 possible values (having 0 for the NORTH direction, 1 for NORTH-EAST,

and so on), it is possible to build an histogram of the gradients for each region. The histograms can
finally be concatenated to compose the SIFT descriptor of the patch.
The second step of the practical work was to compute a Visual Dictionary, so that it is possible to
find frequent patterns and patches with similar SIFT descriptors can be grouped together. In order
to solve this problem we used a K-Means algorithm, determining K centers of the SIFT space and
minimizing the distance from the actual SIFTs.
The final step of this first practical work was to obtain a numerical representation of each image, so
that it can be easily classified. To do so we used a Bag of Words (BoW) algorithm, with which we
were able to summarize all the local SIFT descriptors of the image into a global descriptor, with the
help of the visual dictionary.

### 1_c SVM

Brief description [1_c](https://github.com/giuliaprosio/deep-learning-for-image-undestanding/tree/main/1-c) :

In project 1-ab, we built a processing pipeline that transformed a RGB image into a compact
representation that is more suited to image classification. Now, each image is encoded as a BoW vector
describing in some way the presence (or absence) of p = 1000 patterns in the image. The vector of the i-th
image, thus, is xi ∈ R
p
. Moreover, we know that each image can belong to one of 15 categories from our
dataset. Therefore in this session, we will build the ultimate part of the pipeline, an image classifier that will
takes as input the BoW vector ! A lot of different machine learning models can be used at that point, and
we will use the popular SVM (Support Vector Machine).

## Project 2
Here my paper analyzing the work on this second projct: [go to paper HW-2](https://github.com/giuliaprosio/deep-learning-for-image-undestanding/blob/main/HW2.pdf)

### 2_ab intro to Neural Networks
Brief description [2_ab](https://github.com/giuliaprosio/deep-learning-for-image-undestanding/tree/main/2-ab) : 

The goal of this practical work is to build a simple neural network and to become familiar with these models
and how to train them with the backpropagation (or backpropagation) of the gradient.
To do this, we will begin by theoretically studying a perceptron with a hidden layer and its learning
procedure. We will then implement this network with the PyTorch library first on a toy problem to check
that it is working correctly, then on the MNIST dataset.
The site http://playground.tensorflow.org makes it possible to visualize the functioning and the
learning of small neural networks




[Go to paper HW-2](https://github.com/giuliaprosio/deep-learning-for-image-undestanding/blob/main/HW2.pdf)

[Go to paper HW-3](https://github.com/giuliaprosio/deep-learning-for-image-undestanding/blob/main/HW3.pdf)

[Go to paper HW-4](https://github.com/giuliaprosio/deep-learning-for-image-undestanding/blob/main/HW4.pdf)

