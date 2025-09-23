### Normalization Problem. This function normalizes a randomly generated 2D array by subtracting its mean and dividing by its standard deviation. The result is then saved to a file.

This process ensures the elements in the array are rescaled sto that they have a mean of 0 and a standard deviation of 1.


#### Functions Utilized in Normalization Problem
```
np.random.random ((r,c)):      generates a 5x5 array with random elements from 0-1
.mean:                         calculates for the mean of all the values in the array.
.std:                          calculates for the standard deviation of the array.
.save:                         saves the normalized array in a file for later use.
```
#### Code Overview
#### 1. Initialization

This codeblock imports the numpy library which is essential for array computations.
~~~
# Loads the NumPy library to this program.
import numpy as np
~~~

#### 2. Array Generator

This codeblock generates a random array with a size of 5 by 5 with values of indeces from 0 to 1.
~~~~
X = np.random.random((5,5))
~~~~

#### 3. Descriptive Statistics

This codeblock computes for the necessary descriptive statistic parameter for normalization
~~~~
# Calculates for the value mean of the array
mean = X.mean()
# Calculates for the standard deviation of the array
std_dev = X.std()
~~~~

#### 4. Normalization

This codeblock calculates for the normalized value.
~~~
# Calculates for the normalized value of the array
X_Normalized = ( X - mean ) / std_dev
~~~

#### 5. Save and Display

This codeblock saves the result to .npy file and displays the result to ensure that the code works properly.
~~~
# Saves the normalized value to a file
np.save("X_normalized.npy", X_Normalized)

print ("Original Value: \n", X, "\n")
print ("Mean of X: \n", mean, "\n")
print ("Standard Deviation of X: \n", std_dev, "\n")
print ("Normalized Value of X: \n", X_Normalized,"\n")
~~~

***

### Divisible By 3 Problem. This function generates the squares of the first 100 positive integers. It then reshapes to a 10x10 array, and extracts the integers that are divisible by 3. The result is then saved to a file.

This combines the reshaping of an array and filtering using NumPy.

#### Functions Utilized in 'Divisible by 3' Problem
```
.arrange(x, y)**2:            generates the squares of numbers from 1-100.
.reshape(r, c):               reshapes the array of 100 values to a 2D array with a size of 10x10.
A[A % 3 == 0]:                filters and extracts the elements of the array that are divisible by 3.
.save:                        saves the normalized array in a file for later use.
```
#### Code Overview

#### 1. Initialization

This codeblock imports the numpy library which is essential for array computations.
~~~
# Loads the NumPy library to this program
import numpy as np
~~~

#### 2. Square Generation

This codeblock generates the square of the first 100 positive integers.
~~~
# Generates the square of the first 100 positive integers
sqr_n = np.arange (1,101)**2
~~~

#### 3. Reshape

This codeblock reshapes the generated integers to 10 by 10 shape.
~~~
# Reshapes the sqr_n (1D array) to a 2D array with a shape of 10x10
A = sqr_n.reshape (10,10)
~~~

#### 4. Divisibility

This codeblock obtain all integers that are divisible by 3.
~~~
# Gets all the integers that are divisible by 3
div_by_3 = A[A % 3 == 0]
~~~

#### 5. Save
Saves the result in a .npy file.
~~~
# Saves the integers divisible by 3 to a file
np.save("div_by_3.npy", div_by_3)
~~~
