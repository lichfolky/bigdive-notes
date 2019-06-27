# I-react
Resilience

*Awareness* for *Risk Management*:
Prevent disasters using **risk forecasts** and **early warning**

Sources:
+ Earth observations
+ Forecast models
+ Human generated data

Data driven system.

Tweet classification using **NLP** and **Deep Learning**


##### Social Monitoring Module
- Classification
- Environment Recognition
- Social Monitoring
- Sentiment analysis

##### Event Detection Module

anomaly detection
automatic event detection: the civil protection is notified from the system of an anomaly

##### es: named entity Recognition

text2numbers

**Social media data**

data enhanced with geonames opensource namedEntities dataset

we will use a recurrent neural network

we remove punctuation and we lowercase each msg
the position it's a token position

ML Task:
BIO annotation
beginning intermediate outside

the rows are more because you can have more entities for each
### Subtasks
#### data generation

**tuple** multidimensional matrix

build a vocabulary:
  + one entry for word

<pad> to discriminate useful data

#### dataloading

Dataloader:
feeds a tensor to the networ

read sentenced in dataset and convert in sequence of indices using the volaboulary

**Libs for NPL**
Pytorch
NLTK
SPACY

#### batches
data is provided in batches, not all in the same time.
the nn input layer has a fixed size.
Each token is a single input, insert <pad> if the sentence it's shorter.
We feed the network 1 sentence at time.

#### model fitting and evaluation


### Review model
evaluate the model with confusion matrix
snippet to talk to the model


https://cs230-stanford.github.io/pytorch-nlp.html
