
# Simple CNN for Image Classification

* This project implements a Convolutional Neural Network (CNN) using TensorFlow and Keras to classify images as either cats or dogs. It uses image data preprocessing techniques to augment the dataset and builds a CNN model to train, validate, and make predictions on unseen data.

* This project demonstrates how to build a CNN for binary image classification using the TensorFlow and Keras libraries. The model is trained to classify images as either **cat** or **dog**, and the dataset is preprocessed using `ImageDataGenerator` for real-time data augmentation.



## Dataset

The dataset used is a subset of the [Kaggle Dogs vs. Cats dataset](https://www.kaggle.com/c/dogs-vs-cats/data), consisting of images of cats and dogs in separate folders for training and testing.

- **Training set**: 10,000 images of cats and dogs (5000 each).
- **Test set**: 2,500 images (1250 each for cats and dogs).


## Model Architecture

The CNN architecture consists of the following layers:
1. **Convolution Layer**: 32 filters with 3x3 kernel and ReLU activation.
2. **Max Pooling**: 2x2 pooling layer to reduce the dimensionality.
3. **Second Convolution Layer**: Another Conv2D layer with 32 filters and MaxPooling.
4. **Flattening**: Convert the pooled feature maps into a 1D array.
5. **Dense Layer**: A fully connected layer with 128 units and ReLU activation.
6. **Output Layer**: A single neuron with sigmoid activation for binary classification.

## Training and Evaluation

1. Compile the model using the Adam optimizer and binary cross-entropy loss:
    ```python
    cnn.compile(optimizer='adam', loss='binary_crossentropy', metrics=['accuracy'])
    ```

2. Train the CNN on the training data and validate on the test data:
    ```python
    cnn.fit(training_set, validation_data=test_set, epochs=25)
    ```