## Exercise 4: ordinal suffix calculator

> * Create a file with the content found at the bottom of this exercise.
> * Run the program with the argument `test` to see the only test fail.
> * Now go into the `suffix` function and add code to get the first test to pass.

The simplest thing we can do is to make the function return `'st'`:

```python
def suffix(n):
    return 'st'
```

> * Add the following assertions, *one by one*, run the program to watch them fail,
>   and then fix the program to make them pass:
>     * `self.assertEqual('nd', suffix(2))`
>     * `self.assertEqual('rd', suffix(3))`
>     * `self.assertEqual('th', suffix(4))`
>     * `self.assertEqual('th', suffix(5))`

We can get there by _successively_ adding special cases, and it would look like
this at the end:

```python
def suffix(n):
    if n == 2:
        return 'nd'
    elif n == 3:
        return 'rd'
    elif n == 4:
        return 'th'
    elif n == 5:
        return 'th'
    else:
        return 'st'
```

> * Look at your program so far and see if there's anything you can do to improve
>   it, while still keeping all the tests working.

Here's one way to simplify the program at this point:

```python
def suffix(n):
    if n == 1:
        return 'st'
    elif n == 2:
        return 'nd'
    elif n == 3:
        return 'rd'
    else:
        return 'th'
```

> * Now add the following assertions, one by one, implementing as you go:
>     * `self.assertEqual('th', suffix(11))`
>     * `self.assertEqual('th', suffix(12))`
>     * `self.assertEqual('th', suffix(13))`
>     * `self.assertEqual('st', suffix(21))`
>     * `self.assertEqual('nd', suffix(22))`

To make these tests pass, we can turn the program into this:

```python
def suffix(n):
    s = str(n)
    if s.endswith('1') and n != 11:
        return 'st'
    elif s.endswith('2') and n != 12:
        return 'nd'
    elif n == 3:
        return 'rd'
    else:
        return 'th'
```

(`str.endswith` is just one way to check the one's digit of an integer. `n %
10` would also work, for example.)

Yes, as you can clearly see, we're missing a test case to generalize the third
`if` condition. That would require one more test (`n == 23`).

> * Well done! Try running the program passing in an argument such as `411` or
>   `562`. Does it output what you expected?

It doesn't, so we need to improve the code a bit further, giving this:

```python
def suffix(n):
    s = str(n)
    if s.endswith('1') and not s.endswith('11'):
        return 'st'
    elif s.endswith('2') and not s.endswith('12'):
        return 'nd'
    elif s.endswith('3') and not s.endswith('13'):
        return 'rd'
    else:
        return 'th'
```


Create a file with the following content as a start.

```py
import sys
import unittest


def suffix(n):
    return None


class Test(unittest.TestCase):
    def test_suffix(self):
        self.assertEqual(suffix(1), 'st')


script_name = sys.argv[0]
arguments = sys.argv[1:]

USAGE = 'Usage: {0} <number>'.format(script_name)

if len(arguments) == 0 or len(arguments) > 1:
    print(USAGE)
elif arguments[0] == 'test':
    if __name__ == '__main__':
        unittest.main()
else:
    number = int(arguments[0])
    suffix = suffix(number)
    print('{0}{1}'.format(number, suffix))
```