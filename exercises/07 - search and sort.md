## Exercise 7: sorting and searching

* Write a function `is_palindrome` that, given a word `w`, returns `True` if
  and only if `w` is equal to its reverse, `w == w[::-1]`.
* A *square* is any integer `n ** 2` that's the product of `n` times itself.
  Generate a list of squares of all `n < 1e6`, one million.
* Now make a list of only those numbers from `squares` whose string value `s`
  is a palindrome `is_palindrome(s)`. You're free to write it with either a
  `for` loop, or a `filter` or a list comprehension, whichever pleases you.
* Did it work? Then write it in one of the other ways.
* Can you take the list of palindromic squares `n ** 2` and get the original
  numbers `n` back? There's a square root function in `math.sqrt`, but you
  need to import it.
* Generate a list of all possible two-digit strings, `'00' .. '99'`, and
  save it to a variable.
* What position did `'67'` end up in? Don't count, use `.index` on the list.
* Use `random.sample` to pick a "hand" of five such numbers and print it.
* Make a `while` loop that keeps picking such random hands until it gets one
  with a "double digit" such as `'33'`. (Hint: you can re-use `is_palindrome`
  for this.)
