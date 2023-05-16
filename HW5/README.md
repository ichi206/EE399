# Homework 5: Comparing Different Neural Networks by Predicting Lorenz Equation

by Gerald I. Nakata

## Abstract

As stated in the previous homework, neural networks are the the basis of modern machine learning. In this assignment different types of neural network architecture are used to make predictions on future values of the Lorenz function.

## Section I: Introduction and Overview

This assignment involved creating a feed-forward neural network (FFNN), a long short-term memory neural network (LSTM), a recurrent neural network (RNN), and an echo state network (ESN) to make predictions on the future states of a lorenz function. The networks were trained at predictions p = 10, 28, and 40 and then tested at p = 17 and 35.

## Section II: Theoretical Background

The different types of neural networks explored in this assignment were listed in Section I and will be further explained here with the exception of FFNNs which were explained in HW4.

Long short-term neural networks (LSTMs) are a type of RNN that have units composed of input gates, output gates, and forget gates which allow for information to be temporarily stored for better learning data.

Recurrent neural networks (RNNs) are a type of neural network that can have nodes connected in loops to allow for node weights to impact past nodes. This framework is good for predictive modeling of functions.

Echo state networks (ESNs) are another type of RNN that have a 'reservoir' of neurons which have connections and weights randomly assigned and the only weights modified are the ones connecting hidden neurons to outputs.

## Section III: Algorithm Implementation and Development

Keras was the main library used in implenting these neural networks with data derived from the given lorenz equation. Each model was fit to training data with values 10, 28, and 40 steps forward and were trained for 50 epochs each. The general format was adapted from HW4 with the input and output dimensions changed, as well as some architecture modifications to change it from a classifier to a predictive model. The ESN was a bit more difficult to implement and chatGPT was used to create the architecture. Each of the models were tested for their accuracy at predicting 17 and 35 steps ahead.

## Section IV: Computational Results

For the FFNN the accuracy was surprisingly high, possibly due to lucky hyperparameterization.

**FFNN, p = 10, 28, and 40

![image](https://github.com/ichi206/EE399/assets/6571263/054cb985-f9bd-4254-a031-df24281bb696)

The FFNN function was also plotted onto the given lorenz graph to better see the aberrations from the function.

**FFNN Projected over Lorenz

![image](https://github.com/ichi206/EE399/assets/6571263/ac6b66fc-a2d7-40d6-b6de-7fd3628e60d4)

Then, the accuracy for the model was tested at 17 and 35 steps ahead.

**FFNN, p = 17 and 35

![image](https://github.com/ichi206/EE399/assets/6571263/5e62dea7-cc85-40e5-8989-43e7b2280743)


This was repeated for the LSTM.

**LSTM, p = 10, 28, and 40

![image](https://github.com/ichi206/EE399/assets/6571263/743e2b4b-e0f6-4a6c-ac6e-78f558bf870d)

**LSTM Projected over Lorenz

![image](https://github.com/ichi206/EE399/assets/6571263/4dd06b2a-2125-430c-8fac-2aa26d69bf7e)

**LSTM, p = 17 and 35

![image](https://github.com/ichi206/EE399/assets/6571263/10d4f6ce-4cc2-4f85-9de9-afc7512ca389)

The RNN as well.

**RNN, p = 10, 28, and 40

![image](https://github.com/ichi206/EE399/assets/6571263/354a3f1b-ec42-4195-8979-9bc5dece2191)

**RNN Projected over Lorenz

![image](https://github.com/ichi206/EE399/assets/6571263/e11dcac2-1472-4111-9769-6e26e75177b7)

**RNN, p = 17 and 35

![image](https://github.com/ichi206/EE399/assets/6571263/2b54d00d-6d2f-4e9a-9c13-7d47399f6792)

And finally, the ESN.

**ESN, p = 10, 28, and 40

![image](https://github.com/ichi206/EE399/assets/6571263/a574c63a-2fb0-4dfe-a584-87a284702e75)

**ESN Projected over Lorenz

![image](https://github.com/ichi206/EE399/assets/6571263/c1fe89e6-54a1-46da-a4fd-91970b6618a5)

**ESN, p = 17 and 35

![image](https://github.com/ichi206/EE399/assets/6571263/4a658b9f-1667-44d3-a41a-8cb056cf79cb)

## Section V: Summary and Conclusions

This assignment explored several new neural networks and the predictive capabilities of each of the new frameworks. The accuracy for each of the networks were oddly high considering how difficult it should be to predict future data for a function as erratic as lorenz. A causes could be very lucky hyperparameterization, or not using diverse enough of a dataset and thus making the data too easy to fit to.
