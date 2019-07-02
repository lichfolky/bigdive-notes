# ML Intro

Classic examples of DL:
+ semantic segmentation image reconstruction
+ speech recognition
+ image annotation
+ face recognition

![boo](https://blog.dataiku.com/hs-fs/hubfs/Top%20Prediction%20Algorithms.jpg?width=1368&height=1936&name=Top%20Prediction%20Algorithms.jpg)

**Classical error:**
thinking that most complex the model is, the better is for my data


>decision tree one by one take the sample the other tree got wrong and augment weight

### Dataset

X = (N samples, DFeatures)  
y = (N number or labels)    

### Feature Engineering

Documents => X    

### Model Validation

learning model
we want to find the **target function**
we try to approximate it with a **hypothesis function**

**Score function**
you compare target and hypothesis functions
> es accuracy, confusion matrix  

$\frac{TP +TN}{TP + TN + FP + FN}$

**accuracy** $\frac{TP +TN}{TP + TN + FP + FN}$

**precision** TP / (TP + FP)
negative are not so important  
**recall** TP / (TP + FN)  
**F1**  (2 * precision * recall)/(precision + recall)


### Class probability

vector (classification, probability)

### The learning model

**input** X  
**output** y  
**target function** f : X -> Y  

**data:** (x1,y1),..(x_n,y_n)  
**hypothesis** g : X -> Y  

#### The REAL: Learning Model
**learning Algorithm** A  
**hypotesis set** H = {h}    g in H (set of candidate formulas)

#### final result
**final hypotesis** g ~= h

```
for the single perceptron:
...
h(x) = sign(w^t x)

take sign(w^t xn) != yn
and update the weight vector:
w <- w + yn xn
```

-**E_in(g)** train error or in-sample error  
-**E_out(g)** validation error or out-sample error (difficult to measure)

 **Approximation problem**
can we make Ein(g) small enough

**Generalization problem**
can we make sure that eout(g) is close enough Ein(g)

`BOOK: learning from data a short course`
### Learning Theory

Questions to consider:
+ Do you have enough data?
+ Is the model too simple?
+ What is the best strategy to reduce error or increase performance


Can a model generalize better?
+ Collect more sample
+ Collect more features
+ Change Model

### is learning feasible?


>  hoeffding's Inequality


h(x) = f(x) green
h(x) != f(x) red

...

M # hypotesis

the more it's complex the model ....

> vladimir vapnik  
> alexey chervonenkis

we are trying to approssimate the g to the target function

### Part 2

$P[|E_{in}(g) - E_{out}|>\epsilon] < 2Me^{-2\epsilon^2N}$

**dichotomy** a binary labelling of $\chi$

**hypotehesis** $h :\chi \rightarrow \{-1, +1\}$

number to hypothesis can be infinite $|H|$  
number of dichotomies $|H(x_1,x_2,..., x_N)|$ is at most $2^N$

**the growth function**

counts the most dichotomies on any N points

**the break points**

**shatter** produce all $2^k$ dichotomies


> hypothesis set: $sign(w^+x)$

we replace the M with the growth function

we can learn only if the growth function it's polinomial!

**Decision tree**

if you don't give a limitation to the decision tree you will not generalize

**the VC dimension**

The hypothesis set h is said to shatter a set S\C X
shattare realase all 2^N possibilities

the larges number of n  
the most points h can shatter

k os a break point for h

k > $d_{vc}(H)$

$d_{vc}(H)$ is finite => g /in generalize


degree of freedom

\#of parameters analog degrees of freedom  
$d_vc$ equivalente 'binary' degreees of


expected error

in sample error growth the e_out decrease

**Validation Curve**
```
generalization error
training error

in relation on model complexity


OVERFITTING<>OVERFITTING

```
##### Estimanting $E_{out}$

out of sample error is estimated via validation

the more data point the closer to $E_{out}$

###Validation Techniques

##### train test splice
##### K-cross validation

n validations, with a piece big #Datapoint/n
after avg of them

##### Leave one out cross validation

 we feep a single sample for validations
n-1 to fit the model

#### model bias on learning curve

graph with data and generalization e


the hyperparameters control the degree of liberty

```
The rocket

Data is fuel
The rocket it's fuel
```

#### Regularization

linear regression with regularization
you can impose limits to the choice of parameters
adding limitations


### EX


`model = LinearRegression(normalize=True, fit_intercept=False)`
fit_intercept deve passare dallo zero

hyperparameters:  
normalize=True,  
fit_intercept=False

parameters, you cant't choose them they are choosen by the Algorithm:  
model.coef_
model.intercept_


>model.predict([[3], [4], [2000]])  

for each row, predict a target


X_fit.ravel() = X_fit.flatten()


#### Coefficient of Determination $R^2$

[https://en.wikipedia.org/wiki/Coefficient_of_determination](https://en.wikipedia.org/wiki/Coefficient_of_determination)


## Part 3

Batch size

gradient descend

Test loss 0.509 % points we get wrong (1 - accuracy)

every perceptron has a bias, it's like a different weight  
$biasInput = 1*w_b$.

**learning rate**

start with a medium learning rate (it should't diverge)
after you decrease it.

the gradient it's always upwards.  
(It's calcuated with a partial differentiation: $G = ∂J(W)/∂W$ )

update weights: $W = W - ηG$

[exercise](https://playground.tensorflow.org)
