## Exercise 3: finding someone's age

Implement this program.

```python
birth_date = 'YYYY-MM-DD'   # fill in your actual birth date here
birth_year = int(birth_date[0:4])

from datetime import *
today = date.today()

age = today.year - birth_year
print('This year you turn ' + age + ' years.')
```

Try running the program. Does it output the right thing?

Think about how you can extend the program to check whether it is before or
after your birthday this year, and to compute your current age.
