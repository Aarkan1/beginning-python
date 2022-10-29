## Exercise 6: lists and `for` loops

> * Open up a new script file. Make a variable `months = ['January', ...,
>   'December']` with all the months in order.

```python
months = [
    'January',
    'February',
    'March',
    'April',
    'May',
    'June',
    'July',
    'August',
    'September',
    'October',
    'November',
    'December',
]
```

> * Write a `for` loop to print out these month names, one on each line. Run the
>   program to make sure it works.

```python
for month in months:
    print(month)
```

> * Now expand your program with another variable (at the top level) of month lengths. Ignore any complications involving leap years.

```python
month_lengths = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]
```

> * Now make the program print all the days of the year: `January 1`, then
>   `January 2`, all the way to `December 31`. This will require an inner `for`
>   loop inside of the one you already wrote.

```python
for month, days_in_month in zip(months, month_lengths):
    for n in range(1, days_in_month + 1):   # + 1 because range endpoint is exclusive
        print(f'{month} {n}')
```

> Extra tasks (you can pick one of more of these):
>
> * If you want, plug in the `suffix` function from exercise 4 into this
>   program, so that it prints `January 1st`, etc.

After copy-pasting (or `import`ing) the `suffix` function, the `print`
statement needs to be changed to this:

```python
print(f'{month} {n}{suffix(n)}')
```

> * Check if the current year is a leap year, and if so, include `February 29`
>   among the dates printed. (This requires you to `import datetime`.)

You'll need an `if` statement:

```python
import datetime

# ...

year = datetime.date.today().year
if year % 4 == 0 and not (year % 100 == 0 and not year % 400 == 0):
    month_lengths[1] += 1   # zero-based index
```

If we don't want to own the (error-prone) leap year arithmetic ourselves,
there's also the `calendar` module:


```python
import datetime
import calendar

# ...

year = datetime.date.today().year
if calendar.isleap(year):
    month_lengths[1] += 1
```

> * Have the program print all the dates in backwards order.

We can leave the outer and inner loops in place, but run `reversed` on all the
lists that go into the loops:

```python
for month, days_in_month in zip(reversed(months), reversed(month_lengths)):
    for n in reversed(range(1, days_in_month + 1)):
        print(f'{month} {n}{suffix(n)}')
```
