# Chapter 1

## page 54 - questionnaire

### 1. Do you need these for deep learning

lots of math - false

lots of data - true

lots of expensive computers - false

a Phd - false

### 2. Name five areas where deep learning is now best tool in the world

image recognition/classification

image segmentation (is that the same)

NLP - sentiment, chat bot

time series prediction, weather prediction

game theory - go


### 3.  what was first device based on neuron

perceptron

### 4. what are the reqs for parallel distributed networks

my answers borrowed from [Stanford PDP paper](https://stanford.edu/~jlmcc/papers/PDP/Chapter2.pdf "Stanford PDP paper")


A set of processing units

A state of activation

An output function for each unit

A pattern of connectivity among units

A propagation rule for propagating patterns of activities through
the network of connectivities

An activation rule for combining the inputs impinging on a unit
with the current state of that unit to produce a new level of
activation for the unit.

A learning rule whereby patterns of connectivity are modified by
experience

An environment within which the system must operate

### 5. What were the 2 theoretical misunderstandings that held back the field of NN

one layer NN were too big and slow to be useful, the addition of layers was needed but hat only became the normal practice within the last decade, due to better hardware and data availability

### 6. What is a GPU
video card, cuda + nvida = better ML perfromance thgan cpu

### 7. run 1+1 in notebook , result 2


### 8 run the chapters notebook and guess output - done

###  9.  complete the jupyter notebook at https://oreil.ly/9uPZe
done

### 10. why is it hard for trad comp programs to recognize photos?
too many cases to program against

### 11. what did samuel mean by weight assigmment

model parameters in todays world.  weights today are the specific parameters, sgd back propagated to the layers as they learn and tune the model to get it more accurate

### 12. what term do we use today for his "weights"
see 11

### 13.
draw a picture of samuels model

training model

inputs  >->|
           |>-> model >-> results >-> performance >->|
weights >->|                                         |
    |<----------------------------------------------<|


trained model

inputs >-> model >-> results

### 14. why is it hard to understand how a ML model works
the ansers to why are buried in the layers and the weights


### 15. whast the name of the theorum that shows a Nn can solve any prob to any accuracy?

universal approximation theorum

### 16.  what do you need in order to train a model
labelled data split into train data, validation data and test data

### 17.  feedback loop in policing model

if the model predicts where there will be more arrests, and the popo focus sending more police to that area, then it is likely even more arrests will hapepen there , bias feedback loop activate

### 18.  do you always have to use 224X224 images with cat recognition
nope.  its a legacy standard, it gives good performance(speed) but not hard fast rule

### 19.  classification v regression
you calssify items that can be labelled.  good/bad, cat/dog, will live/will die
you use regression for data that has range, not label.
house prices, temperature

### 20. validation v test set
train set = the data we train the model on

validation set = we compare training set to this set during model optimization, try to get the best results.

test set - after model is complete, this is the true test, truly unseen data.  if you contracted someone to build you a model, this can tell you how well they really did as long as you kept it for yourself.

### 21. how does fastai handle validation set

it defaults to .20 if you forget to specify

### 22. does random sample always work for validation set
nope.  if you have thousands of pictures, of say 5 people doing a task

a random sample of those pictures would likely include all 5 people

you really want to exlude a person so you can validate agaisnt truly unseen data.  stratify across people, hold out an entire person


same for time series, you dont randomly pull out data points for validation, instead you would probably use the last n records, and see if the model can predict the known future well.


### 23.  overfitting
training a model aggressively on one set of data so that it cannot predict unseen data with any accuracy

### 24. metric vs loss

metric is how well our model performs, suitable for human consumption

loss tells the model how far away from the answer it is, it will be used by the model to adjust the weights

loss function is not always suitable for a humans to use as a metric.

### 25.  pretrained models

image classification as an example, a good pretrained model already learned the base layers, edges, circles, gradients, we just substitue in the head, the speicifics that we are training for and much faster way to build your final model

pretrained models have thw weights baked in, so instead of fit, we fine_tune thus preserving the original models weights.


### 26. head

the app specific portion of the model, the final layer(s)



### 28. early CNN layers vs later layers
early - edges, gradients
later - shapes, cats, dogs

### 29. image models used for only photos?

nope.  turn anything into an image and start classifying, many example of turning other data into an image
mouse clicks
sound waves
executable binaries

### 30. what is an architecture
the physical layering of the CNN
one layer with 10 nodes?
5 layers with varying nodes
fully connected layuers
etc

### 31. y_range
when trying to regress things that have a top and bottom range
sentiment analysis, how many rotten tomatos 0-5 or how many stars 0-10 depending on the full range of the data

### 32.  hyper parameters

used to control the ml process, unlike weights, they are derived during the training process to get the modcel closer to the best result.

### 33. best way to avoid failure in an org

hold back a truly unseen test set to be used to validate the final version of the model.

be sure the test set is just a random sampling as in the cases mentioned in #22



Further Research

### 1. Why GPU, GPU v CPU

CPU has very limited number of cores
GPU has many many cores

GPUs are bandwidth optimized, CPUs are latency optimized

NVidia CUDA runs on the GPU for optimized ML

GPU will use more power than a CPU so for very small tasks the CPU would be the better choice, to optimize power consumption


## 2. feedback loops in ML



the policing example, in 17

youtube video recomendation engine - if youtube recommends videos only on number oif views then the copnspiracy theorists typically watch more videos that anyone else, it will promote those vides more.  the more they are recomended, the more they get watched, feedback loop activate

stock brockerage app, tells me what stock is being purchased the most today, so i buy that stock, fear of missing out, fomo, activate















