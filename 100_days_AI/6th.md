# Day 6: Introduction to NumPy

## Introduction to NumPy

### What is NumPy?
NumPy (Numerical Python) is a powerful library for numerical computing in Python. It provides support for arrays, matrices, and many mathematical functions to operate on these data structures efficiently. NumPy is widely used in data science, machine learning, and scientific computing due to its performance and ease of use.

### Key Features of NumPy
- **N-Dimensional Array**: NumPy's primary feature is its N-dimensional array object, ndarray, which is a powerful and versatile data structure.
- **Mathematical Functions**: Provides a wide range of mathematical functions to perform operations on arrays.
- **Broadcasting**: Allows for vectorized operations on arrays of different shapes.
- **Linear Algebra**: Supports linear algebra operations, including matrix multiplication and decomposition.
- **Random Sampling**: Tools for generating random numbers and sampling from distributions.

## Installing and Importing NumPy

### Installing NumPy
Ensure you have NumPy installed. You can install it using pip if it's not already installed:
```sh
pip install numpy
```
### Importing NumPy
Import the NumPy library in your Python script:
```p
import numpy as np
```
### Creating Arrays
Create a NumPy array from a Python list:
```python
array = np.array([1, 2, 3, 4, 5])
print("Array:", array)
```
### Array Operations
Perform basic arithmetic operations on NumPy arrays:
```python
array = np.array([1, 2, 3, 4, 5])
print("Array:", array)

# Add 10 to each element
print("Array + 10:", array + 10)

# Multiply each element by 2
print("Array * 2:", array * 2)

# Square each element
print("Array squared:", array ** 2)
```
### Array Indexing and Slicing
Access elements and subarrays using indexing and slicing:
```python
array = np.array([1, 2, 3, 4, 5])

# Access the first element
print("First element:", array[0])

# Access elements from index 1 to 3
print("Elements from index 1 to 3:", array[1:4])

# Access the last element
print("Last element:", array[-1])
```
### Reshaping Arrays
Reshape an array to a different dimension:
```python
array = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9])
reshaped_array = array.reshape(3, 3)
print("Reshaped array (3x3):\n", reshaped_array)
```
### Sum, Mean, and Standard Deviation
Use NumPy's built-in mathematical functions:
```python
array = np.array([1, 2, 3, 4, 5])

# Calculate the sum of all elements
print("Sum:", np.sum(array))

# Calculate the mean of all elements
print("Mean:", np.mean(array))

# Calculate the standard deviation
print("Standard Deviation:", np.std(array))
```
### Exercise 1: Create a 4x4 Identity Matrix
```python
identity_matrix = np.eye(4)
print("4x4 Identity Matrix:\n", identity_matrix)
```
### Exercise 2: Generate an Array of 10 Random Numbers Between 0 and 1
```python
random_array = np.random.random(10)
print("Array of 10 random numbers between 0 and 1:\n", random_array)
```
### Exercise 3: Create a 3x3 Matrix with Values Ranging from 0 to 8
```python
matrix = np.arange(9).reshape(3, 3)
print("3x3 Matrix with values ranging from 0 to 8:\n", matrix)
```
### Exercise 4: Create a Random Vector of Size 10 and Sort It
```python
random_vector = np.random.random(10)
sorted_vector = np.sort(random_vector)
print("Random vector of size 10:\n", random_vector)
print("Sorted vector:\n", sorted_vector)
```
#  Additional Resources

- Refer to the official [NumPy Documentation](https://numpy.org/doc/stable/) for more in-depth information and examples.

## Summary
- **Learn**: Understand the basics of NumPy for numerical computing.
- **Follow**: Complete the NumPy Quickstart Tutorial.
- **Implement**: Practice basic operations with NumPy arrays.

Feel free to ask if you need help with any specific exercise or concept!
