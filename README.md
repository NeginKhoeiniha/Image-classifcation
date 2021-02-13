# Intro-to-Tensorflow
This is a step by step introduction to Tensorflow

## First:
The very first step, what is called "Hello World" in programming, is the notebook "The Hello World". Very basic yet fundamental! The data used in this notebook is quite simple, predicting the corresponding value for a sample namber in an arrey.

## Second:
For the next step, we tried loading a dataset from keras, fashion MNIST, and trying a bigger neural network as well. At the end, we did a little prediction too. The instructions are commented.

## Third:
This step is actually the second step with a little improvment which has a big effect. We added two layers of convolution, each followed by a maxpooling layer. There is also a class which makes the model stop training when reaches a certain accuracy.

##Fourth
On the fourth step, we set up data generators that will read pictures in our source folders, convert them to float32 tensors, and feed them (with their labels) to our network. We'll have one generator for the training images and one for the validation images. Our generators will yield batches of images of size 300x300 and their labels (binary).

As you may already know, data that goes into neural networks should usually be normalized in some way to make it more amenable to processing by the network. (It is uncommon to feed raw pixels into a convnet.) In our case, we will preprocess our images by normalizing the pixel values to be in the [0, 1] range (originally all values are in the [0, 255] range).

In Keras this can be done via the keras.preprocessing.image.ImageDataGenerator class using the rescale parameter. This ImageDataGenerator class allows you to instantiate generators of augmented image batches (and their labels) via .flow(data, labels) or .flow_from_directory(directory). These generators can then be used with the Keras model methods that accept data generators as inputs: fit, evaluate_generator, and predict_generator.
