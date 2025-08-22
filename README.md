# Vector Operations in Python

This project implements **2D (`R2Vector`)** and **3D (`R3Vector`)** vector classes in Python.  
The code provides support for common vector operations such as addition, subtraction, scalar multiplication, dot product, cross product, and comparison operators.

---

## Features

### ✅ `R2Vector` (2D Vectors)
- Initialization with `x` and `y` coordinates
- String (`__str__`) and representation (`__repr__`) methods
- Vector **norm** (magnitude)
- Vector **addition** and **subtraction**
- Scalar multiplication and **dot product**
- Equality and inequality comparisons
- Norm-based comparisons (`<`, `>`, `<=`, `>=`)

### ✅ `R3Vector` (3D Vectors)
- Inherits from `R2Vector` with an additional `z` coordinate
- Supports all `R2Vector` operations
- Adds **cross product** functionality

---

## Code Example

```python
from vector import R2Vector, R3Vector

# Create two 3D vectors
v1 = R3Vector(x=6, y=9, z=3)
v2 = R3Vector(x=0.75, y=2.25, z=4)

print(f'v1 = {v1}')        # (6, 9, 3)
print(f'v2 = {v2}')        # (0.75, 2.25, 4)

# Vector addition
v3 = v1 + v2
print(f'v1 + v2 = {v3}')   # (6.75, 11.25, 7)

# Vector subtraction
v4 = v1 - v2
print(f'v1 - v2 = {v4}')   # (5.25, 6.75, -1)

# Dot product
v5 = v1 * v2
print(f'v1 * v2 = {v5}')   # 45.75

# Cross product
v6 = v1.cross(v2)
print(f'v1 x v2 = {v6}')   # (30.75, -22.5, 3.0)
