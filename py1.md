```python
from matplotlib import pyplot as plt
x = range(120)
y = [12,23,15,19,10]
plt.plot(x,y)
plt.show()
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-2-ae4ec8011bc7> in <module>
          2 x = range(120)
          3 y = [12,23,15,19,10]
    ----> 4 plt.plot(x,y)
          5 plt.show()
    

    D:\Python\Anaconda3\lib\site-packages\matplotlib\pyplot.py in plot(scalex, scaley, data, *args, **kwargs)
       2794     return gca().plot(
       2795         *args, scalex=scalex, scaley=scaley, **({"data": data} if data
    -> 2796         is not None else {}), **kwargs)
       2797 
       2798 
    

    D:\Python\Anaconda3\lib\site-packages\matplotlib\axes\_axes.py in plot(self, scalex, scaley, data, *args, **kwargs)
       1663         """
       1664         kwargs = cbook.normalize_kwargs(kwargs, mlines.Line2D._alias_map)
    -> 1665         lines = [*self._get_lines(*args, data=data, **kwargs)]
       1666         for line in lines:
       1667             self.add_line(line)
    

    D:\Python\Anaconda3\lib\site-packages\matplotlib\axes\_base.py in __call__(self, *args, **kwargs)
        223                 this += args[0],
        224                 args = args[1:]
    --> 225             yield from self._plot_args(this, kwargs)
        226 
        227     def get_next_color(self):
    

    D:\Python\Anaconda3\lib\site-packages\matplotlib\axes\_base.py in _plot_args(self, tup, kwargs)
        389             x, y = index_of(tup[-1])
        390 
    --> 391         x, y = self._xy_from_xy(x, y)
        392 
        393         if self.command == 'plot':
    

    D:\Python\Anaconda3\lib\site-packages\matplotlib\axes\_base.py in _xy_from_xy(self, x, y)
        268         if x.shape[0] != y.shape[0]:
        269             raise ValueError("x and y must have same first dimension, but "
    --> 270                              "have shapes {} and {}".format(x.shape, y.shape))
        271         if x.ndim > 2 or y.ndim > 2:
        272             raise ValueError("x and y can be no greater than 2-D, but have "
    

    ValueError: x and y must have same first dimension, but have shapes (120,) and (5,)



    
![png](output_0_1.png)
    



```python
from matplotlib import pyplot as pit
x = range(120)
y = [12,23,15,19,10]
plt.plot(x,y)

plt.show()
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-3-ed4bdfd8b640> in <module>
          2 x = range(120)
          3 y = [12,23,15,19,10]
    ----> 4 plt.plot(x,y)
          5 plt.show()
    

    NameError: name 'plt' is not defined



```python
from matplotlib import pyplot as plt
x = range(2,22,2)
y = [12,23,15,19,10]
plt.plot(x,y)
plt.show()
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-3-ccabcd98730a> in <module>
          2 x = range(2,22,2)
          3 y = [12,23,15,19,10]
    ----> 4 plt.plot(x,y)
          5 plt.show()
    

    D:\Python\Anaconda3\lib\site-packages\matplotlib\pyplot.py in plot(scalex, scaley, data, *args, **kwargs)
       2794     return gca().plot(
       2795         *args, scalex=scalex, scaley=scaley, **({"data": data} if data
    -> 2796         is not None else {}), **kwargs)
       2797 
       2798 
    

    D:\Python\Anaconda3\lib\site-packages\matplotlib\axes\_axes.py in plot(self, scalex, scaley, data, *args, **kwargs)
       1663         """
       1664         kwargs = cbook.normalize_kwargs(kwargs, mlines.Line2D._alias_map)
    -> 1665         lines = [*self._get_lines(*args, data=data, **kwargs)]
       1666         for line in lines:
       1667             self.add_line(line)
    

    D:\Python\Anaconda3\lib\site-packages\matplotlib\axes\_base.py in __call__(self, *args, **kwargs)
        223                 this += args[0],
        224                 args = args[1:]
    --> 225             yield from self._plot_args(this, kwargs)
        226 
        227     def get_next_color(self):
    

    D:\Python\Anaconda3\lib\site-packages\matplotlib\axes\_base.py in _plot_args(self, tup, kwargs)
        389             x, y = index_of(tup[-1])
        390 
    --> 391         x, y = self._xy_from_xy(x, y)
        392 
        393         if self.command == 'plot':
    

    D:\Python\Anaconda3\lib\site-packages\matplotlib\axes\_base.py in _xy_from_xy(self, x, y)
        268         if x.shape[0] != y.shape[0]:
        269             raise ValueError("x and y must have same first dimension, but "
    --> 270                              "have shapes {} and {}".format(x.shape, y.shape))
        271         if x.ndim > 2 or y.ndim > 2:
        272             raise ValueError("x and y can be no greater than 2-D, but have "
    

    ValueError: x and y must have same first dimension, but have shapes (10,) and (5,)



    
![png](output_2_1.png)
    



```python
from matplotlib import pyplot as plt
x = range(2,26,2)
y = [15,13,14,17,20,25,26,27,22,23,28,13] 
plt.figure(figsize=(20,8),dpi=80)
plt.plot(x,y)
_xtick_labels = [i/2 for i in range(2,49)]
plt.xticks(_xticks_labels)
plt.savefig("./t1.svg")
plt.show()

