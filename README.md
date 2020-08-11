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
* A validation dataset of size 12,000 was deduced from the Training dataset with its size being changed to 48,000.
* This linear model uses 784 nodes at input layer, 512, 256 nodes in the first and second hidden layers respectively, with ouput layer of 10 nodes (10 classes).
* The test accuracy is ***98%*** (***This result uses dropout probability of 20%***)
* A "model.pt" file has been included. With this one can directly load the model state_dict and use for testing.
