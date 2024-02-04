# Homework Assignment 1 (due Feb 11th @ 11:59pm)

The goal of this assignment is to explore the world of tensors and 
broadcasting using the [numpy](https://numpy.org/devdocs/) library.  
You'll gain valuable hands-on experience with these fundamental concepts, 
earning a total of 100 points for your efforts.

Feel free to drop by our office hours or post your questions directly
on the `Ed Discussion` forum.

> [!IMPORTANT]
> For all the questions on this assignment, **no loops are allowed**.  Seek
> vectorized and broadcasting operations to achieve the desired outcomes.
> Likewise, you are not allowed to use built-in functions that may
> offer trivial one-shot solutions.

## `Question 1 (15 pts)`
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

## `Question 2 (15 pts)`
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

## `Question 3 (15 pts)`
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

## `Question 4 (15 pts)`
Write a function named `q4` with the specification below:
```
Input:   an ndarray of shape at least 1d and dtype=float
Output:  an ndarray of the same shape and dtype=float
```
The function returns an ndarray where the magnitude of
all row-vectors in the innermost 2d ndarrays is 1.  For
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

## `Question 5 (10 pts)`
Write a function named `q5` with the specification below:
```
Input:   an ndarray of shape at least 1d and dtype=int
Output:  sum of all elements multiples of 7 or 11
```
The function returns the sum as a scalar value.
```python
# input
[44 18 39 33 33 32]

# output
110

# input
[[[[ 9 39 24]
   [36 19 41]
   [46 39  5]]

  [[28 15 24]
   [22 24 48]
   [42 38  6]]]


 [[[ 2 25 46]
   [19 39  5]
   [17 24 14]]

  [[ 9 38 24]
   [15 37  2]
   [35 47 10]]]]

# output
141
```

## `Question 6 (15 pts)`
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

## `Question 7 (15 pts)`
Write a function named `q7` with the specification below:
```
Input:   an ndarray of shape at least 2d (...,m,n) and dtype=float
         an scalar value k >= 1
Output:  a padded ndarray of shape (...,m+2k,n+2k) and dtype=float
```
The function returns an ndarray where zeros have been added
to the four sides of all innermost 2d arrays in the input ndarray.
Input parameter k controls the amount of padding.
```python
# input shape (2,2) and k=1
[[0.         0.         0.         0.        ]
 [0.         0.90871286 0.99775115 0.        ]
 [0.         0.16949961 0.86268474 0.        ]
 [0.         0.         0.         0.        ]]

# input shape (2,1,2,2) and k=2
[[[[0.         0.         0.         0.         0.         0.        ]
   [0.         0.         0.         0.         0.         0.        ]
   [0.         0.         0.69188511 0.21990861 0.         0.        ]
   [0.         0.         0.23399214 0.99926364 0.         0.        ]
   [0.         0.         0.         0.         0.         0.        ]
   [0.         0.         0.         0.         0.         0.        ]]]


 [[[0.         0.         0.         0.         0.         0.        ]
   [0.         0.         0.         0.         0.         0.        ]
   [0.         0.         0.94755712 0.83227846 0.         0.        ]
   [0.         0.         0.60942744 0.27105814 0.         0.        ]
   [0.         0.         0.         0.         0.         0.        ]
   [0.         0.         0.         0.         0.         0.        ]]]]
```

## Submission and Grading
This assignment uses an autograder.  For each of the questions you either 
pass the test cases (full points) or not (zero points).  To ensure 
compatibility with the autograder, your program must follow the exact 
specifications provided above, in particular, using the same function names 
and strictly following all input/output requirements.

You will submit a single file named `functions.py` containing all of your 
functions via `Gradescope`.  Multiple submissions are allowed with a 
limit of XXX.

> [!CAUTION]
> Remember, academic integrity is of utmost importance.  Any attempts at cheating
> or plagiarism will result in a forfeiture of credit.
