# Homework 4: Intro to Neural Networks

by Gerald I. Nakata

## Abstract

Neural Networks are the basis for modern machine learning, often being used interchangably even though they are not equivalent. In this assignment the feed forward neural network was explored. The structure was used to fit the data from HW1 as well as the MNIST data from HW3. The performance of the FFNN was compared against the previous fits for the HW1 data and the classifiers in HW3 for the MNIST data.


## Section I: Introduction and Overview

This assignment involved creating a Feed Forward Neural Network (FFNN) for the HW1 data and comparing the fit to the regressions in HW1. This is done with the first 20 data points being training data and the last 10 being testing data, and with the frist 10 being training and the last 10 being testing. The FFNN loss was then compared to the different regressions from HW1. After, an FFNN was made to classify the MNIST digit data and compared to the classifiers explored in HW3.


## Section II: Theoretical Background

FFNNs are the simplest type of neural networks since the flow of data is rather straightforward as the name suggests. The data is fed into an input layer which changes the data dimensions to match the first hidden layer, then keeps transforming the data until it reaches the output layer. The loss/error is then calculated, then backpropagation is utilized to modify the weights of the neural network and 'step' towards a lower loss/error.

While neural networks take little organized data to implement, they have a proclivity to overfit the data and require hyperparameter tuning as well as other methods to prevent such from happening.


## Section III: Algorithm Implementation and Development

The main new module used in this assignment was pytorch, including a few submodules. The torch.nn module allowed the streamlined creation of the neural network architecture and torch.optim simplified the application of backpropagation. The first FFNN was created to fit the data from HW1 so the input size and output sizes were 1 since it was a function. The hidden layer dimensions were both arbitrarily set to 10 for a total of 3 layers. The FFNN was rather simple with each layer feeding directly into each other without any activation functions between them. The two fits were then conducted, first with 20 training points, then with 10. The input and output data both needed to be reshaped to ensure that the matrix multiplication worked properly when inputted into the FFNN.

A different FFNN was then constructed for the classifying the MNIST data, this time using a Softmax activation at the end. This produces a probability distribution for each of the potential output classes, which is perfect for a classifier. 


## Section IV: Computational Results

Problem 1 of the homework applied the FFNN to the dat from HW1 using the last 10 data points as a test set and the first 20 and 10 as training sets. The FFNN results for the 20 train and 10 test sets are shown below:

![image](https://user-images.githubusercontent.com/6571263/236603637-ccb77481-421e-4413-8549-6d6315150deb.png)

And the 10 train and 10 test are the following:

![image](https://user-images.githubusercontent.com/6571263/236603944-d4c9b4af-70e1-436b-8411-0a329a3966db.png)

This showed that both FFNN fits to the HW1 data performed worse than even the worst HW1 regression, the 19th degree polynomial with 10 training points.

![image](https://user-images.githubusercontent.com/6571263/236604679-65f05fac-5c54-4335-b76f-2f9d7fb86e77.png)

This can likely be attributed to overfitting the data and a lack of hyperparameter tuning to find optimal results.

The second part of the assignment started with calculating the first 20 PCA modes which are as printed out along with their associated variance.

![image](https://user-images.githubusercontent.com/6571263/236605862-07c176a4-5a13-49b3-8217-bd2b6f450b4f.png)

The next section was using the FFNN architecture to create a classifier for the MNIST data used in HW3 which had the following accuracy:

![image](https://user-images.githubusercontent.com/6571263/236605923-d3297ad7-00e7-40cb-9d0a-27abf9af64ac.png)

Compared to the LSTM, SVM, and decision tree classifiers in HW3 the FFNN performed worse than all of them at 93.20% accuracy.

## Section V: Summary and Conclusions

This assignment introduced the neural network in the form of the FFNN and allowed us to experiment with it. While the neural network is very powerful, this particular assignment demonstrated its proclivity for overfitting data. While hyperparameter tuning can reduce the loss/error, there are other methods which can help, including data dropout, which will likely be explored at a later date.
