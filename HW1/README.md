# HW1: Basic Machine Learning Data Fit

by Gerald I. Nakata

# Abstract

Introductory assigment to machine learning in Python to create line fits and visualizing data space to locate error funtion minima.


# Section I: Introduction and Overview

This assignment involved creating function fits for a given data set. 
![image](https://user-images.githubusercontent.com/6571263/231073290-d02bb567-3a5c-44fd-b613-243040f9a86e.png)

This includes a linear, cosine, parabolic, and 19th degree polynomial fits. The fits were constructed with both all of the data, the first 20 values to train and the last 10 to test, and the first 10 to train and the last 10 to test. 


# Section II: Theoretical Background

A few Python modules were used including numpy (for basic array algebra), matplotlib.pyplot to graph data, and scipy.optimize to make the fit equations.


# Section III: Algorithm Implementation and Development

The implementation was rather straightforward, making the regression equation and using scipy to minimize error. For the cosine implementation the starting coefficients were modified to try and get a better minima.


# Section IV: Computational Results

The following graphs are regressions and a heatmat from the assignment and labelled accordingly. (Note, the 19th Deg Polynomials have a very large y-axis)

Cosine Regression:
![image](https://user-images.githubusercontent.com/6571263/231073885-60dba6ca-907a-4865-b39b-ebd61661c675.png)


Cosine Regression, Fixing C and D, Sweeping A and B Coefficients:
![image](https://user-images.githubusercontent.com/6571263/231074379-2fbe60d9-ea1b-4f6f-91f7-a73d88449ce7.png)

Note, there are 6 distinct minima, potentially 8 visible.


20 Train/10 Test Linear Regression:

![image](https://user-images.githubusercontent.com/6571263/231075067-19e9d721-2034-4454-a192-997d95d73247.png)


20 Train/10 Test Parabolic Regression:

![image](https://user-images.githubusercontent.com/6571263/231075242-40a18f05-1e16-4874-8911-5521888391ac.png)


20 Train/10 Test 19th Deg Polynomial Regression:

![image](https://user-images.githubusercontent.com/6571263/231075458-3ea2c5bb-c438-4d29-987a-a6b50dcd0e5d.png)


10 Train/10 Test Linear Regression:

![image](https://user-images.githubusercontent.com/6571263/231076394-8fdcb283-eaeb-4163-b20e-858c7599f3ce.png)


10 Train/10 Test Parabolic Regression:

![image](https://user-images.githubusercontent.com/6571263/231077024-a6176051-caad-4721-ba64-be170700192b.png)


10 Train/10 Test 19th Deg Polynomial Regression:

![image](https://user-images.githubusercontent.com/6571263/231077092-7fa24bae-b6e4-48e2-96c4-db04b287a4e6.png)



# Section V: Summary and Conclusions

This assignment was an exploration of the Python tools for basic fits and introductory machine learning. The part ii data, with the error heatmap showed that existance of multiple minima that could be hit when attempting to find a regression to reduce error. 
