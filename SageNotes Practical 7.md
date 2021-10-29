# **_SageMath Notes :-_**

# Curve Fitting using SageMath

---

```Python
#! Legend

>>> Input   #Comments

Output
```

### **_Syntax to fit a curve_**


```Python
>>> data = [(71,69), (68,72), (73,70), (69,70), (67,68), (65,67), (66,68),(67,64)]
>>> show(data)

[(71, 69) , (68, 72) , (73, 70) , (69, 70) , (67, 68) , (65, 67) , (66, 68) , (67, 64)]


>>> point(data, color="lime", size=20, legend_label="Scatter Plot")

# Scatter Plot of all the points in the data list.

# Defining the curve we want to fit on the data.
>>> a,b = var('a,b')
>>> y(x) = a + b*x

>>> f = find_fit(data,y)
>>> show(f)

# returns the value of parameters a and b if available c.
[a = 39.54545454553874, b = 0.42424242424116654]


# Creating the function of the parameterized curve.

>>> model = y.subs(f1) 
>>> model


x |--> 0.42424242424116654*x + 39.54545454553874

# Plotting the model curve.

>>> plot(model, color="red", legend_label="Model Curve")
```