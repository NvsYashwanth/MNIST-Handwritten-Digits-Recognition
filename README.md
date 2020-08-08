# MNIST-Handwritten-Digits-Recognition
## MNIST dataset

The MNIST database is available at http://yann.lecun.com/exdb/mnist/

The MNIST database is a dataset of handwritten digits. It has 60,000 training
samples, and 10,000 test samples. Each image is represented by 28x28 pixels, each
containing a value 0 - 255 with its grayscale value.







A validation dataset of size 12,000 was deduced from the Training dataset with its size being changed to 48,000. This linear model uses 784 nodes (image pixels) at input layer, 512, 256 nodes in the first and second hidden layer, with the ouput layer of 10 nodes each for a class. A "model.pt" file has been included. With this one can directly load the model state_dict and use for testing. With a dropout probability of 20%, this model achieves 98% overall accuracy.
