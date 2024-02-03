# Homework Assignment 1 (due Feb 9th)

The goal of this assignment is to explore the world of tensors and 
broadcasting using the [numpy](https://numpy.org/devdocs/) library.  
You'll gain valuable hands-on experience with these fundamental concepts, 
earning a total of 100 points for your efforts.

Feel free to drop by our office hours or post your questions directly
on the `Ed Discussion` forum.

> [!IMPORTANT]
> For all the questions in this assignment, no loops are allowed.  Seek
> vectorized and broadcasting operations to achieve the desired outcomes.
> You are not allowed to use built-in functions that may offer trivial
> one-shot solutions.

## `Question 1 ( pts)`
Write a function named `q1` with the specification below:
```
Input:   an integer value n >= 1
Output:  a 2D ndarray of shape n x n
```
The returned array is a matrix with the following pattern:
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

## Submission and Grading
This assignment uses an autograder.  For each of the questions you either 
pass the test cases (full points) or not (zero points).  To ensure 
compatibility with the autograder, your program must follow the exact 
specifications provided above, specifically, using the same function names 
and follow input/output requirements.

You will submit a single file named `functions.py` with all of your functions
via `Gradescope`.

> [!CAUTION]
> Remember, academic integrity is of utmost importance.  Any attempts at cheating
> or plagiarism will result in a forfeiture of credit.
