# **_SageMath Notes :-_**

# Computing Linear Algebra using SageMath

---

```Python
#! Legend

>>> Input   #Comments

Output
```

### **_Defining a Matrix_**

```Python
>>> # Defining 3 by 3 matrix
>>>A=matrix([
    [1,2,3],
    [4,5,6],
    [7,8,9]
    ])
>>> show('A=',A)

>>> show(matrix(ZZ / RR / CDF / QQ, 3,2, [1,2,3,4,5,6]))

# ZZ => Integer
# RR => Real
# CDF => Complex Double Float
# QQ => Rational


>>> A.transpose()

# Transpose of A


>>> A.det()

# Determinant of A


>>> A.inverse()

# Inverse of A


>>> A.rank()

# Rank of A


>>> A.adjugate()

# Adjugate / Adjoint of A


>>> A.trace()

# Trace of A


>>> ones_matix(3,3)

# 3 by 3 matrix of ones


>>> zero_matix(3,3)

# 3 by 3 matrix of zeros


>>> identity_matix(3)

# 3 by 3 identity matrix


>>> random_matix(ZZ, 3,3,x=a,y=b)

# 3 by 3 matrix of random numbers belonging to Z in the range a to b.


>>> C = A.augment(B)

# Augmenting A with B.


>>> C.echelon_form()

# Echelon form of C


>>> A.characteristic_polynomial(x)

# Characteristic polynomial of A in terms of x.


>>> A.eigenvalues()

# Eigenvalues of A


>>> A.eigenvectors_right()

# Right eigenvectors of A
#For each distinct eigenvalue, returns a list of the form (e,V,n) where e is the eigenvalue, V is a list of eigenvectors forming a basis for the corresponding right eigenspace, and n is the algebraic multiplicity of the eigenvalue.


>>> A.eigenmatrix_right()

# Return matrices D and P, where D is a diagonal matrix of eigenvalues and the columns of P are corresponding eigenvectors (or zero vectors).
```

```Python

```
