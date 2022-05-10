name : confusion matrix
tags : 
backlinks : 
source : #HOML

###### Content:
A confusion matrix is a way to measure the performance of a classifier. The general idea is to count the number of times instances of class A are classified as class B, instead of properly being classified as class A. In a confusion matrix, the columns represent the predicted [[classification]], while the rows represent the actual [[classification]].

In the example below, there is a classifier that can classify data as either belonging to class A, B, C, or D. Comparing the predictions made by the model on a set of data with the actual labels for the data, you can construct a confusion matrix.

|     | A   | B   | C   | D   |
| --- | --- | --- | --- | --- |
| A   | 103 | 24  | 15  | 0   |
| B   | 12  | 122 | 20  | 11  |
| C   | 0   | 2   | 116 | 20  |
| D   | 12  | 10  | 5   | 100 |

So if we wanted to see the number of class A data that the model predicted to belong to class B, you look at row 1, column 2 of the matrix.

###### Properties:


###### Additional Thoughts:
