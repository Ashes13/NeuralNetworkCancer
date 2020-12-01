# Creating neural networks for a cancer diagnosis using Matlab

## Executive Summary

This report is for showing the findings of understanding how to use neural networks to classify classes for cancer as either malignant or benign. There are 3 experiments used to optimize the neural network. It uses the patternnet network from MATLAB toolkit and each experiment looks at updating methods of updating the neural network to see the effect on the classification error rate. The test train split for all experiments was 50:50 with no validation set. The dataset was provided by Matlab

### Experiment 2 

The aim of experiment 1 is to find the optimal hidden layers (nodes)and epoch iterations by testing different node and epoch combinations. 3 node sizes are tested which are 2, 8 and 32. Then for each node the Neural networks(NNs) were tested at different epoch iterations, which were  [ 4 8 16 32 64]. Therefore 15 combinations of epoch and nodes were trained and tested. The classification error rate at each epoch and node combinations were noted. Each combination was also ran 30 times and the error rate was averaged. The error rate was averaged and graphed to analyze and derive the best node and epoch combination.

### Experiment 2

For the second experiment, the node and epoch combinations derived form Experiment 1 was used to build and ensemble of neural network classifiers, with different weights initialized for each classifier. These classifiers all predicted the cancer classes. Then a majority vote system was implemented to identify the classification on the test dataset from the ensemble networks. The accuracy was noted down (1 – classification error rate) and was compared against the average accuracy of each of the individual classifiers. Different odd numbers of ensemble sizes were tested which at 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25 . Each ensemble size was repeated 30 times. The average accuracy from the majority vote system and the single classifiers for the different ensemble sizes were noted down and graphed.
This was also repeated with lower and higher nodes and epochs combinations.


### Experiment 3
For the third experiment  the training function was changed from traincsg to traingd and traingdm. Which were optimizers using grading descent and gradient decent with momentum. They both performed worse than traincsg. This is likely due to learning rate and momentum constant parameters not being optimized. however traingd performed better with classifiers set to  node 32 and epoch 32, with traingdm performing better at lower node and epoch combinations. 



