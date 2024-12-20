## Image Descriptors with SIFT and Bag of Words

The purpose of the practical work was to produce an algorithm able to classify images using visual descriptors.

In order to do so we proceeded by steps, the first being the realization of a SIFT descriptor for each
16x16 pixel patch of each picture contained in the dataset 12-Scenes.
The first tool presented throughout the Practical Work was the Scale-Invariant Feature Transform
(SIFT) - which is a local descriptor widely used in Image Classification as it is a feature extraction
method that is invariant to scale and orientation of the images and robust to fluctuations of illumination, noise and minor viewpoint changes in the images.

Among the key-points in the computation of the SIFT descriptor the first one is to calculate the gradient of each pixel composing the patch selected.

After having then computed the weighted gradient using a Gaussian mask and discretizing the orientation of the gradient to 8 possible values (having 0 for the NORTH direction, 1 for NORTH-EAST, and so on), it is possible to build a histogram of the gradients for each region. 

The histograms can
finally be concatenated to compose the SIFT descriptor of the patch.

The second step of the practical work was to compute a Visual Dictionary, so that it is possible to
find frequent patterns and patches with similar SIFT descriptors can be grouped together. In order
to solve this problem we used a K-Means algorithm, determining K centers of the SIFT space and
minimizing the distance from the actual SIFTs.
The final step of this first practical work was to obtain a numerical representation of each image, so
that it can be easily classified. To do so we used a Bag of Words (BoW) algorithm, with which we
were able to summarize all the local SIFT descriptors of the image into a global descriptor, with the
help of the visual dictionary.