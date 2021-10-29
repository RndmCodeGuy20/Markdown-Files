# **_SageMath Notes :-_**

# To Use SageMath as an Advanced Calculator

---

```Python
#! Legend

>>> Input   #Comments

Output
```

## <u> 1. Basic Operations :-</u>

### **_Division_**

```Python
>>> 79/12

79/12
```

### **_Division (Float Answer)_**

```Python
>>> 79/12.0 # int/float = float

6.5833333333333


>>> 79/12.n()
# Lower case "n()" is an alias for "numerical_approx()" and may be used as a method.

6.5833333333333


>>> 79/12.n(digits = 5)

6.5833 # 5 Significant figures.


>>> numerical_approx(pi, digits=10) # also pi.n(digits = 10)

3.141592654
```

### **_Function Result_**

```Python
>>> function(int)

int / function(int)


>>> function(float)

float #(result)


>>> sin(81.0)

-0.629887994274454


>>> sin(81)

sin(81)
```

### **_Digits Manipulation_**

```Python
>>> F = factorial(10)
>>> F

3628800


>>> F.ndigits() #Returns number of digits in 10!

7


>>> w = F.digits()
>>> w[6] #Printing the 1st term in the number F

3
```

#### Indexing

| 3   | 6   | 2   | 8   | 8   | 0   | 0   |
| --- | --- | --- | --- | --- | --- | --- |
| 6   | 5   | 4   | 3   | 2   | 1   | 0   |

### **_Playing with Numbers and Variables_**

```Python
>>> n.is_prime()
>>> is_prime(n)

# Return "True" if n is a prime number, and "False" otherwise.


>>> n.factor()
>>> factor(n)

# Return the factorization of "n".  The result depends on the type of "n".


>>> n.next_prime()
>>> next_prime(n)

#The next prime greater than the integer n. If n is prime, then this function does not return n, but the next prime after n.


>>> gcd(a,b)

# Return the greatest common divisor of "a" and "b".


>>> lcm(a,b)

# The least common multiple of a and b, or if a is a list and b is omitted the least common multiple of all elements of a.

>>> list(primes(a,b))

# Returns a list containing all primes from a to b.


>>> nth_prime(n)

# Return the n-th prime number (1-indexed, so that 2 is the 1st prime.)
```

### **_Functions Revisited_**

```Python
# Sample Function declaration

>>> x = var('x')
>>> f = sin(x^2)*exp(-x) + 3*x + 1
>>> show(f)

# Pretty prints the arguments in an intelligent way.

>>> f(n)

# Float value of sin(n^2)*exp(-n) + 3*n + 1

>>> diff(f,n)
>>> f.diff(n)

# The nth derivative of f.


>>> f.integral()
>>> integral(f)

# Return an indefinite or definite integral of an object "x".


>>> solve([a*x^2+b*x+c == 0],x)
>>> solve([3*x1 - 2*x2 == 7, 2*x1 + 3*x2 == 11],x1,x2)

# Algebraically solve an equation or system of equations (over the complex numbers) for given variables.
# Inequalities and systems of inequalities are also supported.
```
