# Roots-of-Equations-Examples-C-CPP-Matlab-
This repository is about implementing different methods for roots of equations in C/C++/Matlab with different examples. The essence of this topic is to provide readers with a quick reference for different methods plus their implementation in C/C++/Matlab. 

**The Newton-Raphson formula:**

The formula:

![](https://latex.codecogs.com/gif.latex?x_%7Bi&plus;1%7D%20%3D%20x_i%20-%20%5Cfrac%7Bf%28x_i%29%7D%7Bf%27%28x_i%29%7D)

##### Example: 
determine the root(s) of this equation

![](https://latex.codecogs.com/gif.latex?f%28x%29%20%3D%20e%5E%7B-x%7D%20-%20x)

##### Solution:

![](https://latex.codecogs.com/gif.latex?x_0%20%3D%200%20%5C%5C%20f%27%28x%29%20%3D%20-e%5E%7B-x%7D%20-%201)

Matlab code is 
```Matlab
clear variables; clc

x = 0; %initial guess
iterNum = 10; % maximum number of iterations

for i = 0:iterNum
      f =  exp(-x) - x;
   dfdx = -exp(-x) - 1;
   x = x - f/dfdx;
end
fprintf('root of equation is %.8f\n', x)
```
The resut is   
`root of equation is 0.56714329`


