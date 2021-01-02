# Convolutional Autoencoder Project

The aim of this project is to develop a convolutional autoencoder for imagens. <br/>
The encoder part of the model will be used later in a model to clusterize images.

## About the Project

The models were developed in Python using Keras.<br/>
The models were validated using 5-folds cross-validation and all of them were tested on the same dataset.<br/>
As examples, we trained the autoencoder with 2 datasets: CIFAR-10 and MNIST.

## About the Training
In both examples, the models were trained with backpropagation using Adam  algorithm.<br/>
The training was performed for 100 epochs with batch size = 32.<br/>
The loss used while training the model with CIFAR-10 was a combination of mean squared error and cosine similarity (multiplied by minus 1). And the loss used while training the model with MNIST was the mean squared error.


## Models

The models consist of some blocks of convolutional, activation and batch normalization layers and blocks of fully connected (dense) layers. The output of the encoder part of model trained with the CIFAR-10 dataset is an array with size 128x1. The autoencoder trained with the MNIST dataset was a little changed, so that the output size of encoder part could have the same size as the numeber of known classes of this dataset (that is, an array of size 10x1).<br/>
For shrinking and increasing the height and width of the data throughout the model it was used max pooling and up sampling with nearest neighbour interpolation, respectively. All the convolutions were made using same padding.  <br/>
The figures below show the models developed and the legend that explains what each layer is.<br/>
In the image, the data flows from the left to the right. This way, the left grey box represents the original image and the right grey box representes the reconstructed one. 

#### Model trained with MNIST dataset

![model flowchart - mnist](https://user-images.githubusercontent.com/58445878/103463149-0cd0ff80-4d09-11eb-8957-a0079d98d89e.png)

#### Model trained with CIFAR-10 dataset

![model flowchart - cifar10](https://user-images.githubusercontent.com/58445878/103463163-1fe3cf80-4d09-11eb-9375-a5f42160ac97.png)

#### Legend

<img src="https://user-images.githubusercontent.com/58445878/103463169-2b36fb00-4d09-11eb-80e9-b5bff48420d7.png" width="600">
