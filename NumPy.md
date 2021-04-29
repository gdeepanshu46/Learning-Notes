# NumPy.

- It is a library for the Python programming language
- It adds support for large, multi-dimensional arrays and matrices
- A long with a large collection of high-level mathematical functions to operate on these arrays.

## Why NumPy over Lists?

- Consumes less memory
- Fast, it uses Contiguous Memory Allocation
- No type checking is required as NumPy stores similar data
- Convenient to use

## The Basics

```python
import numpy as np
a = np.array([1, 2, 3], dtype='int16')
b = np.array([
    [1, 2, 3, 4, 5, 6, 7],
    [8, 9, 10, 11, 12, 13, 14],
    [15, 16, 17, 18, 19, 20, 21]
])
```

## Accessing Elements

```python
# get dimension
a.ndim
b.ndim

# get shape
a.shape
b.shape

# get specific element
b[0, 1]
b[0][1]

# get specific row
b[0] #or 
b[0, :]

# get specific column
b[:, 1]

# getting specific part of array [start : end : stepsize]
b[0, 1::2]

# changing element
b[0, 0] = 0
```

## Initializing different types of Arrays

```python
# all 0's matrix
np.zeros(5)
np.zeros((3, 3))

# all 1's matrix
np.ones(5)
np.ones((3, 3))

# all other number's matrix
np.full((3, 3), 99)

# all random decimals numbers matrix
np.random.rand(3, 3)

# all random integers matrix
# values lies btw 0 and 5
np.random.randint(0, 5, size=(3, 3))

# identity matrix
np.identity(3)		
```

## Be Careful while Copying Arrays

```python
c = np.array([1, 2, 3])
# d = c does shallow copy
d = c.copy() # does deep copy
d
d[0] = 100
c
```

## Mathematics

```python
# all sorts of operations can be done on individual elements

# square
a ** 2

# sum
a + 2

# sin
np.sin(a)

# mulitplication
g = np.ones((2, 3))
h = np.full((2, 3), 2)
g*h
```

## Linear Algebra

```python
e = np.ones((2, 3))
f = np.ones((3, 2))
np.matmul(e, f)

# find determinant
i = np.identity(3)
np.linalg.det(i)
```

