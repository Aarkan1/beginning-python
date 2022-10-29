## Exercise 2: variables and types

If you do the following on the interactive shell

```python
>>> x = 5
>>> y = x
>>> x += 8
```

What are the values of `x` and `y` after this?

If you do

```python
>>> a = [1, 2]
>>> b = a
>>> a += [3, 4]
```

What are the values of `a` and `b`? (Also try running `id(a)` and `id(b)`.)

Make a Python program file with the following two lines:

```python
x = 7.0
print(x ** 2 - x - 6)
```

Run the program. Is there a value of `x` that will make the expression evaluate
to `0`? Try to change it and re-run the program.