```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-4-fa89b3528567> in <module>
          5 plt.plot(x,y)
          6 _xtick_labels = [i/2 for i in range(2,49)]
    ----> 7 plt.xticks(_xticks_labels)
          8 plt.savefig("./t1.svg")
          9 plt.show()
    

    NameError: name '_xticks_labels' is not defined



    
![png](output_3_1.png)
    



```python
from matplotlib import pyplot as plt
x = range(2,26,2)
y = [15,13,14,17,20,25,26,27,22,23,28,13] 
plt.figure(figsize=(20,8),dpi=80)
plt.plot(x,y)
_xtick_labels = [i/2 for i in range(2,49)]
plt.xticks(_xtick_labels)
plt.savefig("./t1.svg")
plt.show()
```


    
![png](output_4_0.png)
    



```python
from matplotlib import pyplot as plt
x = range(2,26,2)
y = [15,13,14,17,20,25,26,27,22,23,28,13] 
plt.figure(figsize=(20,8),dpi=80)
plt.plot(x,y)
_xtick_labels = [i/2 for i in range(2,49)]
plt.xticks(_xticks_labels)
plt.savefig("./t1.png")
plt.show()
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-6-6e236e619bad> in <module>
          5 plt.plot(x,y)
          6 _xtick_labels = [i/2 for i in range(2,49)]
    ----> 7 plt.xticks(_xticks_labels)
          8 plt.savefig("./t1.png")
          9 plt.show()
    

    NameError: name '_xticks_labels' is not defined



    
![png](output_5_1.png)
    



```python
from matplotlib import pyplot as plt
x = range(2,26,2)
y = [15,13,14,17,20,25,26,27,22,23,28,13] 
plt.figure(figsize=(20,8),dpi=80)
plt.plot(x,y)
_xtick_labels = [i/2 for i in range(2,49)]
plt.xticks(_xtick_labels)
plt.savefig("./t1.png")
plt.show()
```


    
![png](output_6_0.png)
    



```python
from matplotlib import pyplot as plt
x = range(2,26,2)
y = [15,13,14,17,20,25,26,27,22,23,28,13] 
plt.figure(figsize=(20,8),dpi=80)
plt.plot(x,y)
_xtick_labels = [i/2 for i in range(2,49)]
plt.xticks(_xtick_labels[::3])
plt.savefig("./t1.png")
plt.show()
```


    
![png](output_7_0.png)
    



```python
from matplotlib import pyplot as plt
x = range(2,26,2)
y = [15,13,14,17,20,25,26,27,22,23,28,13] 
plt.figure(figsize=(20,8),dpi=80)
plt.plot(x,y)
_xtick_labels = [i/2 for i in range(2,49)]

plt.xticks(_xtick_labels[::3])
plt.yticks(range(min(y),max(y)+1))
plt.savefig("./t1.png")
plt.show()
```


    
![png](output_8_0.png)
    



```python
from matplotlib import pyplot as plt
x = range(2,26,2)
y = [15,13,14,17,20,25,26,27,22,23,28,13] 
plt.figure(figsize=(20,8),dpi=80)
plt.plot(x,y)
_xtick_labels = [i/0.5 for i in range(2,49)]
plt.xticks(_xtick_labels)
plt.savefig("./t1.png")
plt.show()
```


    
![png](output_9_0.png)
    



```python
from matplotlib import pyplot as plt
import random
a =[random.randint(20,35) for i in range(120)]
x = range(0,120)
y = a
plt.figure(figsize=(20,8),dpi=80)
plt.plot(x,y)
plt.show()
```


    
![png](output_10_0.png)
    



