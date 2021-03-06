## Loss functions
Emprical loss: total loss over entire dataset
Cross Entropy loss: use for models that output a probaility between 0 and 1
Mean Squared Error loss: use for regression models that output continuous real numbers

## Loss optimization
argmin of losses
argmax of log losses

## learning rate
Too low, can be stuck in local minimum
Too high, overshooting and diverge

## How to find the perfect learning rate:
Constant learning rate, binray search, test and try
Adaptive learning rates: increase or decrease while training
	SGD / not adaptive
	Adam, Adadelta, Adagrad, RMSProp / adaptive


## batching
size of 1: Too noisy 
Entire dataset: computationally expensive
Middle Ground: mini batch 
	Advantage: Faster, More accurate estimation of gradient, Smoother convergence, allow for larger learning rates because you can trust the steps with less noises. Parrallel computings with batches

## Models fittingness
Underfitting < Ideal fit < overfitting
Overfitting memorizing data, ideal fit generalizations.

## Regularization Techniques
Discourage our model to learn complex ideas, because we want generalization to test data.

## Technique 1 Dropout: 
drop some of the neurons in hidden layers to 0 or activation level to zero. Can't build memorization channel to the neuron. 50% memo 50% forgot. Genralize better.
## Technique 2 Early Stopping: 
Initially, the test and training data accuracy both increases. If the model overfits to the training data, the test data accuracy will decrease. So find the model when the test data accuracy went down, that is our ideal model.  
