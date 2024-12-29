
# Simple CNN for Image Classification

* This project implements a Convolutional Neural Network (CNN) using TensorFlow and Keras to classify images as either cats or dogs. It uses image data preprocessing techniques to augment the dataset and builds a CNN model to train, validate, and make predictions on unseen data.

* This project demonstrates how to build a CNN for binary image classification using the TensorFlow and Keras libraries. The model is trained to classify images as either **cat** or **dog**, and the dataset is preprocessed using `ImageDataGenerator` for real-time data augmentation.

## Model Architecture

The CNN architecture consists of the following layers:
1. **Convolution Layer**: 32 filters with 3x3 kernel and ReLU activation.
2. **Max Pooling**: 2x2 pooling layer to reduce the dimensionality.
3. **Second Convolution Layer**: Another Conv2D layer with 32 filters and MaxPooling.
4. **Flattening**: Convert the pooled feature maps into a 1D array.
5. **Dense Layer**: A fully connected layer with 128 units and ReLU activation.
6. **Output Layer**: A single neuron with sigmoid activation for binary classification.