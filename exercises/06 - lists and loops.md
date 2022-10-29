## Exercise 6: lists and `for` loops

* Open up a new script file. Make a variable `months = ['January', ...,
  'December']` with all the months in order.
* Write a `for` loop to print out these month names, one on each line. Run the
  program to make sure it works.
* Now expand your program with another variable (at the top level) of month
  lengths. We ignore any complications involving leap years.
  ```python
  month_lengths = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]
  ```
* Now make the program print all the days of the year: `January 1`, then
  `January 2`, all the way to `December 31`. This will require an inner `for`
  loop inside of the one you already wrote.

Extra tasks (you can pick one of more of these):

* If you want, plug in the `suffix` function from exercise 4 into this
  program, so that it prints `January 1st`, etc.
* Check if the current year is a leap year, and if so, include `February 29`
  among the dates printed. (This requires you to `import datetime`.)
* Have the program print all the dates in backwards order.
