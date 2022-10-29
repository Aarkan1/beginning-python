# Beginning Python - Solutions

## Exercise 1: the interactive shell

> * What's `724 + 1918`? (That is, write `724 + 1918` and hit Enter.)
> * What's `100 - 23.5`?
> * What's `16 ** 4`?
> * What's `1969 % 100`?

```
$ python3
Python 3.7.2 (default, Mar 15 2019, 11:48:22) 
[GCC 6.3.0 20170516] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 724 + 1918
2642
>>> 100 - 23.5
76.5
>>> 16 ** 4
65536
>>> 1969 % 100
69
```

> What happens when you do `math.sqrt(18)`? Try first doing `import math` and
> then computing the square root again.

It fails when the module hasn't been imported yet.

```python
>>> math.sqrt(18)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'math' is not defined
```

After importing it, it works fine.

```python
>>> import math
>>> math.sqrt(18)
4.242640687119285
```

Can also import it directly and use it without going through the module.

```python
>>> from math import sqrt
>>> sqrt(18)
4.242640687119285
```

> What happens when you do `math.sqrt(-18)`?

It fails, because `math.sqrt` doesn't appreciate negative numbers.

```python
>>> math.sqrt(-18)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: math domain error
```

It works with `cmath.sqrt`, though, which recognizes complex numbers:

```python
>>> import cmath
>>> cmath.sqrt(-18)
4.242640687119285j
```

> If you were unsure what the `str.upper` method does, what would you write?

```python
>>> help(str.upper)
```

If you were unsure what this method was called, what would you write?

```python
>>> dir(str)
```

> Also try to use the method, with something like `'abc'.upper()`.

```python
>>> 'abc'.upper()
'ABC'
```
