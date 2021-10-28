# **_SageMath Notes :-_**

---

```Python
#! Legend

>>> Input   #Comments

Output
```

## <u> Plotting Graphs:-</u>

### **_Plot_**

```Python
>>> f(x) = a*x+b # any explicit function.

# Use plot by writing

#   "plot(X, ...)"


>>> plot(x^3, (-2, 2), ymin = -4, ymax = 4, axes=False)

# Returns a plot with, x values ranging from -2 to 2, and y values ranging from -4 to 4.
# Axes are set to false ie., axes will not be shown.
```

### **_Graph Attributes_**

```Python
>>> plot(x^2,(x,-2,2),color='orange',title="Upward Parabola",figsize=3,thickness=2,gridlines='True', legend_label='test curve')

# x values ranging from -2 to 2.
# color => changes color of traced curve.
# title => gives a title to the figure.
# figsize(n,n) => dimensions of image in n x n inches.
# thickness => thickness of the traced curve.
# gridlines => shows a dotted grid.
# legend_label => gives a legend to the curve.

# Other attributes :-
{'alpha': 1,
 'thickness': 1,
 'fill': False,
 'fillcolor': 'automatic',
 'fillalpha': 0.5,
 'plot_points': 200,
 'adaptive_tolerance': 0.01,
 'adaptive_recursion': 5,
 'detect_poles': False,
 'exclude': None,
 'legend_label': None,
 'aspect_ratio': 'automatic'}
```

### **_Combined Graphs_**

```Python
>>> curve1=plot(-x^2,0,2,color="red")
>>> curve2=plot(+x^2,0,2,color="green")
>>> curve3=plot(4+x,0,2,color="blue")
>>> curve1 + curve2 + curve3

# Plots all the curves on a combined canvas.


# Alternate method :-
>>> plot(-x^2,0,2,color="red") + plot(+x^2,0,2,color="green") + plot(4+x,0,2,color="blue")

# Plots all the curves on a combined canvas.
```

### **_Scatter Plots_**

```Python
>>> data = [(0,0),(1,1),(2,2),(3,3),(4,4)]
>>> scatter_plot(data)

# Returns a Graphics object of a scatter plot containing all points in the datalist.
```

More about Scatter Plots [here](SageNotes%20Practical%201.md)

### **_Implicit Function Plotting_**

### **_Implicit Function :-_**

A mathematical function defined by means of a relation that is not solved for the function in terms of the independent variable or variables.

```Python
>>> var('x,y') # declaring variables
>>> f(x,y)=x^n+y^n-1 # declaring implicit functions, n is usually defined.
>>> implicit_plot(f,(x,-2,2),(y,-2,2),color='orange') # corresponding x and y limits are also given.
# Same attributes can be used to beautify the figure.

# "implicit_plot" takes a function of two variables, f(x, y) and plots the curve f(x,y) = 0 over the specified "xrange" and "yrange" as demonstrated below.
# "implicit_plot(f, (x,xmin,xmax), (y,ymin,ymax), ...)"
```

### **_Famous Curves_**

```Python
>>> f(x,y) = x^n+y^n-1

# n = even gives closed graph and n = odd gives open graph


>>> f(x,y) = y^2*(2-x)-x^2*(2+x)

# Famous Alpha Curve
```

### **_Parametric Plot_**

$x = f(t) , y = f'(t)$, where $t ∈ theta$

```Python
>>> var('t')
>>> parametric_plot([t*sin(1-t^2),t*cos(t^2)],(t,-2*pi,2*pi)) # Limits of t are given correspondingly.

# Plot a parametric curve or surface in 2d or 3d.
# "parametric_plot()" takes two or three functions as a list or a tuple and makes a plot with the first function giving the x coordinates, the second function giving the y coordinates, and the third function (if present) giving the z coordinates.
```

| $t*sin(1-t^2)$ | $t*cos(t^2)$ | $f(t)$                 |
| -------------- | ------------ | ---------------------- |
| x = f1(t)      | y = f2(t)    | z = f3(t) (if present) |

### **_Polar Plot_**

$r = f(t) $, where $t ∈ theta, r ∈ R$
This is similar to $y = f(x)$.

```Python
>>> var('t')
>>> polar_plot(2*(1+cos(t)),(t,-2*pi,2*pi),title='Cardioid')

# "polar_plot" takes a single function or a list or tuple of functions and plots them with polar coordinates in the given domain.

```

```Python
>>> L=[p1,p2,p3,p4] # 4 graphs
>>> G=graphics_array(L,2,2) # a 2x2 grid of p1,p2,p3,p4
>>> G.show(figsize=6)
```
