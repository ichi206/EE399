# Homework 6: Performance Analysis of Model Relative to Different Parameters

by Gerald I. Nakata

## Abstract

The given learning model was given to predict temperature at the ocean surface. Predictive models can be tested in a variety of ways, and in this instance a number of parameters were varied to test the viability of the given model.

## Section I: Introduction and Overview

This assignment involved varying parameters for the input data to test the resilience of the given model. The varied parameters were time lag, added noise, and the number of sensors of the input data to see if they impacted performance.

## Section II: Theoretical Background

The given model was an LSTM, which was defined in HW5 as follows:

Long short-term neural networks (LSTMs) are a type of RNN that have units composed of input gates, output gates, and forget gates which allow for information to be temporarily stored for better learning data.

This model is used to predict the surface temperature of the ocean at varying locations. The time lag variable impacts how far back data is given input data is for the model to predict from. The gaussian noise is simply added noise to the data. Finally, the number of sensors is how many different sensor locations are measured and given as input data.

## Section III: Algorithm Implementation and Development

The code for the model was given, so the only parts that need to be done were the different analyses. For these, the input data was modified in three separate ways: The changing of the time lag, the addition of Gaussian noise, and having a different number of sensors. The data was then run through the trained model to see how it performed as the variables were varied.

## Section IV: Computational Results

The graphs of the variable plotted against loss of the model are plotted below:

**Time Lag**

![image](https://github.com/ichi206/EE399/assets/6571263/f8990a91-4acf-4454-839a-617feb587eb9)

**Gaussian Noise**

![image](https://github.com/ichi206/EE399/assets/6571263/d0b9a5e1-bb9b-4fef-a9bd-47a8582c85d9)

**Number of Sensors**

![image](https://github.com/ichi206/EE399/assets/6571263/3b3589c6-fe1d-4ec8-a861-26b4136edb4b)


These graphs show a few different things. The increase in time lag increases the loss, likely due to the model not being trained to intake the data. The gaussian noise did not appear to impact the performance, maybe the range is not large enough for the noise to impact the model. Finally, the number of sensors did not appear to have any impact on the model's performance.

## Section V: Summary and Conclusions

This assignment explored how to apply different variable analyses to measure the performance of a learning model. It was also one of the largest data sets used, so the usage of Git LFS was needed in order to obtain the data set as well.
