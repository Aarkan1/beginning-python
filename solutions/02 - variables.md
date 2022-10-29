## Exercise 2: variables and types

> If you do the following on the interactive shell
>
>     >>> x = 5
>     >>> y = x
>     >>> x += 8
>
> What are the values of `x` and `y` after this?

```python
>>> x
13
>>> y
5
```

(`x` and `y` are unrelated; the `x += 8` binds `x` to a new `int`, but not `y`.
The `y = x` was a _copy_ of the `int`.)

> If you do
>
>     >>> a = [1, 2]
>     >>> b = a
>     >>> a += [3, 4]
>
> What are the values of `a` and `b`? (Also try running `id(a)` and `id(b)`.)

```python
>>> a
[1, 2, 3, 4]
>>> b
[1, 2, 3, 4]
>>> id(a)
139746040352968
>>> id(b)
139746040352968
```

The exact numbers for the `id`s will vary in your environment, but they will be
the same for `a` and `b`.

(`a` and `b` are related; the `a += [3, 4]` doesn't bind `a` to a new `list`,
but extends the existing one, which is also bound by `b`. The `b = a` was a
_copy_ of the _reference_ to the list created in `a = [1, 2]`. Therefore, both
`a` and `b` refer to the same `list` in memory.)

> Make a Python program file with the following two lines:
>
> ```python
> x = 7.0
> print(x ** 2 - x - 6)
> ```
>
> Run the program. Is there a value of `x` that will make the expression evaluate
> to `0`? Try to change it and re-run the program.

While we can certainly do this by trial-and-error, and eventually run into the
two roots 3.0 and -2.0...

```python
>>> x = 3.0
>>> print(x ** 2 - x - 6)
0.0
>>> x = -2.0
>>> print(x ** 2 - x - 6)
0.0
```

...it does require an element of luck, and we might not want to depend on luck.

Instead, we could "carpet bomb" a range of values to find the roots:

```python
>>> [(x, x ** 2 - x - 6) for x in range(-5, 5)]
[(-5, 24), (-4, 14), (-3, 6), (-2, 0), (-1, -4),
 (0, -6), (1, -6), (2, -4), (3, 0), (4, 6)]
```

But even that requires that the roots are found at the integers. The one
fail-safe way is to plug the coefficients into the quadratic formula:

```python
>>> from math import sqrt
>>> def quadratic_formula(p, q):
...   d = sqrt(p ** 2 / 4 - q)
...   return -p/2 + d, -p/2 - d
... 
>>> quadratic_formula(-1, -6)
(3.0, -2.0)
```
