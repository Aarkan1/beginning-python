## Exercise 10: dictionaries

* Write a script that iterates through `words.txt` and puts all the
  five-letter words in a dictionary `words`. For each entry, the key should be
  the word itself, and the value should be an empty list.
* Now add neighbor information to those lists in the dictionary. (You'll need
  to implement or copy the `neighbors` function yourself. See exercise 8.)

```python
        for k1 in words:
            for k2 in words:
                if neighbors(k1, k2):
                    words[k1].append(k2)
```

* Quick aside: can you think of a way to add the words in sorted order without
  slowing down this nested loop too much? Ask the instructor if you're unsure.
* Now add a final loop that queries for a word and prints its neighbors:

```python
        while True:
            word = input('Enter a word: ')
            print(words[word])
```

* Can you find a path of neighboring words that connects `oiled` and `ponds`?
