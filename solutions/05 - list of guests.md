## Exercise 5: Printing a list of guests

> * Make a list of the following five guests, and put it in a variable `guests`:
>     * 'Mr. Ratchett'
>     * 'Mr. Bouc'
>     * 'Mrs. Hubbard'
>     * 'Mr. Michel'
>     * 'Miss Ohlsson'

```python
>>> guests = ['Mr. Ratchett', 'Mr. Bouc', 'Mrs. Hubbard',
...           'Mr. Michel', 'Miss Ohlsson']
```

> * Make a `for` loop that prints all five names in the `guest` list.

```python
>>> for guest in guests:
...   print(guest)
... 
Mr. Ratchett
Mr. Bouc
Mrs. Hubbard
Mr. Michel
Miss Ohlsson
```

> * Before the `for` loop, use `guests.append` to add a `'Mr. Foscarelli'` to the
>   list.

```python
>>> guests.append('Mr. Foscarelli')
```

> * Find ways, using the slice syntax, to print:
>     * Just the first three names of the list.

```python
>>> guests[:3]
['Mr. Ratchett', 'Mr. Bouc', 'Mrs. Hubbard']
```

> * Just the last two names of the list.

```python
>>> guests[-2:]
['Miss Ohlsson', 'Mr. Foscarelli']
```

> * Every other name in the list.

Either we mean "all the names _besides_ the first three and the last two"...

```python
>>> guests[3:-2]
['Mr. Michel']
```

...or (more likely), we mean "all the names with an even index":

```python
>>> guests[::2]
['Mr. Ratchett', 'Mrs. Hubbard', 'Miss Ohlsson']
```

(We get the odd-indexed guests by starting at 1.)

```python
>>> guests[1::2]
['Mr. Bouc', 'Mr. Michel', 'Mr. Foscarelli']
```
