## Exercise 10: dictionaries

> * Write a script that iterates through `words.txt` and puts all the
>   five-letter words in a dictionary `words`. For each entry, the key should be
>   the word itself, and the value should be an empty list.

```python
words = {}

with open('words.txt', encoding='utf-8') as f:
    for line in f:
        line = line.rstrip()
        if "'" in line:
            continue
        if len(line) != 5:
            continue
        words[line] = []
```

> * Now add neighbor information to those lists in the dictionary. (You'll need
>   to implement or copy the `neighbors` function yourself. See exercise 8.)
> 
>             for k1 in words:
>                 for k2 in words:
>                     if neighbors(k1, k2):
>                         words[k1].append(k2)

See above.

> * Quick aside: can you think of a way to add the words in sorted order without
>   slowing down this nested loop too much? Ask the instructor if you're unsure.

First off, from Python 3.7 and onward, the words will be in insertion order
already, which is also sorted order in this case.

Secondly, if that weren't the case (for example in an older version of Python),
we would do best to sort _outside_ of any loop:

```python
sorted_words = sorted(words.keys())
for k1 in sorted_words:
    for k2 in sorted_words:
        # loop body identical
```

> * Can you find a path of neighboring words that connects `oiled` and `ponds`?

We can rely on brute-force search, and with some luck find a path:

```python
Enter a word: oiled
['ailed', 'filed', 'ogled', 'piled', 'riled', 'tiled', 'wiled']
Enter a word: piled
['ailed', 'filed', 'oiled', 'paled', 'piked', 'piles', 'pined',
 'piped', 'poled', 'riled', 'tiled', 'wiled']
Enter a word: pined
['dined', 'fined', 'lined', 'mined', 'piked', 'piled', 'pines',
 'piped', 'wined']
Enter a word: pines
['Hines', 'dines', 'fines', 'lines', 'mines', 'nines', 'panes',
 'penes', 'pikes', 'piles', 'pined', 'pings', 'pinks', 'pints',
 'pipes', 'pones', 'tines', 'vines', 'wines']
Enter a word: pones
['Jones', 'bones', 'cones', 'hones', 'panes', 'penes', 'pines',
 'pokes', 'poles', 'ponds', 'popes', 'pores', 'poses', 'poxes',
 'tones', 'zones']
```
