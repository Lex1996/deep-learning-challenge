# Deep Learning Model for Charity Success Prediction

## Overview of the Analysis

The purpose of this analysis is to build a deep learning model that predicts whether charitable organizations will be successful based on various input features. The goal is to create a model that can assist in identifying organizations most likely to receive funding, thus optimizing the allocation of resources.

## Target and Features

* Target Variable: The target variable for the model is IS_SUCCESSFUL, which indicates whether a charitable organization was successful (1) or not (0) in obtaining funding.

* Features: The following variables are used as features for the model:

    * APPLICATION_TYPE: The type of application submitted by the organization.
    * AFFILIATION: The type of affiliation the organization has.
    * CLASSIFICATION: The classification of the organization.
    * USE_CASE: The primary use case for the funding.
    * ORGANIZATION: The type of organization.
    * INCOME_AMT: The income amount of the organization.
    * SPECIAL_CONSIDERATIONS: Whether there are any special considerations for the organization.
    * ASK_AMT: The amount of funding requested by the organization.

* Removal of Variables

    * The EIN and NAME columns were removed from the input data as they are neither targets nor features.

## Compiling, Training, and Evaluating the Model

### Model Architecture

* The deep neural network model was designed with two hidden layers:

    * First Hidden Layer: 72 neurons with ReLU activation function.
    * Second Hidden Layer: 20 neurons with ReLU activation function.

* The output layer consists of a single neuron with a sigmoid activation function, which is suitable for binary classification tasks.

### Model Compilation

The model was compiled using the Adam optimizer with a learning rate of 0.0002.
The loss function used is binary cross-entropy, appropriate for binary classification.
The accuracy metric was used for model evaluation.

### Model Training

* Three attempts were made to train the model with varying numbers of epochs and batch sizes.
* In the first attempt, the model was trained for 20 epochs with a batch size of 32.
* In the second attempt, the model was trained for 20 epochs with a batch size of 70.
* In the third attempt, the model was trained for 25 epochs with a batch size of 85.

### Model Performance

* Attempt 1:
    Accuracy on training data: 73.36%
    Accuracy on testing data: 72.96%

* Attempt 2:
    Accuracy on training data: 73.61%
    Accuracy on testing data: 73.03%

* Attempt 3:
    Accuracy on training data: 74.14%
    Accuracy on testing data: 72.85%

The model performance did not achieve the target accuracy of 75% or above. Despite adjusting the number of epochs and batch sizes, the model's performance remained below the target threshold.

## Summary

In summary, the deep learning model developed for predicting the success of charitable organizations did not meet the target accuracy of 75% or above in any of the three attempts. This suggests that the model may not be effectively capturing the complex relationships within the data.