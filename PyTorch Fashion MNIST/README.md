# Fashion MNIST PyTorch Image Classification

* This project involves building a simple neural network to classify images from the Fashion MNIST dataset. The dataset contains 10 categories of clothing and accessories.

* I have used Pytorch for this project, and also this is with some of the **Regularisation techniques**.

### Regularisation techniques:
1. Data Augmentation

2. Batch Normalisation

3. Dropout

### Regularisation Tips:
* It is Always good to train a model without Regularisation first and get a baseline for the model.

* Next you can use Regularisation techniques in order or one by one to improve model performance.

## Model Architecture

1. **Convolution Layer 1**: 32 filters with a 3x3 kernel, followed by Batch Normalization and ReLU activation.
2. **Dropout**: A dropout layer with a probability of 0.2 to prevent overfitting.
3. **Convolution Layer 2**: 64 filters with a 3x3 kernel, followed by Batch Normalization and ReLU activation.
4. **Dropout**: Another dropout layer with a probability of 0.2.
5. **Max Pooling**: A 2x2 max-pooling layer to reduce the dimensionality.
6. **Flattening**: The output from the pooling layer is flattened into a 1D array.
7. **Fully Connected Layer 1**: A dense layer with 128 units and ReLU activation.
8. **Fully Connected Layer 2**: A dense layer with 10 units, outputting the final class scores.

The model is designed for multi-class classification with 10 output classes.
