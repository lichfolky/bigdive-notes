## From image classification to semantic segmentation

**Object localisation** > image classification  
Where in the image it's the object (bounding box)
1 Class one
**Object detection**  
multiple object instance with label and box  
**Semantic segmentation**  
multiple objects with label and segmentation (contour)  
**Instance segmentation**  
add multiple instances  


## Segmentation

(4, 2, 1) channels

all the network we saw before worked like a funnel

1 dimensional layer of classes as output.

**balanced dataset**: if we have an equal representation of classes.

rare disease: better to classify an healthy guy ill than the opposite

take random patches from images to check if there's information

> python generator
> use yield
> like lazy evaluation


```
print(x_tst.shape, y_tst.shape)
(200, 160, 160, 8) (200, 160, 160, 10)

input
200 items
160 * 160 patch dimensions
8 channels
----
output
200 items
160 * 160 patch dimensions
10 classes
```

## U network
contraction path
extraction path

with no padding you loose a little information in the borders

the size vo copy and crop doesn't match, so we crop a part of the image and we use it as an input for the opposite layer

**UpConvolution**  
upConv 2x2
```
1 4        1 1 4 4  
5 6   =>   1 1 4 4  
           5 5 6 6  
           5 5 6 6  
```

standard for segmentation
jaccard coefficient for validation


**Generators**
generators are very convenient, we can't build the entire training set but we can generate it

method fit_generator instead of fit  
(put the parenthesis! in the first argument)


fully convolutional NN we don't have dense layers


segmentation it's pixel level classification

we need epochs to have data points to visualize a training curve

std training set 200 images
  batch sizes of 20
  steps_per_epoch 10

steps_per_epoch


every row it's a class:
classification, predition, binary predition (0.5>)
(threshold)


Without the dense layers you need the
last layer as convolution(1,1) fully connected
to map the final classes

subplot funcion starts with 1...

## Transfer Learning

One trick for Deep convolutional NN that works wery well in many domains.

Deep learning it's totally data driven.

I have a network with a trained class and I need to classify another class.

You don't have to start from scratch, the visual features of the old network.

We could use the pre-trained net as a feature extractor,
and append a model to the features network.

We don't care about dense layers features correlation.

We will need to fine tuning the last layers, and meaby
let the back-propagation adjust a little more the features extraction (ex the last layer of the convolutional part).

we can have very little data!

Classification, after the flattening layer = avg_pool

Data augmentation

t-SNE
t-Distributed Stochastic Neighbor Embedding
unsupervised learning algorithm
tca?

include_Top = False give me only the features extraction!

Fine Tuning
layer.trainable = True / False

GlobalAveragePooling2D reduce features a litte more than pooling
