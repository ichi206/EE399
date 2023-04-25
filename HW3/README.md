# Homework 3: SVD Interpretations and Classifiers

by Gerald I. Nakata

## Abstract

Classifiers are the algorithimic approach to identifying certain groups a data point may belong to based on input data. In this assigment different Linear Classifiers were used to categorize MNIST data. The different matrices of Singular Value Decompositon were explored as well to ensure our understanding of what each matrix represents.

## Section I: Introduction and Overview

This assigment involved the processing of MNIST data using SVD to create a 3D plot representation that showed the liklihood of each digit image data being one of the three digits set as the axes. Linear Decomposition Analysis (LDA) was performed for a classifier between 3 digits, then three different classifiers (LDA, Support Vector Machine (SVM), and Decision Trees (DT)) were utilized to differentiate between two different digit combinations.

## Section II: Theoretical Background

SVD is one concept utilized in this assignment which allows for the decomposition of any matrix into three principal parts. From a purely mathmatical perspective, the matrices, U, Sigma, and V.t, are components of a matrix transformation. U is the matrix which contains the eigenvectors of the columns of the input (A*A.t) matrix (as columns) and V.t contains the the input matrix row eigenvectors as rows (for V it would have the row eigenvectors as columns). Sigma is a diagonal matrix containing the eigenvalues corresponding to each eigenvector. Functionally, the matrix U aligns the data so that the eigenvectors are on top of the axes, the Sigma matrix scales the data, and the V.t matrix rotates the data back from eigenspace into 'real space'.

The different types of classifiers used in this assignment are LDA, SVM, and DTs.

Linear Discriminant Analysis, LDA, attempts to reduce the dimensionality of data to maximize the separation in the end classification and is rather similar to the way SVD functions.

Support Vector Machines, SVMs, seeks hyperplanes that optimally split data into different groups based on what the label is. This can include some complex functions for the hyperplane to separate complex data.

Decision Trees, DTs, are the last method explored in this assignment. Functionally, lines are progressively drawn to separate groups further towards a complete split. While this is similar to SVMs, the split is more simple, but cannot handle as complex of data as easily as SVMs.

## Section III: Algorithm Implementation and Development

A few new modules were utilized in this assigment, including sklearn's train_test_split to separate MNIST data into training and test sets (note that all of the data was split with 80% for training and 20% for testing), accuracy_score and classification_report to see how different classifiers performed, LogisticRegression was used to model the LDA classifier, SVC for the SVMs, and DecisionTreeClassifier for the decision trees. A few issues were encountered whilst programming for this assignment, notable, when creating the nested for loops, an error that only one class was being used for the target data set. The issue was eventually found to be that when using the nested for loops there was no check to see if the two digits being compared were the same digit, so a check had to be added to mitigate the issue. This issue was fixed by adding print statements for which numbers were being compared, and an error message that ChatGPT recommended as an internal catch for if the same digit was passed to the functions.

## Section IV: Computational Results

The SVD of the digit images was completed and the singular value spectrum was found to have size (784,). This should be a diagonal matrix of these values to be functionally used as part of the SVD. It was also found that around 100 modes created a relatively clear image reconstruction. Fewer could be used but it would blur the edges of the digit.

![image](https://user-images.githubusercontent.com/6571263/234189159-5befafaf-75d0-46c0-8a3e-1e7eb1b6431e.png)

For the interpretations of the SVD matrices, the U matrix can be seen as the relationship between each input image pixel to the overall pattern of the image, while the Sigma matrix is the scaling factor that shows how prominent these pixel patterns are relative to each other. The V matrix (transpose of V.t component) represents the relation of each of the images to the pixel data weight based on pattern, which has a transpose that can be used as the last step in reconstructing the images.

The last of the SVD work was the 3D plot of 3 V-modes colored based on digit label, in this case modes 2, 3, and 5.

![image](https://user-images.githubusercontent.com/6571263/234190404-d02e6cf5-10bc-49f7-9928-1c74c47af57b.png)

The next section was classifiers. The two digit classifier data will be shown later since it was run to compare each digit combination.
For the three digit classifier (using LDA), the results are as shown below.

![image](https://user-images.githubusercontent.com/6571263/234190801-1c361c81-100f-4cb1-a067-eeedda0d2814.png)

To find which two digits were the most easy and two most difficult to separate each digit combination was run and the accuracy of the models were compared.

![image](https://user-images.githubusercontent.com/6571263/234191507-ce25b8c3-76f4-4d19-b323-9706f0eff4da.png)
![image](https://user-images.githubusercontent.com/6571263/234191584-f7d2db8c-163a-44d5-a1a9-f12024a38968.png)
![image](https://user-images.githubusercontent.com/6571263/234191650-ece3b209-4ce0-4a1e-bbed-719c176fc710.png)
![image](https://user-images.githubusercontent.com/6571263/234191728-91c34fb7-4052-45b2-85d5-560fc3233d87.png)
![image](https://user-images.githubusercontent.com/6571263/234191800-53e762aa-9399-4e12-b85f-ba3263851efc.png)
![image](https://user-images.githubusercontent.com/6571263/234191892-6c357ff0-bcc6-420d-a6be-9d1aa17912cf.png)
![image](https://user-images.githubusercontent.com/6571263/234191962-467375ad-032e-4748-be65-3daf5cc7643d.png)
![image](https://user-images.githubusercontent.com/6571263/234192013-6ea52bd3-72ff-4a9c-a99b-234ba979da9c.png)
![image](https://user-images.githubusercontent.com/6571263/234192107-edef0b67-7b9c-4ccf-9df9-178cb439502d.png)
![image](https://user-images.githubusercontent.com/6571263/234192236-c1d84117-1063-4480-9b1b-20ce1cd493f1.png)

The highest classifier accuracy was determined as the most easy to separate digits, in this case 6 and 7.
Classifier accuracy between digit 6 and 7 : 0.9996471418489767

Likewise, the lowest classifier accuracy was determined to be the most difficult to separate digits, in this case 3 and 5.
Classifier accuracy between digit 3 and 5 : 0.9516908212560387

For the last section SVMs, LDAs, and DTs are compared against each other as classifiers. They all perform rather comparable to each other, with some doing better at classifying some digit combinations than others. Unfortunately, at the SVM comparing 2 and 3, so I can only show data up to that point.

![image](https://user-images.githubusercontent.com/6571263/234193703-209319c7-188d-4a4a-88df-7e533e55ab66.png)
![image](https://user-images.githubusercontent.com/6571263/234193786-af077260-a1f7-4206-a5bd-be7e8693eba1.png)
![image](https://user-images.githubusercontent.com/6571263/234193861-10379fba-5721-48bc-9993-e6377deba3f7.png)
![image](https://user-images.githubusercontent.com/6571263/234194032-aeb4355d-8570-47de-b072-c71f6dbf2060.png)

Based solely on this data:

SVMs performent the worst at separating 1 and 8, and best at separating 0 and 1
SVM Classifier accuracy between digit 1 and 8 : 0.9785787147228834
SVM Classifier accuracy between digit 0 and 1 : 0.9996617050067659

Decision trees performed the worst at separating 0 and 6, and best at separating 0 and 1
Decision Tree Classifier accuracy between digit 0 and 6 : 0.9782293178519593
Decision Tree Classifier accuracy between digit 0 and 1 : 0.9979702300405954

## Section V: Summary and Conclusions

This assignment explored the understanding behind SVD as well as three different types of classifiers that can be utilized for supervised machine learning along with their associated Python libraries. This was also the first time utilizing data split for cross validation in an assignment thus far, and is an important part of ensuring the integrity of the models produced. 
