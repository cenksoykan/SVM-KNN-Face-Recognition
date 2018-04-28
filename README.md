# Report

## Classification using PCA + 1NN with 5-fold cross validation

For PCA:

* Centerized the images
* Calculated Covariance matrix
* Calculated eigen values and eigen vectors
* Sorted the eigen values in descending order and then sorted the eigen vectors by the same index
* Took the first 70 principal components and plotted the data into new dimensions.

For 1NN:

* Calculated the euclidean distance for each test image with every train image
* Sorted the distance in ascending order and took the 1st one as the result
* Compare the result with original class and computed the accuracy

After the 5-fold cross validation, the average accuracy for **PCA + 1NN** was 96.75%

## Repeating Task 1 after resizing the images from 112 x 92 to 56 x 46

The average accuracy after **Resizing Images + PCA + 1NN** was 96.0%

Comparing this with the original dimensions accuracy, there does not seem to be much change in the accuracy.

## Classification using LDA + 1NN with 5-fold cross validation

For LDA:

* Calculated class wise mean vectors
* Calculated in-class scatter matrix
* Calculated between-class scatter matrix
* Calculated eigen values and eigen vectors
* Sorted the eigen values in descending order and then sorted the eigen vectors by the same index
* Took the first 70 principal components and plotted the data into new dimensions.

After the 5-fold cross validation, the average accuracy for **LDA + 1NN** was 96.0%

## Task 1: Classification using PCA + LDA + 1NN with 5-fold cross validation

After the 5-fold cross validation, the average accuracy for **PCA + LDA + 1NN** was 98.0%

Comparing this with previous results we can see that PCA before LDA helps increasing the accuracy of 1NN.

## Task 2: Classification using SVM with 5-fold cross validation

For SVM:

* Generated Gramian Matrix
* Calculated values of P, q, A, b, G, h and solved quadratic equation
* Determined support vectors
* Calculatied bias and weights
* Prediction was done using one-vs-rest approach

After the 5-fold cross validation, the average accuracy for **SVM** was 97.4%

## Task 3: Classification using PCA + SVM with 5-fold cross validation

After the 5-fold cross validation, the average accuracy for **PCA + SVM** was 92.7%

Comparing this with previous SVM results we can see that PCA decreases the accuracy of SVM drastically.

---

Answering the question whether KNN or SVM is more sensitive to high dimensionality of data.

**Answer:** SVM is more sensitive to high dimensionality as reducing the dimensions through PCA affects negatively to SVM, on the other hand PCA and LDA helps KNN to increase its accuracy with lower dimensions.

This is because PCA retrieves the features with highest information gain and discards the other, but SVM does not work feature wise, it relies on data-space dimensions which is reduced by PCA.
