# Homework Assignment 1 (due Feb 9th)

The goal of this assignment is to explore the world of tensors and 
broadcasting using the [numpy](https://numpy.org/devdocs/) library.  
You'll gain valuable hands-on experience with these fundamental concepts, 
earning a total of 100 points for your efforts.

Feel free to drop by our office hours or post your questions directly
on the `Ed Discussion` forum.

> [!IMPORTANT]
> For all the questions in this assignment, **no loops are allowed**.  Seek
> vectorized and broadcasting operations to achieve the desired outcomes.
> You are not allowed to use built-in functions that may offer trivial
> one-shot solutions.

## `Question 1 ( pts)`
Write a function named `q1` with the specification below:
```
Input:   an integer value n >= 1
Output:  an ndarray of shape=(n,n) and dtype=int
```
The function returns an ndarray with the following pattern:
```python
# n = 3
[[ 30  30  30]
 [-30  20  30]
 [-30 -30  10]]

# n = 5
[[ 50  50  50  50  50]
 [-50  40  50  50  50]
 [-50 -50  30  50  50]
 [-50 -50 -50  20  50]
 [-50 -50 -50 -50  10]]
```

## `Question 2 ( pts)`
Write a function named `q2` with the specification below:
```
Input:   an integer value n >= 1
Output:  an ndarray of shape=(n,n) and dtype=int
```
The function returns an ndarray with the following pattern:
```python
# n = 3
[[0 1 2]
 [1 2 3]
 [2 3 4]]

# n = 5
[[0 1 2 3 4]
 [1 2 3 4 5]
 [2 3 4 5 6]
 [3 4 5 6 7]
 [4 5 6 7 8]]
```

## `Question 3 ( pts)`
Write a function named `q3` with the specification below:
```
Input:   an integer value n >= 1
Output:  an ndarray of shape=(n,n,n) and dtype=int
```
The function returns an ndarray with the following pattern:
```python
# n = 2
[[[ 0  0]
  [ 0  0]]

 [[10 10]
  [10 10]]]

# n = 4
[[[ 0  0  0  0]
  [ 0  0  0  0]
  [ 0  0  0  0]
  [ 0  0  0  0]]

 [[10 10 10 10]
  [10 10 10 10]
  [10 10 10 10]
  [10 10 10 10]]

 [[20 20 20 20]
  [20 20 20 20]
  [20 20 20 20]
  [20 20 20 20]]

 [[30 30 30 30]
  [30 30 30 30]
  [30 30 30 30]
  [30 30 30 30]]]
```

## `Question 4 ( pts)`
Write a function named `q4` with the specification below:
```
Input:   an ndarray of shape at least 1d and dtype=float
Output:  an ndarray of the same shape and dtype=float
```
The function returns an ndarray where the magnitude of
all row-vectors in the innermost 2d ndarray is 1.  For
1d inputs, the magnitude of the array should become 1.
```python
# input shape (4,) => magnitude of the output vector is 1
[0.5357516 0.41866108 0.68772969 0.2544032]

# input shape (4,3) => magnitude of each row vector is 1
[[0.52416155 0.657591 0.54113652]
 [0.92469168 0.10775349 0.36514995]
 [0.88627862 0.17416369 0.42915872]
 [0.16722488 0.92872427 0.33091853]]

# input shape (2, 1, 4, 2) => magnitude of each row vector is 1
[[[[0.94223819 0.33494358]
   [0.99797798 0.06356055]
   [0.26889724 0.96316887]
   [0.99997926 0.00644059]]]

 [[[0.50687869 0.86201739]
   [0.98685332 0.16161844]
   [0.75085082 0.66047183]
   [0.09566265 0.99541381]]]]
```

## `Question 5 ( pts)`
Write a function named `q5` with the specification below:
```
Input:   an ndarray of shape at least 1d and dtype=int
Output:  sum of all elements multiples of 7 or 11
```
The function returns the sum as a scalar value.
```python
# input
[14  5  4  3  2 15]

# output
34

# input
[[[[ 7  2 13]
   [ 5  3  7]
   [ 1  3  9]]

  [[ 2 10 11]
   [ 9  1 12]
   [13  3  7]]]


 [[[ 1  5  7]
   [13  4  7]
   [ 8 14  5]]

  [[14 14  3]
   [ 8 13 11]
   [10  1  9]]]]

# output
112
```

## `Question 6 ( pts)`
Write a function named `q6` with the specification below:
```
Input:   an integer value n >= 1
Output:  an ndarray of shape=(n,n) and dtype=int
```
The function returns an ndarray with the following pattern:
```python
# 1
[[1]]

# 3
[[1 1 1]
 [1 2 4]
 [1 3 9]]

# 5
[[  1   1   1   1   1]
 [  1   2   4   8  16]
 [  1   3   9  27  81]
 [  1   4  16  64 256]
 [  1   5  25 125 625]]
```

## Submission and Grading
This assignment uses an autograder.  For each of the questions you either 
pass the test cases (full points) or not (zero points).  To ensure 
compatibility with the autograder, your program must follow the exact 
specifications provided above, specifically, using the same function names 
and strictly follow all input/output requirements.

You will submit a single file named `functions.py` containing all of your 
functions via `Gradescope`.  Multiple submissions are allowed with a 
limit of XXX.

> [!CAUTION]
> Remember, academic integrity is of utmost importance.  Any attempts at cheating
> or plagiarism will result in a forfeiture of credit.
