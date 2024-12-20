## Domain adaptation

A big problem when training neural network is the difficulty of obtaining correctly labeled data. Domain adaptation tries to approach this problem by training on a labeled source set while simultaneously
also being able to perform well on a similar target set of unlabeled data. The network consists of three
parts, a feature extractor, a label predictor and a domain classifier. The feature extractor, as the
name suggests extracts features from the input images, and then label predictor is trained to predict
the labels of the labeled set. The most important part of the network, which allows the processing
of unlabeled data is the domain classifier - its job is to say if a sample belongs to the labeled source
domain or the unlabeled target domain. In order to do the classification for both sets we want the
feature extractor to learn features that generalize well which means that the domain classifier can’t
distinguish between the two sets. That also means we want to maximize the loss with regard to the
domain classifier. This is done by reversing the gradients in the gradient reversal layer which sits
between the feature extractor and the domain classifier.

The goal of this exercise was to implement this DANN network, as described above.


