##### Normalization Problem. This function normalizes a randomly generated 2D array by subtracting its mean and dividing by its standard deviation. The result is then saved to a file.

This process ensures the elements in the array are rescaled sto that they have a mean of 0 and a standard deviation of 1.

```
np.random.random ((r,c)):      generates a 5x5 array with random elements from 0-1
.mean:                         calculates for the mean of all the values in the array.
.std:                          calculates for the standard deviation of the array.
.save:                         saves the normalized array in a file for later use.
```

##### Divisible By 3 Problem. This function generates the squares of the first 100 positive integers. It then reshapes to a 10x10 array, and extracts the integers that are divisible by 3. The result is then saved to a file.

This combines the reshaping of an array and filtering using NumPy.

```
.arrange(x, y)**2:            generates the squares of numbers from 1-100.
.reshape(r, c):               reshapes the array of 100 values to a 2D array with a size of 10x10.
A[A % 3 == 0]:                filters and extracts the elements of the array that are divisible by 3.
.save:                         saves the normalized array in a file for later use.
```
