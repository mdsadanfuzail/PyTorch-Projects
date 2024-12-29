# Movies-Recommendation-System


This project implements a Restricted Boltzmann Machine (RBM) using PyTorch to perform collaborative filtering for recommendation systems. It takes user-item interaction data and learns to reconstruct missing values in the user-item matrix for generating personalized recommendations. The model is trained using contrastive divergence with Gibbs sampling to update the weights.

This project demonstrates how to build an RBM for collaborative filtering using PyTorch, where the model learns hidden representations of users and items, enabling the prediction of missing values in the user-item matrix. The model is trained with training data and evaluated using test data to measure reconstruction error and accuracy.

## Model Architecture

The RBM architecture consists of the following components:

1. **Weight Matrix (W)**: A matrix of size `(nh, nv)` where `nh` is the number of hidden units and `nv` is the number of visible units (features).
2. **Bias for Hidden Layer (a)**: A bias vector of size `(1, nh)` for the hidden layer.
3. **Bias for Visible Layer (b)**: A bias vector of size `(1, nv)` for the visible layer.
4. **Sampling Hidden Layer (sample_h)**: 
   - Computes the activation as the matrix product of the visible layer and the weight matrix, added to the hidden bias.
   - Applies the sigmoid activation function to compute the hidden unit probabilities.
   - Samples hidden states using Bernoulli distribution.
5. **Sampling Visible Layer (sample_v)**:
   - Computes the activation as the matrix product of the hidden layer and the weight matrix, added to the visible bias.
   - Applies the sigmoid activation function to compute the visible unit probabilities.
   - Samples visible states using Bernoulli distribution.
6. **Training**:
   - The model is trained using contrastive divergence, where the weights are updated based on the difference between the positive and negative phase.
   - The weights are updated by computing the product of the visible and hidden unit activations during the training phase.
   - The model is trained over multiple epochs, using batches of data to optimize the reconstruction error.
7. **Testing**:
   - The model is tested by reconstructing the visible layer from the hidden layer and comparing the predicted values with the actual values in the test set.
   - The test loss and accuracy are computed based on the error between the reconstructed and actual values.

The model is used for collaborative filtering, generating personalized recommendations by learning hidden features of users and items.
