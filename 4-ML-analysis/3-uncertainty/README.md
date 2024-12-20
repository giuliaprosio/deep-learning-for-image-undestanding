## Uncertainty applications

The purpose of this work is estimating uncertainty for predictions our models do. In the first part we
tried to qualitatively evaluate the most uncertain images in our test set. To do that we built a leNet-5
style network with dropout layers in order to implement Monte-Carlo dropout variational inference.
We used three different mesures to compute the uncertanity of samples, those are variation-ratios,
entropy and mutual information.
The second part deals with failure prediction, which means predicting if the network is doing a misclassification on the current sample. In order to do that, a ConfidNet is used which consists of two parts,
the normal classification part and a second network, the confidence net which is trained seperatly. Its
job is to predict if the classification network is failing to predict a correct class.
The last part of this course dealt with detecting if an input sample is outside the distribution the
network was trained on.
