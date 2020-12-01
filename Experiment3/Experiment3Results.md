#Experiment 3 

We use 2 different optimizers for our neural networks trainingd and traingdm

## Trainingd

This is optimizer that uses gradient descent which uses backpropagation to calculate the derivates of the performance which the default is cross entropy.
Backpropagation calculate the derivates of perf with respect to the weight and biases of the network. 

It uses the formula : dX = lr * dperf/dX 
where lr is the learning rate 

Training for this algorithm stops when either:
•	Max epoch is reached
•	Time is exceeded
•	Performance (cross entropy is minimized)
•	Performance gradient is below the minimum gradient(see default below)

Please note that these default parameters of traingd were used in the experiment 
net.trainParam.lr             0.1         Learnign rate
net.trainParam.min.grad       1e-5        Maximum prefomracne gradient
net.trainParam.time           inf         Maximum time to train in seconds

## Trainingdm

This is similar to the previous method however it also accounts for the previous change in weight/bias to the equation as momentum combat the problem of local minima
Backpropagation is used to calculate derivatives of performance perf with respect to the weight and bias variables X. 

dX = mc*dXprev + lr*(1-mc)*dperf/dX

where dXprev is the previous change to the weight or bias and mc is the momentum constant.

Here are the default parameters we use for this training function
net.trainParam.lr	        0.01	      Learning rate
net.trainParam.mc	        0.9       	Momentum constant
net.trainParam.min_grad	  1e-5	      Minimum performance gradient
net.trainParam.time	      inf	        Maximum time to train in seconds

## Result
Overall gradient descent performed marginally better than gradient descent with momentum at node and epoch 32 however at lower node and epoch combination  gradient descent performed marginally worse. However this could be due to the learning rate and momentum constant parameters not being optimized
