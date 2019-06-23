# Machine-Learning
A detailed guid into machine learning with python.

Note-A pre-requisite to understanding the below content will be a basic statistics and probability, also fundamentals of Python. I will try to keep that math simple and will explain any tangents as we progress. 

## Before we dwell into machine learning, let's start by understanding what machine learning essentially is.

  Machine learning is essentially trying to program a computer to perform tasks without explicitly having programed it to do so. This is acheived with help of algorithims and statistical modeling that help it solve problems by identifying patterns and making inferences. 
  This acheived by first writing an algorithm that trains itself of a large data set to idenity patterns within that data and then superimposing these patterns on a new data in question. 
  
## Now how to go about doing all that is stated above?

  To get have better intution and uderstanding of what we should be doing let's take into cosideration a hypothetical company Company X. Company X is very new to that market and started of this a IPO(initial public offering) of 1$. The share value of the company has been growing at a steady pase of 10$ every month. Now with the help of some simple linear alzebra we can easly model a graph or line that will best depict this growth. Now if we were to represent the above example in the form of a linear equation it would be Y = 10 * X + 1. We can now use this line to make predictions about the future share value of company X. Well in this case we will be able to exactly predict the share price of company X at every month but unfortunately real world senarions are not this forgiving. Thus we resort to making best possible predictions. This we term as linear regression. This is one of the fundaments of machine learning and this is going to be our entry point into machine learning.  
![alt text](images/yx10.png)
  
### So what is linear regression?

  From our above example I think we all now have a decent understanding of what linear regression is. It is simply **finding the best fit line** for a give set of data points and making predictions of of it for new incomming data.
  Here are the fundamental steps involved in linear regression: (We will be discussing every step in detail as we go ahead).
  1. Clean the data.
  2. Take a training set and isolate it from the test set.
  3. Train the algorithm on the training data and get the best fit line by minimizing the mean square error (or an estimator of your choice).
  4. Test the algorithims performance with the test data. 
  5 Use the algorithm to make future predictions.
  
The best way to learn anything is through hands on experience. So we are now going to impliment the above steps on a data set. For this purpose we are going to create random data points and draw a regression line on them. 

#### Step 1: create data.
  Create random points. You can use the random function for this or just create list of random points. In this case let the points be:
  [[2,3], [3,5], [1.2], [8,9], [7,8]].
#### Step 2: clean the data.
  The data in this case has no nulls hence there is no reason remove any null values. If there were nulls we could do the following things. 
  1. Replace the null vaules with the average of the particular field or column.
  2. If the dataset that we have is large enough then we can just drop the row with the null value.
#### Step 3: draw the best fit line for the data.
  ```
  import numpy as np
  from statistics import mean
  from matplotlib import pyplot as plt

  def findSlope(xs,ys):
      xm = mean(xs)
      ym = mean(ys)
      xy = np.append(xs,ys)
      xym = mean(xy)
      xSm = mean(np.square(xs))

      slope = ((xm*ym) - xym)/(xSm - xm*xm)

      b = ym - slope*xm
      return slope,b

  data = [[2,3], [3,5], [1,2], [8,9], [7,8]]

  xs   = []
  xs.append([data[i][0] for i in range(len(data))])

  ys = []
  ys.append([data[i][1] for i in range(len(data))])

  xs = np.array(xs[0])
  ys = np.array(ys[0])

  slope, b = findSlope(xs,ys)

  lxs = []
  lxs.append([(slope*i + b) for i in xs])

  lxs = np.array(lxs[0])

  plt.scatter(xs,ys)
  plt.plot(xs,lxs)
  plt.show()
```
## Result:
![alt text](images/regressionLine.png)

Now we can see the best fit line in the above image. We can now plot new data points with the help of this line. For example if we were given a point along the x-axis all we would have to do is replace x the line equation (y = m * x + c) of the above line to predict y.

```
#point to predict
predictx = 4
predicty = slope*predictx + b
```
![alt text](images/regressionLinePredict.png)


