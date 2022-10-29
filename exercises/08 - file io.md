## Exercise 8: file I/O

* Make a script that opens up `words.txt` for reading, iterates through 
  the lines, and puts all the *five-letter* words in a list.
* Apostrophes are not letters, so make sure there are no such words in the list.
* Did you notice at the end of the list, there are some *four*-letter words?
  That's because we're still reading bytes, not characters, and that accented
  "e" counts for two bytes. Fix this by adding `encoding = 'utf-8'` to the
  `open()` call (for Python2 you would instead convert with
  `line = unicode(line, 'utf-8')`).
* Make a function `distance(w1, w2)` that counts how many letters differ
  between two words `w1` and `w2` of the same length.
* Make a function `neighbors(w1, w2)` that returns `True` if the `distance`
  between `w1` and `w2` is exactly 1. (And `False` otherwise.)
* Now loop through the list and print all the words that are `neighbors` of
  the word `'cares'`.