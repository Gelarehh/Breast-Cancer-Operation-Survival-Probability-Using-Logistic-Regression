## Logistic Regression

Logistic regression is a statistical method for analyzing a dataset in which there are one or more independent variables that determine an outcome. The outcome is measured with a dichotomous variable (in which there are only two possible outcomes). 

The logistic function, also called the sigmoid function was developed by statisticians to describe properties of population growth in ecology, rising quickly and maxing out at the carrying capacity of the environment. It’s an S-shaped curve that can take any real-valued number and map it into a value between 0 and 1, but never exactly at those limits.

logistic function: 

<img src="https://latex.codecogs.com/svg.latex?\small&space;\sigma(x)=1/(1+exp(-x))" />

In the training process, the logistic function is applied to the multiplication of the vector of parameters and X. Theta is also called the weights factor or confidences of the equation and X is the feature set.

<img src="https://latex.codecogs.com/svg.latex?\small&space;\sigma({{\theta}^T}x)=1/(1+exp(-{{\theta}^T}x))" />

<br/><br/>

<p align="center">
  <img width="500" height="300" src="https://user-images.githubusercontent.com/66460485/129236247-45c3dc2d-634f-45e9-b935-a816138aadf7.png">
</p>

**Training Process**
<ol>
<li>Initialize <img src="https://latex.codecogs.com/svg.latex?\small&space;\theta"> </li>
<li>Calculate <img src="https://latex.codecogs.com/svg.latex?\small&space;\sigma({{\theta}^T}x)"> </li>
<li>Compare the outcome of step 2 with the actual lable and drive error </li>
<li>Repeat steps 2 and 3 for all data samples and define a cost fuction as a function of errors</li>  
<li>Change <img src="https://latex.codecogs.com/svg.latex?\small&space;\theta"> to reduce the cost</li>
<li>Repeat the itteration from step 2</li>
</ol>

In order to minimize the cost, an optimization method, called **gradient descent** method is used. Therefore, step 5 can be done as follows:
<li>Calculate the gradient vector of the cost function</li>
<li>Update the weights using step 1 and a learning rate</li>

## Dataset
Dataset contains cases from study conducted on the survival of patients who had undergone surgery for breast cancer.
> Attributes

<ol>
<li>Age of patient at time of operation (numerical) </li>
<li>Patient's year of operation (year - 1900, numerical)</li>
<li>Number of positive axillary nodes detected (numerical)</li>
<li>Survival status, 1 or 2</li>
</ol>

- 1 = the patient survived 5 years or longer
- 2 = the patient died within 5 year
