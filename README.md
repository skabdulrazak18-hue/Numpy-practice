"""
NumPy example Practice Program
Real-time use: This program demonstrates how arrays are used in
student marks calculation, sensor data checking, and data comparison
in AI/IoT applications.
"""

import numpy as np

# =========================
# Part A – Basic array operations
# Used in real life: combining two datasets like marks or salary
# =========================

np.info(np.add)  # shows info about np.add function

A = np.array([1, 2, 3, 4])              # dataset 1
B = np.linspace(1.0, 4.0, 4)            # dataset 2 (evenly spaced values)
C = np.add(A, B)                        # element-wise addition

print("A:", A.tolist())
print("B:", B.tolist())
print("A+B (C):", C.tolist())

# initialize arrays (used in ML, sensors, etc.)
Z = np.zeros(4)   # start with all zeros
O = np.ones(4)    # start with all ones

print("zeros:", Z.tolist())
print("ones:", O.tolist())


# =========================
# Part B – Check if array contains zero
# Used in real life: validate payments/sensor data (no zero values)
# =========================

print("\n==(B) Test whether none of the elements of array is zero")

arr1 = np.array([5, -2, 3, 1])
arr2 = np.array([5, 0, 3, 1])

none_zeros_arr1 = np.all(arr1 != 0)   # True if no element is zero
none_zeros_arr2 = np.all(arr2 != 0)

print("arr1:", arr1.tolist(), "none zero?", none_zeros_arr1)
print("arr2:", arr2.tolist(), "none zero?", none_zeros_arr2)


# =========================
# Part C – Element-wise comparison
# Used in real life: compare expected vs actual values (sensors/AI)
# =========================

print("\n==(C) Element-wise comparison ==")

X = np.array([1.0, 2.0, 3.0, 4.0])   # expected values
Y = np.array([0.9, 2.0, 3.0, 4.2])   # actual values

print("X:", X.tolist())
print("Y:", Y.tolist())

gt = np.greater(X, Y)           # X > Y
ge = np.greater_equal(X, Y)     # X >= Y
lt = np.less(X, Y)              # X < Y
le = np.less_equal(X, Y)        # X <= Y
eq = np.equal(X, Y)             # X == Y

# check if values are almost equal (used in ML & finance)
is_close = np.isclose(X, Y, atol=1e-2, rtol=1e-8)
all_close = np.allclose(X, Y, atol=1e-2, rtol=1e-8)

print("greater:", gt.tolist())
print("greater_equal:", ge.tolist())
print("less:", lt.tolist())
print("less_equal:", le.tolist())
print("equal:", eq.tolist())
print("is_close:", is_close.tolist())
print("all_close:", all_close)
