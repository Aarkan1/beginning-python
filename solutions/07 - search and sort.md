## Exercise 7: sorting and searching

> * Write a function `is_palindrome` that, given a word `w`, returns `True` if
>   and only if `w` is equal to its reverse, `w == w[::-1]`.

```python
>>> def is_palindrome(w: str):
...   return w == w[::-1]
... 
>>> is_palindrome('abba')
True
```

> * A *square* is any integer `n ** 2` that's the product of `n` times itself.
>   Generate a list of squares of all `n < 1e6`, one million.

```python
>>> squares = [n ** 2 for n in range(int(1e6))]
>>> len(squares)
1000000
```

> * Now make a list of only those numbers from `squares` whose string value `s`
>   is a palindrome `is_palindrome(s)`. You're free to write it with either a
>   `for` loop, or a `filter` or a list comprehension, whichever pleases you.

```python
>>> palindromic_squares = [n for n in squares if is_palindrome(str(n))]
>>> len(palindromic_squares)
37
>>> palindromic_squares
[0, 1, 4, 9, 121, 484, 676, 10201, 12321, 14641, 40804, 44944, 69696, 94249, 698896,
1002001, 1234321, 4008004, 5221225, 6948496, 100020001, 102030201, 104060401, 121242121,
123454321, 125686521, 400080004, 404090404, 522808225, 617323716, 942060249,
10000200001, 10221412201, 12102420121, 12345654321, 40000800004, 637832238736]
```

> * Did it work? Then write it in one of the other ways.

```python
>>> palindromic_squares = []
>>> for n in squares:
...   if is_palindrome(str(n)):
...     palindromic_squares.append(n)
... 
>>> palindromic_squares = list(filter(lambda n: is_palindrome(str(n)), squares))
```

> * Can you take the list of palindromic squares `n ** 2` and get the original
>   numbers `n` back? There's a square root function in `math.sqrt`, but you
>   need to import it.

```python
>>> import math
>>> [math.sqrt(n) for n in palindromic_squares]
[0.0, 1.0, 2.0, 3.0, 11.0, 22.0, 26.0, 101.0, 111.0, 121.0, 202.0, 212.0, 264.0, 307.0,
836.0, 1001.0, 1111.0, 2002.0, 2285.0, 2636.0, 10001.0, 10101.0, 10201.0, 11011.0,
11111.0, 11211.0, 20002.0, 20102.0, 22865.0, 24846.0, 30693.0, 100001.0, 101101.0,
110011.0, 111111.0, 200002.0, 798644.0]
```

Note that `math.sqrt` gives back `float` values even when, as here, they all
have a zero fractional part.

> * Generate a list of all possible two-digit strings, `'00' .. '99'`, and
>   save it to a variable.

Here are two ways, one using nested loops, the other using formatting/padding:

```python
>>> two_digit_strings = [f'{m}{n}' for m in range(10) for n in range(10)]
>>> two_digit_strings = [f'{n:02d}' for n in range(100)]
```

> * What position did `'67'` end up in? Don't count, use `.index` on the list.

```python
>>> two_digit_strings.index('67')
67
```

Well, that's a bit obvious in retrospect. `:-)`

> * Use `random.sample` to pick a 'hand' of five such numbers and print it.

```python
>>> import random
>>> random.sample(two_digit_strings, 5)
['19', '91', '17', '26', '08']
```

> * Make a `while` loop that keeps picking such random hands until it gets one
>   with a 'double digit' such as `'33'`. (Hint: you can re-use `is_palindrome`
>   for this.)

```python
>>> random_hand = []
>>> while not any([s for s in random_hand if is_palindrome(s)]):
...   random_hand = random.sample(two_digit_strings, 5)
... 
>>> random_hand
['42', '51', '93', '00', '46']
```
