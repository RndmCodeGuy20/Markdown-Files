# **_SageMath Notes :-_**

# Solution of differentials equations in SageMath

---

```Python
#! Legend

>>> Input   #Comments

Output
```

### **_Solving Differential Equations_**

We start by defining variable x and function y depending on this variable.

```Python
x=var('x')
y= function('y')(x)

desolve(equation,variable,ics=.....,ivar=......,show_method=......)
```

| **_Attribute_** | **_Description_**                                                |
| --------------- | ---------------------------------------------------------------- |
| variable        | Dependent variable i.e. 'y'                                      |
| ics             | Initial conditions [xo, yo]                                      |
| ivar            | Independent variable i.e. x                                      |
| show_method     | Method which has been used to get the solution.i.e. Linear,Exact |

```Python
# Example

>>> x=var('x')
>>> y= function('y')(x)
>>> desolve(diff(y,x)-sin(2*x),y,show_method=True)

[_C - 1/2*cos(2*x), 'linear']


>>> desolve(diff(y,x)-sin(2*x),y,[0,1])

-1/2*cos(2*x) + 3/2     # Solution of differential equation at x=0 and y=1, and hence find the integrating constant C.

```

### **_Solving Second Order Differential Equations_**

```Python
>>> desolve(equation,variable,ics=[x0, y0, y′0 ]`or`[x0, y0, x1, y1].....,ivar=......,show_method=......)

# Example

>>> x=var('x')
>>> y=function('y')(x)
>>> desolve(diff(y,x,2)+2*diff(y,x)+y == cos(x),y)

(_K2*x + _K1)*e^(-x) + 1/2*sin(x)


>>> desolve(diff(y,x,2)+2*diff(y,x)+y == cos(x),y,[0,3,pi/2,2])

3*(x*(e^(1/2*pi) - 2)/pi + 1)*e^(-x) + 1/2*sin(x)
```

### **_Solving Simultaneous Differential Equations_**

```Python
>>> desolve_system(equations,variables,ics=.....,ivar=......,show_method=......)

# Solve a system of any size of 1st order ODEs. Initial conditions are optional.
```

#### _Example_

Solve :

$\frac {dx}{dt} = 1, \frac{dy}{dt} - x = -1, x(0) = 1, y(0) = 2$

```Python
>>> t = var('t')
>>> x = function('x')(t)
>>> y = function('y')(t)
>>> de1 = diff(x,t) + y - 1 == 0
>>> de2 = diff(y,t) - x + 1 == 0
>>> desolve_system([de1, de2], [x,y])

[x(t) == (x(0) - 1)*cos(t) - (y(0) - 1)*sin(t) + 1,
y(t) == (y(0) - 1)*cos(t) + (x(0) - 1)*sin(t) + 1]
```
