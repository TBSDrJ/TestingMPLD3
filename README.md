# TestingMPLD3

I am trying out the python package mpld3: [MPLD3 Quick Start Guide](https://mpld3.github.io/quickstart.html).

I am hoping to be able to export matplotlib graphs into HTML, trying to help out student [Nicholas Liu](https://github.com/liunicholas).

I hd some issues, but that turns out to be because I decided to name my Django project 'mpld3' which is the same as the name of the module.  So, this creates three nested folders, all named 'mpld3' and, in the innermost one, places a file called `__init__.py`.  The problem with that is, if you are in the middle one, and execute the command `import mpld3`, python detects the subfolder as the module to be imported, not the installed module.

And then you get the result below:

>I did not have any success with this.  The pip install in python 3.7 came through with no public functions; when I run `dir(mpld3)` in a python shell, I get: `['__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__path__', '__spec__']` which does not include any of the useful functions.

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
