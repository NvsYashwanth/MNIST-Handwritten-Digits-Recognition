# MNIST-Handwritten-Digits-Recognition
[![ForTheBadge built-with-love](http://ForTheBadge.com/images/badges/built-with-love.svg)](https://github.com/NvsYashwanth)

![](https://badgen.net/badge/Code/Python/blue?icon=https://simpleicons.org/icons/python.svg&labelColor=cyan&label)        ![](https://badgen.net/badge/Library/Pytorch/blue?icon=https://simpleicons.org/icons/pytorch.svg&labelColor=cyan&label)       ![](https://badgen.net/badge/Tools/pandas/blue?icon=https://simpleicons.org/icons/pandas.svg&labelColor=cyan&label)       ![](https://badgen.net/badge/Tools/numpy/blue?icon=https://upload.wikimedia.org/wikipedia/commons/1/1a/NumPy_logo.svg&labelColor=cyan&label)        ![](https://badgen.net/badge/Tools/matplotlib/blue?icon=https://upload.wikimedia.org/wikipedia/en/5/56/Matplotlib_logo.svg&labelColor=cyan&label)
## MNIST dataset

The `MNIST` database is available at http://yann.lecun.com/exdb/mnist/

The `MNIST` database is a dataset of handwritten digits. It has 60,000 training
samples, and 10,000 test samples. Each image is represented by 28x28 pixels, each
containing a value 0 - 255 with its grayscale value.

![](https://github.com/NvsYashwanth/MNIST-Handwritten-Digits-Recognition/blob/master/images/samples.png)

It is a subset of a larger set available from NIST.
The digits have been size-normalized and centered in a fixed-size image.

Thanks to Yann LeCun, Corinna Cortes, Christopher J.C. Burges.


## Results
***`A validation dataset of size 12,000 was deduced from the Training dataset with its size being changed to 48,000. We train the following models for 20 epochs.`***

***Model - 1 : FCNN***
* This `Linear Model` uses 784 nodes at input layer, 512, 256 nodes in the first and second hidden layers respectively, with ouput layer of 10 nodes (10 classes).
* The test accuracy is ***98%*** (***This result uses dropout probability of 20%***)
* A  `FNet_model.pth` file has been included. With this one can directly load the model state_dict and use for testing.

***Model - 2 : CNN***
* The `Convolutional Neural Netowork` has 2 convolution layers and pooling layers with 3 fully connected layers. The first convolution layer takes in a channel of dimension 1 since the images are grayscaled. The kernel size is chosen to be of size 3x3 with stride of 1. The output of this convolution is set to 16 channels which means it will extract 16 feature maps using 16 kernels. We pad the image with a padding size of 1 so that the input and output dimensions are same. The output dimension at this layer will be 16 x 28 x 28. The we apply RelU activation to it followed by a max-pooling layer with kernel size of 2 and stride 2. This down-samples the feature maps to dimension of 16 x 14 x 14.
* The second convolution layer will have an input channel size of 16. We choose an output channel size to be 32 which means it will extract 32 feature maps. The kernel size for this layer is 3 with stride 1. We again use a padding size of 1 so that the input and output dimension remain the same. The output dimension at this layer will be 32 x 14 x 14. We then follow up it with a RelU activation and a max-pooling layer with kernel of size 2 and stride 2. This down-samples the feature maps to dimension of 32 x 7 x 7.
* Finally, 3 fully connected layers are used. We will pass a flattened version of the feature maps to the first fully connected layer. The fully connected layers have 1568 nodes at input layer, 128, 64 nodes in the first and second hidden layers respectively, with ouput layer of 10 nodes (10 classes). So we have two fully connected layers of size 1568 x 128 followed up by 128 x 64 and 64 x 10.
* The test accuracy is ***99%*** (***This result uses dropout probability of 20%***)
* A `convNet_model.pth` file has been included. With this one can directly load the model state_dict and use for testing.
