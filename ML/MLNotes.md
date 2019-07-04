randomised# Part 1
### Machine learning
#### *Going Data-Driven*

**Complicate** doesn't mean **complex**  
It's not complex if you know how it works

#### The paradigm shift
Equation describing the processes (Process driven) -> Fitted model describing relationship (Data driven)

#### ML machine learning

+ **Supervised learning** learning by examples
  + Classification *discrete lables*
  + Regression *interfere continuos values*
+ **Unsupervised learning** *discover something i don't know*
    + Clustering *create proximity groups*
    + Dimensionality reduction
+ **Reinforcement learning** *learning by active feedback*

#### Classification

Gathering (Visualise) -> Labelling (Classify)  
how to separate classes?

we want to **interfere data (prediction)**
not necessarily a time prevision

we are looking for correlation between features and labels (We assume there is)

hues?

we are not considering internal mechanisms! It's only about interfering, without knowledge.
We consider only data position.  
If the data it's bad -> the result it's bad.

### Neural Networks

A real NN:
dendrites, axon, terminal axon, synapse
time dependent, unsynchronised
it's not really using BackPropagation

traditionally we had one hidden layer

**Deep Neural Network** means a NN with more than one hidden layer

> Example: AlexNet

**Universal approximation theorem** (George Cybenko)
[link](https://en.wikipedia.org/wiki/Universal_approximation_theorem)  
you can use only one layer!
  but it could be unfeasible!! Too complex


Classification it's a task, there's a lot of different ways to do it


### [scikit-learn](https://scikit-learn.org/)
***Model->Fit->Predict***

### K-Nearest Neighbors (KNN)
>  sklearn.neighbors.KNeighborsClassifier


Hyper-Parameters

using the **Number of Neighbors** you calculate distance and you predict a label of a new datapoint, you classify it.

set **Hyper-Parameters**
+ With Theory
+ Exploring data
+ Mimic good results
+ Trying

most of the scikit-learn parameters have a default values

KNN it's based on metrics, distances
important to scale features  
if one dimension it's not scaled (features ranges), It's difficult to fit the data in the correct way.

### Support-Vector Machine
> sklearn.svm.SVC

for a linear separable problems find the maximum margin
we can add dimensions (kernel application)

find a representation to easily separate them

### NN Neural Networks
> sklearn.neural_network.MLPClassifier  
> in nn each point it's multidimensional

shallow network, one hidden layer
composed by **MLP** multi layer perceptron

typically all the nodes of a nn, you work at layer level

**Input layer:** input features  
**Hidden layer** project them in a different dimensional   space
**Output layer** # nodes = output dimensionality

links between nodes are weighted
all the information of the nn it's in the weights

reinforce weights in each iteration of the training set

> convolutional layers, recurrent layers, feedforward layers

### Data input in scikit-learn

**Feature matrix** X : [n_samples, d_features]  
**Label vector** y : [n_labels]

We can use numpy arrays, but using **scipy.sparse** can be more efficient than numpy arrays.


the dataset should be balanced! (classified well)
if we only count the number of correctly classified we

> class weight function
> adjust accuracy

> useful commands:
> numpy  bincount(iris['target'])
> matplotlib.pyplot.scatter(
>
> to analyse data:
> seaborn.pairplot()

### Decision Tree

> sklearn.tree import DecisionTreeClassifier


useful description of the classification decisions.
we use it to model using all standard parameters, but we need to validate the results in some way.

#### analyse the results:

in classification problems you can use **Confusion matrix** to evaluate the resulting model

CM with two classes:

|                | Predicted P | Predicted N     |
| :------------- | :------------- | :-------------- |
| Actual P       | **True Positive**       | False Negatives |
| Actual N       | False Positives    | **True Negatives** |

with more dimensions:

```
sklearn.metrics.confusion_matrix(expected, predicted)
array([[50,  0,  0],
       [ 0, 50,  0],
       [ 0,  0, 50]])
```
the diagonal it's the number of correctly classified data points

##### GOLDEN RULE: **Never test the model with the training data you used for creating the model, you will have an incorrect error estimation**
```
metrics.confusion_matrix(expected, predicted)
array([[15,  0,  0],
       [ 0,  8,  3],
       [ 0,  7,  5]])
iris['target_names']
array(['setosa', 'versicolor', 'virginica'], dtype='<U10')

the '3' in the matrix means: we classificated
as 'virginica' a 'versicolor' 3 times
```

> another command To analyze results:  
> sklearn.metrics.classification_report()  

We want to **generalize**, it's important the model works with 'external' data

`sklearn.model_selection.train_test_split()`

generate two different sets randomly

**training set**: to train the model (input of the algorithm)  
**test set**: to check and validate the resulting model

> Jupyter cursor mac commands  
> ctrl + a cursor at the beginning block  
> ctrl + e cursor at the end of block  
> cmd + click for multiple cursors  

Always dubt about the results: the random train-set selection can be a non optimal one.

# Part 2 - Deep Learning

Geoffrey Hinton


biological plausibility
keras and

Shallow Nets to Inception

hierarchical

deep learning learns layers of features

### error minimisation

Convergence
global minimum and local minimum

Deep learning
do automatic feature extraction : domain free!

Computer prevision:
+ recognition
+ detection
+ segmentation

Deep learning for computer vision

+ inpainting
+ superresolution

Captioning:
+ indexing
+ subtexing

+ pose estimation

GauGAN
with generative adversarial network (GAN)
generator network -> discriminator Networks
falsario -> disctiminatore
entrambi diventano bravi! Generano images:

v3 inception google Adversarial attach

disegno -> foto

### The black box problems
we don't give instruction anymore, only examples
we lost control of what there's inside

+ Biased system
+ Right for the wrong reason
+ GDPR non-compliancy
+ no trust from experts, answer it's only a label
+ adversarial vulnerability

# Explainable AI
DARPA XAI project
Xai Explanation

**Keras**
spykit but for Deep Learning


dense if has input layer

there's a bias

layers freeze to not train them anymore
**Input**
flat image from 16*16 to 256

**Output**
1 output Perceptron for class
1 noted encoding [0,0,0,0,0,0,0,1,0,0,0,0]= 7

optimizer = 'adam'

epochs: go throught all input data xgtimes

MultilayerPerceptron has flat Inputloose the locality

#### Deep convolutional Neural Networks

convolution + non linearity --> max pooling
+
fully connected layers

Nx binary classification

### activation funcions
hystorically step funcions

not really derivable
low or hig derivate = 0
  gradiant vanish

rectified linear unit
relue leaky

easy derivative -> to appliate


### Deep Convolutional NN

weights initially randomised

RGB = 3 channels
> plt.imshow(cat.astype('int')[:200,-400:])
> plt.imshow(cat.astype('int')) [:200,-400:,0])
>plt.rc('image', cmap ='plasma')

batch of 3d objects ->
##### Convolution
 it works on 2D data, divide image by channels
 'filters' or 'kernels':
 size of kernels it's (3-7 normally) a hyperparameter.

 if the result >0 i propagate the signal

 Horizontal and vertical stride: how much forward i jump in each (usually they have same value)

 the weights of kernels are small! not the size of img. I don't care about the image size. weights sharing.


 invarianza transazionale.

 output it's an activation map.

 >from keras.layers.convolutional import Conv2D

Conv2D(  
  ...  
  padding= fake border to take more time the corners of img ('valid', 'same')  
  ...  
  )

##### max pooling
the size of the kernels shoul be at least
the receipting field should have ha size big as the size of the kernerls

 aggregation operation : max (max pooling)

 maxpooling_2D(


   )

max pooling it's a disaster... and it's a disaster that's working

hilton capsules net it's a variance of max pooling


### mondel = sequential()

convolution and pooling -> classification

we flatten all to feed the data to the MLP
we loose the space relation but we already extracted the features

**dropout regularization** This technique turns off neurons the let information flow in multiple layers sparsely. It randomly shout off neurons in the (precedent) layer.

Dense layer (fully connected)

we try to replicate successful architectures
> VGG (visual geometry group)
> alex net

do a .summary() to the model to see shapes and Parameters

(BatchSize(None if not trained), filter dimensions, #offilters)

Output shapes:

size: X*Y*#filters
After convolution the size change
32*32->28*28 if filter size 5*5-> (-4,-4)

activation maps sizes
30 * (5 * 5) filters * 3 channels + 5
(every filter has a bias) = 2280

30 * (5 * 5 * 3 + 1) = 2280

pool size (2,2) it's common choice.



a filter outputs only one Number

Batch

the output layer will have a dimension as the classes we want to classify


the MLP it's more dependent from image size
no weight sharing! (pooling and conv are)

**wide and deep** one of the input of the MLP can be an extra feature added by us
(age, image filters etc...)


### Pretrained models
#### Inception V3

predicted  
decode_prediction()

adam optimiser
