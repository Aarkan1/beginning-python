## Exercise 3: finding someone's age

> Implement this program.
>
> ```python
> birth_date = 'YYYY-MM-DD'   # fill in your actual birth date here
> birth_year = int(birth_date[0:4])
>
> from datetime import *
> today = date.today()
>
> age = today.year - birth_year
> print('This year you turn', age, 'years.')
> ```
> Try running the program. Does it output the right thing?

Yes, it should. For me, it outputs 38.

For what it's worth, the biggest shortcut this script is taking is
`int(birth_date[0:4])`. It's expecting the year to be there without doing any
real string matching or error checking. That can be improved, with regular
expressions and `if` statements.

> Think about how you can extend the program to check whether it is before or
> after your birthday this year, and to compute your current age.

This works:

```python
birth_date = '1981-09-15'
birth_year = int(birth_date[0:4])
birth_month = int(birth_date[5:7])
birth_day = int(birth_date[8:10])

from datetime import *
today = date.today()
birthday_this_year = date(today.year, birth_month, birth_day)

age = today.year - birth_year
if today < birthday_this_year:
    # compensate for birthday this year being in the future
    age -= 1

print('You are currently', age, 'years old.')
```

