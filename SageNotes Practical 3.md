# **_SageMath Notes :-_**

# To learn Calculus with SageMath

---

```Python
#! Legend

>>> Input   #Comments

Output
```

### **_Limits_**

```Python
>>> limit(f(x) , x = a, dir =′ +′or′−′ )

# "dir" - (default: None); dir may have the value 'plus' (or '+' or 'right' or 'above') for a limit from above, 'minus' (or '-' or'left' or 'below') for a limit from below, or may be omitted (implying a two-sided limit is to be computed).

>>> f(x) = x/abs(x)
>>> limit(f(x) , x = 0, dir = '+')

1


>>> limit(f(x) , x = 0, dir = '-')

-1


>>> limit(f(x) , x = 0)

undefined


>>> assume()

# Make the given assumptions.


>>> forget()

# Forget the given assumption, or call with no arguments to forget all assumptions.
```

### **_Derivatives_**

```Python
>>> diff(f,n)
>>> f.diff(n)

# The nth derivative of f.


>>> show(f.diff(n))

# Show the nth derivative of f.
# Pretty print the arguments in an intelligent way.
# For a single positional argument, this function chooses the highest-quality output supported by the user interface.
```

### **_Derivatives_**

```Python
>>> f(x,y) = (x^2 + y^2)^(1/2)
>>> diff(f,x)

# The first derivative of f with respect to x.


>>> diff(f,y)

# The first derivative of f with respect to y.


>>> diff(f,x,y)

# The first derivative of f first with respect to x and then with respect to y.


>>> diff(f,x,n)

# The nth derivative of f with respect to x.


>>> diff(f,y,n)

# The nth derivative of f with respect to y.


>>> diff(f,x,y,n)

# The nth derivative of f with respect to x and then with respect to y.


>>> diff(f,x)(x=a,y=b) # if a,b are float values, evaluation is precise.

# The first derivative of f with respect to x evaluated at a and b.


>>> full_simplify(f)

# Simplify f.


>>> x = var('x')    # x is a symbolic variable
>>> y = var('y')    # y is a symbolic variable
>>> f(x,y) = x^3 + y^3 - 6*x*y  # f is a symbolic function
>>> y=function('y')(x) # y is a function of x
>>> temp=diff(f(x,y)) # temp is a symbolic expression
>>> show(solve(temp,diff(y))) # solve for y

# First we will solve to get differential with respect to x, that will give us a term diff(y(x),x).
# To solve that expression we will differentiate with respect to y and then solve for y.
```

### **_Derivatives_**

```Python
>>> find_local_maximum(f,a,b)

# Numerically find a local maximum of the expression f on the interval [a,b] (or [b,a]) along with the point at which the maximum is attained.


>>> find_local_minimum(f,a,b)

# Numerically find a local minimum of the expression f on the interval [a,b] (or [b,a]) along with the point at which the minimum is attained.


>>> find_root(f,a,b)

# Numerically find a root of the expression f on the interval [a,b] (or [b,a]) along with the point at which the root is attained.
```



```Python

```