```python
from matplotlib import pyplot as plt
import random
a =[random.randint(20,35) for i in range(120)]
x = range(0,120)
y = a
plt.figure(figsize=(20,8),dpi=80)
plt.plot(x,y)


_x_ticks_labels  =["10:{}".format(i) for i in range(60)]
_x_ticks_labels +=["11:{}".format(i) for i in range(60)]
plt.xticks(x[::3],_xtick_labels[::3])

plt.show()
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-17-8c4a4d3d1f29> in <module>
          8 
          9 
    ---> 10 _x_ticks_labels  =["10:{}".fomat(i) for i in range(60)]
         11 _x_ticks_labels +=["11:{}".fomat(i) for i in range(60)]
         12 plt.xticks(x[::3],_xtick_labels[::3])
    

    <ipython-input-17-8c4a4d3d1f29> in <listcomp>(.0)
          8 
          9 
    ---> 10 _x_ticks_labels  =["10:{}".fomat(i) for i in range(60)]
         11 _x_ticks_labels +=["11:{}".fomat(i) for i in range(60)]
         12 plt.xticks(x[::3],_xtick_labels[::3])
    

    AttributeError: 'str' object has no attribute 'fomat'



    
![png](output_11_1.png)
    



```python
from matplotlib import pyplot as plt
import random
import matplotlib

a =[random.randint(20,35) for i in range(120)]
x = range(0,120)
y = a
plt.figure(figsize=(20,8),dpi=80)
plt.plot(x,y)


_xtick_labels  =["10:{}".format(i) for i in range(60)]
_xtick_labels +=["11:{}".format(i) for i in range(60)]
plt.xticks(x[::3],_xtick_labels[::3],rotation=45)
plt.xlabel("Time")
plt.ylabel("Temperature")
plt.title("The Temperature Variation Every Minute From 10am. To 11am.")
plt.show()

```


    
![png](output_12_0.png)
    



```python
from matplotlib import pyplot as plt
import random 

x = range(0,30)
y =[random.randint(0,10) for i in range(30)]

plt.figure(figsize=(20,8),dpi=80)
plt.plot(x,y)

plt.xticks(x)

plt.xlabel("ages")
plt.ylabel("how many gf/bf have you got")
plt.title("Relationship")
plt.show()

```


    
![png](output_13_0.png)
    



```python
from matplotlib import pyplot
import random
from matplotlib import font_manager

x1=range(0,10)
y1=[random.randint(0,50) for i in range(10)]

x2=range(30,40)
y2=[random.randint(4,60) for  i in range(10)]

plt.scatter(x1,y1)
plt.scatter(x2,y2)


_x = list(x1)+list(x2)
_xtick_labels = ["day{}".format(i)for i in x1]
_xtick_labels +=["day{}".format(i)for i in x2]



plt.xticks(_x,_xtick_labels)
```




    ([<matplotlib.axis.XTick at 0x1cefd72bfc8>,
      <matplotlib.axis.XTick at 0x1cefcc1b888>,
      <matplotlib.axis.XTick at 0x1cefbec82c8>,
      <matplotlib.axis.XTick at 0x1cefc7c9848>,
      <matplotlib.axis.XTick at 0x1cefc6a1508>,
      <matplotlib.axis.XTick at 0x1cefccf1dc8>,
      <matplotlib.axis.XTick at 0x1cefccf1a88>,
      <matplotlib.axis.XTick at 0x1cefccf1248>,
      <matplotlib.axis.XTick at 0x1cefd71f208>,
      <matplotlib.axis.XTick at 0x1cefd71f5c8>,
      <matplotlib.axis.XTick at 0x1cefde2e408>,
      <matplotlib.axis.XTick at 0x1cefde2e688>,
      <matplotlib.axis.XTick at 0x1cefd70d708>,
      <matplotlib.axis.XTick at 0x1cefcc19848>,
      <matplotlib.axis.XTick at 0x1cefcc19788>,
      <matplotlib.axis.XTick at 0x1cefde2e288>,
      <matplotlib.axis.XTick at 0x1cefcb6ab88>,
      <matplotlib.axis.XTick at 0x1cefcc06b48>,
      <matplotlib.axis.XTick at 0x1cefda56f88>,
      <matplotlib.axis.XTick at 0x1cefda56588>],
     <a list of 20 Text xticklabel objects>)




    
![png](output_14_1.png)
    



```python

```
