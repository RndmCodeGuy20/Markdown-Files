# **_SageMath Notes :-_**

# To Learn Calculus with SageMath

---

```Python
#! Legend

>>> Input   #Comments

Output
```

### **_Evaluation of Integral_**

```Python
>>> integral(expression, variable, lower_bound, upper_bound)

# Returns Definite value of integral.


# Area between two curves

>>> Area = integral((f(x) - g(x)),x,a,b)
>>> show(Area)
>>> show(Area.n())

Decimal Output
```

### **_Arc Length_**

Arc Length is the length of a curve in a plane, and it is given by :-

$L = \int_{b}^{a} \sqrt(1 + (dxdy)^2) dx$

```Python
>>> show(integral(sqrt(1+derivative(f,x)^2),x,1,2).n())

Decimal Output # f(x) is a function of x.
```

### **_Area of Surface of Revolution_**

Rotating about x-axis, the area of a surface of revolution is given by :-

$S = \int_{b}^{a} 2πy \sqrt (1 +(dydx)^2) dx.$

Rotating about y-axis, the area of a surface of revolution is given by :-

$S = \int_{d}^{c} 2πx \sqrt (1 +(dxdy)^2) dy.$

```Python
>>> show(integral(2*pi*f(x)*sqrt(1+derivative(f,x)^2),x,-r,r))
```