# Convolutional Autoencoder Project

The aim of this project is to develop a convolutional autoencoder for imagens. <br/>
The encoder part of the model will be used later in a model to clusterize images.

## About the Project

The model was developed in Python using Keras.<br/>
The model was validated using 5-folds cross-validation and all of them were tested on the same dataset.<br/>
As examples, we trained this autoencoder with 2 datasets: CIFAR-10 and MNIST.

### About the Training
In both examples, the models were trained with backpropagation using Adam  algorithm.<br/>
The training was performed for 70 epochs with batch size = 32.<br/>
The loss used was a combination of mean squared error and cosine similarity (multiplied by minus 1).


### Model

The model consists of some blocks of convolutional, activation and batch normalization layers and blocks of fully connected (dense) layers.<br/>
For shrinking and increasing the height and width of the data throughout the model it was used max pooling and up sampling with nearest neighbour interpolation, respectively. All the convolutions were made using same padding.  <br/>
The figures below show the model developed and the legend that explains what each layer is.<br/>
In the image, the data flows from the left to the right. This way, the left grey box represents the original image and the right grey box representes the reconstructed one. 

![model flowchart](https://user-images.githubusercontent.com/58445878/102850823-0e412480-43f9-11eb-81c9-42ce921fde79.png)


<img src="https://user-images.githubusercontent.com/58445878/102851095-afc87600-43f9-11eb-8917-9fbd92b913a7.png" width="600">

