# 1.) Normalization Problem:
#### Normalization is one of the most basic preprocessing techniques in data analytics which involves centering and scaling process.
#### Centering means subtracting the data from the mean and scaling means dividing with its standard deviation.
#### In Python, element-wise mean and element-wise standard deviation can be obtained by using .mean() and .std() calls.
#### In this problem, create a random 5 x 5 ndarray and store it to variable X. Normalize X.
#### Save your normalized ndarray as X_normalized.npy

```python
# Start 
# Import the numpy library
import numpy as np
# Initialize variable X as a randomized 5x5 array
X = np.random.rand(5,5)
# Initialize and set X_mean as the mean of X
X_mean = X.mean()
# Initialize and set X_std as the standard deviation of X
X_std = X.std()
# Perform calculation by setting Z as the Normalized form of X
Z = (X - X_mean) / X_std
# Save the normalized array to a .npy file
np.save('X_normalized.npy', Z)
# Test if loading the npy file works
np.load('X_normalized.npy')
# End

```
# 2.) DIVISIBLE BY 3 PROBLEM: 
#### Create a 10 x 10 ndarray which are the squares of the first 100 positive integers.
#### From this ndarray, determine all the elements that are divisible by 3. Save the result as div_by_3.npy

```python
# Start
# Import the python library numpy
import numpy as np
# Generate a 10x10 ndarray with squares of the first 100 positive integers
A = np.arange(1,101).reshape(10,10)**2
# Find all elements in the generated array that are divisible by three
divisible_by_3 = A[A % 3 == 0]
# Save the result to a .npy file
np.save('div_by_3.npy', divisible_by_3)
# Test by loading the saved npy file
np.load('div_by_3.npy')
# End
