# TestingMPLD3

I am trying out the python package mpld3: [MPLD3 Quick Start Guide](https://mpld3.github.io/quickstart.html).

I am hoping to be able to export matplotlib graphs into HTML, trying to help out student [Nicholas Liu](https://github.com/liunicholas).

I did not have any success with this.  The pip install in python 3.7 came through with no public functions; when I run `dir(mpld3)` in a python shell, I get: `['__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__path__', '__spec__']` which does not include any of the useful functions.

When I copy-paste the simple example from the `mpld3` QuickStart Guide:
```
import matplotlib.pyplot as plt, mpld3
plt.plot([3,1,4,1,5], 'ks-', mec='w', mew=5, ms=20)
mpld3.show()
```
I get the following result (as expected):
```
Traceback (most recent call last):
  File "mpld3Test2.py", line 3, in <module>
    mpld3.show()
AttributeError: module 'mpld3' has no attribute 'show'
```
