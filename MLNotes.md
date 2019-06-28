## Machine learning - *Going Data-Driven*

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

Gathering (Visualize) -> Labelling (Classify)  
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
time dependent, unsynchronized
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

### NN
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

reinforce weights for each

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

always dubt about the results:  
also the random trainset selection can be an not optimal one!
