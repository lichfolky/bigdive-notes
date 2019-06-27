## Natural Language Processing

**Francesco Tarasconi** Data scientist

> **CELI, H-FARM**
+ NLP (text and voice)
+ Data science services

**Keywords:**
+ Computational modeling and modeling
+ Computational linguist
+ Knowledge engineer
+ Democratization
+ Data fusion
+ Natural Language Questions
+ Semantic technology (extract semantics from text)

## Why ML
At the beginning it was **cognitive simulation**
> Automate things and replace humans

Now we are more interested in **Narrow AI**: commercially viable smart systems
> Tell the machine to do selective tasks

There's not free lunch and sometimes there are only partial solutions. technology as support not a complete substitute

## Choose the right approach

**data analytics new need**

Predictive analytics: *what will happen*

Prescriptive: *what should we do?*

### ML Architectures

**Rule-based Systems**

deterministic and logical, enumerable rules and explicit solution
if you miss data this is the only way `ES: chatbots`

the data scientist specifies **tasks** and select **models templates**

Output is determined by inference but it's not explainable

**Convolutional neural networks** and **ConvNet**

convolution layer, convolution + max pooling, multiple convolution layers

> the Connectionists model

Backpropagation + Gradient Descent

take batches of data, use them to tune the parameter of the model

**Reinforced Learning**

**Supervised ML**

**Random Forests**

**Recurrent Neural Networks**

**Deep Reinforced Learning**

Model the environment:

In simulated environment the algorithm learns by itself
`Es: AlphaGo played with itself`

### Data fusion
you can use different data sources, but:
- *evaluate* quality
- *select* the most impactful
- *fill-in* spacial and temporal gaps
- *add* key additional information

> **Anomalies in time series**
>
> Weather forecast can improve sales forecast accuracy by about 5%
>
> Goldstein scale, monitors geopolitical stability: Extreme events, can't be predicted but the can be automatically detected (monitoring with social media)

### Speech Synthesis
the same intent can be expressed in *different ways* and can be *ambiguous*.
add Pragmatic compriation `it's hot in here -> turn on conditioner`

**Conversational agents**

**Dialogflow management systems** manage conversation ('what did you say')

**Agent fulfillment**
battery of classification models
rules + probabilistic hybrid

**Computer vision**
Success based on Convolutional Neural Network
`Captioning`

## Practical NLP
### Tools
#### Text normalization
correct mistakes, normalize spelling variants, text encoding, format inconsistencies

#### Morphological analysis
identification and description of morphemes (units of meaning)

it returns all the potential interpretation of each word
disambiguation component: choose the only correct interpretation

#### Named entity recognition
identification of names and assign them in categories

#other tools
- sentiment analysis, opinion mining
- Topic Finding and Cluster analysis
- Automatic Classification (intent or kind of msg)

### Process

**Documents** as a **vector space model**
vector containing number of occurrences of each word

> ['e', 'ciao', 'cane', 're', 'o', ...]
>
> [ 0 ,  1 , 0 , 1, 0, 0, 0, 0, 0, ...]

**Word embeddings**: we need to move a sparse matrix to a reduced and dense dimension

*the dream*: reason through algebra `king - man + woman = queen`

most of the word embedding it m through Neural Network:
create a model that predict the a word in a position of the sentence
but after you use take the layers to solve the word embedding

**shallow method** latent semantic analysis. Use matrix and no more layers. a-parametric compress data

**latent dirichlet allocation** probabilistic model.
parametric: distribution of topics
very popular technology for small sample data. (remove easily noise)

#### Pre-training word embedding (Word2Vec)
**Corpora** large repository of Documents

train a model on large corpora for the chosen language -> the resulting embedding can be used of any downstream tasks

**continuous bag-of-words (CBOW)** and **skip-gram**

customizable you can add features

**WORD2VEC** (a .csv file) are shared by a lot of companies

#### Scale-up Pre-training and transfer learning (BERT)
Stanford challenges: BERT it's on top in a lot of different tasks.
you can tune it for you task
you can build a service that use it.

sequence to sequence prediction (used in gmail)
