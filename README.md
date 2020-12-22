# Convolutional Autoencoder Project

The aim of this project is to develop a convolutional autoencoder to be applied in imagens.
The encoder part of the model will be used later in a model to clusterize images.

## About the Project

The model was developed in Python using Keras.
The model was validated using 5-folds cross-validation and all of them were tested on the same dataset.
As examples, we trained this autoencoder with 2 datasets: CIFAR-10 and MNIST.

### About the Training
In both examples, the models were trained with backpropagation using Adam  algorithm.
The training was performed for 70 epochs with batch size = 32.
The loss used was a combination of mean squared error and cosine similarity (multiplied by minus 1).


### Model

The figures below show the model used and the legend explaining what each layer is.

![model flowchart](https://user-images.githubusercontent.com/58445878/102850823-0e412480-43f9-11eb-81c9-42ce921fde79.png)


<img src="https://user-images.githubusercontent.com/58445878/102835649-0de36200-43d6-11eb-942d-0f447fe3c021.png" width="600">
