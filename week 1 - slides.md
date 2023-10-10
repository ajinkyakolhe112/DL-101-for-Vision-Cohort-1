# Week 1 - Slides
---
<details>
  <summary>Agenda</summary>

## Agenda

### Agenda - Week 1
1. Learn "Simplified Neural Network", end to end
2. Class Problem: Image classification on Simple Data (mnist)
3. Assignment Problem: Image classification on bit more Complex Data (cifar10)
4. Class Ranking: Kaggle Leaderboard & Huggingface Leaderboard

### Agenda - Week 2
1. Learn "Neural Network", end to end. parametric experiments & experiment tracking
2. Class Problem: Image classification on Bit more Complex Data (cifar10)
3. Assignment Problem: Image classification accuracy on Complex Data (imagenet-100 & 1k). Just attempting
4. Assignment Problem: Push accuracy of CIFAR10 / Innovate on. with parametric experiments

### Agenda - Week 3
1. In Class attempting: imagenet 100 & 1k & attempting innovate
    3. Experiment via training_script. arg parser
    4. One batch & time to overfit num_classes batch
2. Building testing functions for essential functions. mastery of shape & kernel sizes,out_size calculation. neurons
3. Class Problem: Image Classification on 1k
4. Existing architectures, CNNs & their principals

### Agenda - Week 4 
1. Transfer Learning
3. Learning Rate Policies, Activation Functions etc. Hyper-parameter optimization (cifar10 & imgnet 100)
2. Experiment via yaml config
3. Comming Next: LLM or Classification -> Segmentation -> Others

</details>

---

## Types of Intelligence
1. No Intelligence      - 
1. Narrow Intelligence  - One Task
1. General Intelligence - Multiple Tasks
1. Super Intelligence   - More tasks than possible by Single Human

**Journey of Intelligence**. From smallest, to however higher we can push. 
A powerful tool & new problems which could be solved with that tool. 


---

## Economical Value & Complexity of Intelligence
1. Complexity & Value of Standing Up
2. Value of Understanding a Word
3. Value of Understanding a Picture
4. Value of Driving

Value lies in things which are easy for us but very hard for computers. Data which our senses process via our brain.

"comment": value of calculus

---
## Biological Intelligence. Basis. Neurons & Connections

Coolest facts about brain. 
Brain -> *Connections* -> *Network*
(Mylenation -> Brain Fold Happening
Rats have clean brain. )

Brain *learns* via multiple ways. Mirror neurons, reflection, stories, experience. They all speed up our learning. 
A -> Apple. Takes around 10 to 100 different apples to learn. 


---
## Artifcial Intelligence Basis: Neurons
Artificial Intelligence Basis. Neuron & Connections. learning rate is just one simplest of learning way. 
They are slow, take a lot of compute power. But they are valuable. 
---
## Simulating first Intelligence - Artificially

```python
dataset_for_training, dataset_for_validation = get_datasets()
model = Attempt1_Model()
error_func = ""
optimizer = torch.optim.Adam([], lr=0.01)

for example in dataset_for_training:
  y_predicted = model.predict(example)
  y_actual    = god.predict(example)
  
  loss = error_func(example)
  optimizer.zero_gradient()
  loss.backward()
  For param in model.parameters():
    param = param - param * gradient
```

"comment" brute force reducing of error. results in learning. even if we don't know.

---
## Why Go through so much trouble. Artificially intelligence ?

1. Flexibility. Vision vs Artificial Vision
2. Generalizability. Any Data, anything. (GPT)
4. Huge number of low hanging fruits.. ladder length has increased. 
3. Improvement has one independent amplifier. Data Volume
4. Improvement has one independent amplifier. Hardware Power / Model Capacity as UFA


### Data: Any . Model: Any Data
Data => Any Data
Model => Universal Function Approximation

Any = Sun's Energy, Molecules Protein, Electrons in a Battery, 
AI as GPT. 
Excel as GPT. Used for any & every situation. a General skill. 
---


## **Model in Detail as Data Transformer**
1. Model = 
    2. Group of Blocks
    3. Group of Layers
    4. Group of Neurons
 
----
```python
feature_extractor = nn.Sequential( # build a function which returns model built from list of channels.
  nn.Conv2d(1,50,3),
  nn.ReLU(),
  nn.BatchNorm2d(50),
  
  nn.Conv2d(1,50,3),
  nn.ReLU(),
  nn.BatchNorm2d(50),
  

)
decision_maker = nn.Sequential(
  nn.Linear(500,50)
  nn.Linear(50,10)
)
model = nn.Sequential(
  feature_extractor,
  decision_maker
)
y_predicted_logits = model(example)
y_predicted_probs  = nn.functional.softmax(y_predicted_logits)

```

---
```python
model.parameters_analysis()
```

---
## Cost or Value of a Single Parameter
Value of Intelligence
Cost of Parameter in Training vs in Predicting
Forward Pass of Big Models. Training a big model from huggingface. Real demo
Value in Reducing Parameters



<comment> homework. innovation in improving accuracy or reducing parameters or better understanding architecture.
---
EVERY IMPROVEMENT IN ACCURACY than before, is a valuable addition.
Because its a nascent field. Uncharted & Unexplored Area. 

If you can improve, you can produce value. Then you are very valuable in this time. # difference audience
If you want to solve big problem, DL is a fundamentally powerful tool which will help you. # different audience

---
## **Dataset** in Detail. as Tensor Matrix

---
## **Model in Detail** (Just Forward Pass & Layer by Layer)
CNN & Linear Model
Weights & Vector Size. Maths Multiplication

y = f(X,W)

---

## **Error Function & Backward Pass**

Chain Rule

---
## **Dataset**
Diamentions of Single Example
BCHW & B,Features

**DATA**. Learning from Data... As long as we have enough data, we can learn from it. 
torch.tensor is the Datatype for Data

Analogy. 
Science Exam. Physics. 
You can study textbook. Understand physics. Or
You get past 20 years question papers. You figure out & reverse engineer from the answers. You will get the marks, you would not have understood it, but you will be able to get the marks. 
Those marks are accuracy score. 

*Generalization* IMP POINT. KEY POINT OF NEURAL NETWORKS. Because we are learning from the answers, we have to check if it's generalised. 
---

## **Loss & Accuracy Curve**
Custom Dataset to realize impact of Accuracy
1. CIFAR10 Classes + (Human, Child Label)
2. Report misclassified / killed as consequence of inaccuracy

---
## **Model Training & Gradient Descent**
& Monitoring training progress

---

https://playground.tensorflow.org/#activation=relu&batchSize=10&dataset=circle&regDataset=reg-plane&learningRate=0.03&regularizationRate=0&noise=0&networkShape=3,3&seed=0.00044&showTestData=false&discretize=false&percTrainData=50&x=true&y=true&xTimesY=false&xSquared=false&ySquared=false&cosX=false&sinX=false&cosY=false&sinY=false&collectStats=false&problem=classification&initZero=false&hideText=false&noise_hide=true&regularization_hide=true&batchSize_hide=true&regularizationRate_hide=true&percTrainData_hide=true&showTestData_hide=false

---
1. Data is available
2. Model is to be written incrementally not remembered. 
    3. You could use ready made model
   4. You need to understand principal of building a good model. & process too

---
**Pythonic Code Philosophy**
- Easiest to read code & understand. Smallest complications