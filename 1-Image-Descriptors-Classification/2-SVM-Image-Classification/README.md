## SVM 

In project 1, we built a processing pipeline that transformed an RGB image into a compact
representation that is more suited to image classification. Now, each image is encoded as a BoW vector
describing in some way the presence (or absence) of p = 1000 patterns in the image. The vector of the i-th
image, thus, is xi ∈ Rp.

Moreover, we know that each image can belong to one of 15 categories from our
dataset. Therefore in this session, we will build the ultimate part of the pipeline, an image classifier that will
take as input the BoW vector. A lot of different machine learning models can be used at that point, and
we will use the popular SVM (Support Vector Machine).