## Exercise 8: file I/O

> * Make a script that opens up `words.txt` for reading, iterates through the
>   lines, and puts all the *five-letter* words in a list.

```python
fives = []

with open('words.txt') as f:
    for line in f:
        line = line.rstrip()
        if len(line) != 5:
            continue
        fives.append(line)
```

> * Apostrophes are not letters, so make sure there are no such words in the
>   list.

We can add another `if` statement inside the for loop that filters out this case:

```python
for line in f:
    # ...same as before...
    if "'" in line:
        continue
    fives.append(line)
```

> * Did you notice at the end of the list, there are some *four*-letter words?
>   That's because we're still reading bytes, not characters, and that accented
>   "e" counts for two bytes. Fix this by adding `encoding = 'utf-8'` to the
>   `open()` call (for Python2 you would instead convert with
>   `line = unicode(line, 'utf-8')`).

```python
open('words.txt', encoding='utf-8')
```

> * Make a function `distance(w1, w2)` that counts how many letters differ
>   between two words `w1` and `w2` of the same length.

```python
def distance(w1, w2):
    score = 0
    for c1, c2 in zip(w1, w2):
        if c1 != c2:
            score += 1
    return score
```

Or, if we prefer the FP/list comprehension approach:

```python
def distance(w1, w2):
    return sum([1 for c1, c2 in zip(w1, w2) if c1 != c2])
```

> * Make a function `neighbors(w1, w2)` that returns `True` if the `distance`
>   between `w1` and `w2` is exactly 1. (And `False` otherwise.)

```python
def neighbors(w1, w2):
    return distance(w1, w2) == 1
```

> * Now loop through the list and print all the words that are `neighbors` of
>   the word `'cares'`.

```python
>>> for word in fives:
...     if neighbors('cares', word):
...         print(word)
... 
bares
cages
cakes
canes
capes
cards
cared
caret
carps
carts
cases
caves
cores
cures
dares
fares
hares
mares
pares
rares
tares
wares
```
