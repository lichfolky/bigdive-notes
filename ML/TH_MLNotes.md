# ML Intro


![bo](Images\Top Prediction Algorithms.jpg)

Classic examples of DL:
+ semantic segmentation image reconstruction
+ speech recognition
+ image annotation
+ face recognition

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
