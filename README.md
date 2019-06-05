# Machine-Learning
A detailed guid into machine learning with python.

Note-A pre-requisite to taking this course will be a basic understanding of statistics and probability and fundamentals of Python. I will try to keep that math as simple as possible and will explain any tangents as we progress. 

## Before we dwell into machine learning let's start by understanding what machine learning essentially is.

  Machine learning is essentially trying to program a computer to perform tasks without explicitly having programed it to do so. This is acheived with help of algorithims and statistical modeling that help it solve problems by identifying patterns and making inferences. 
  This acheived by first writing an algorithm that trains itself of a large data set to idenity patterns within that data and then superimposing these patterns on a new data in question. 
  
## Now how to go about doing all that is stated above?

  To get have better intution and uderstanding of what we should be doing let's take into cosideration a hypothetical company Company X. Company X is very new to that market and started of this a IPO(initial public offering) of 1$. The share value of the company has been growing at a steady pase of 10$ every month. Now with the help of some simple linear alzebra we can easly model a graph or line that will best depict this growth. Now if we were to represent the above example in the form of a linear equation it would be Y = 10 * X + 1. We can now use this line to make predictions about the future share value of company X. Well in this case we will be able to exactly predict the share price of company X at every month but unfortunately real world senarions are not this forgiving. Thus we resort to making best possible predictions. This we term as linear regression. This is one of the fundaments of machine learning and this is going to be our entry point into machine learning.  
!(/images/yx10.png)
  
### So what is linear regression?

  From our above example I think we all now have a decent understanding of what linear regression is. It is simply **finding the best fit line** for a give set of data points and making predictions of of it for new incomming data.
  Here are the fundamental steps involved in linear regression: (We will be discussing every step in detail as we go ahead).
  1. Clean the data.
  2. Take a training set and isolate it from the test set.
  3. Train the algorithm on the training data and get the best fit line by minimizing the mean square error (or an estimator of your choice).
  4. Test the algorithims performance with the test data. 
  5 Use the algorithm to make future predictions.
  
