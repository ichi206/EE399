# Homework 2: Correlation Matrices and SVD of Face Data

by Gerald I. Nakata

## Abstract

Correlation matrices and Singular Value Decomposition (SVD) are two separate methods of interpreting facial data and capturing the relationships between different faces. Both approaches are utilized in this assignment to visualize the matrix representations in Python and to further familiarize us with the different Python functions availabel to streamline any machine learning implementations.

## Section I: Introduction and Overview

This assignment involved the processing of face data (the 'yalefaces.mat' file) using two different methods. The construction of a correlation matrix and the usage of Singular Value Decomposition (SVD) to get a matrix representation of face data.

## Section II: Theoretical Background

The correlation matrix is the covariance matrix over the product of the standard deviations of the rows and columns. This matrix measures how correlated the facial data at different indices are. The second method, SVD, where the inputted matrix is decomposed into three separate matrices, U, the matrix of normalized eigenvectors from X dotted with X.T (where X is the input matrix), V, the matrix of normalized eigenvectors from X.t dotted with X, and S, the diagonal matrix filled with the square root of eigenvalues from U or V.

## Section III: Algorithm Implementation and Development

A few different modules were used for this were in numpy for matrix algebra. For the correlation matrices, numpy.corrcoeff(input_matrix) was utilized with the input matrix being the sub matrices asked for in the problems. For SVD, luckily there is a function to easily process matrices, np.linalg.svd(input_matrix), so most of the matrix algebra was handled by numpy functions.

## Section IV: Computational Results

a) This section creates the correlation matrix of the first 100 faces and plots it to visualize the relationships between the face data
![image](https://user-images.githubusercontent.com/6571263/232965389-883770bd-09a9-45a4-80d6-a5a6a783187f.png)

b) Using the correlation matrix from the previous section, the indices of the two most correlated faces and the two least correlated faces were found and plotted from the original dataset.
![image](https://user-images.githubusercontent.com/6571263/232965624-5fc62d7f-b1e1-4bdb-85e6-757ce1a5eabc.png)

c) Part a was repeated, but for the 10 faces at indices [1,313,512,5,2400,113,1024,87,314,2005]
![image](https://user-images.githubusercontent.com/6571263/232968339-468a6ef9-0402-43d8-8eac-0845301ecbcb.png)

d) The matrix Y was created from dotting X with X.T and the six eigenvectors corresponding to the six largest eigenvalues were determined.
![image](https://user-images.githubusercontent.com/6571263/232966185-daf2485e-d782-4837-9dcf-2d03eef50f89.png)

e) The SVD for input matrix X was found and the six principal component directions were determined.
![image](https://user-images.githubusercontent.com/6571263/232966373-aa7d8230-a40a-45d8-947b-8bf8782c9312.png)

f) The first eigenvector and the first SVD mode were compared by getting the euclidean distance between them.
![image](https://user-images.githubusercontent.com/6571263/232967296-64c997b2-f2cd-4bcf-8bec-77181f46ae5c.png)

g) The percentage variance captured by each of the 6 SVD modes were printed and the modes were plotted.
![image](https://user-images.githubusercontent.com/6571263/232967462-8d9d4139-4d7d-4d47-90cd-f958fdbe2295.png)

## Section V: Summary and Conclusions

This assignment further explored the Python tools that can be utilized for basic machine learning and the different visualizations that can be utilized, in this assignment it was pcolor. The preexisting Python functions, such as for SVD, streamline much of processing for the facial data and make finding relationships easier. 
