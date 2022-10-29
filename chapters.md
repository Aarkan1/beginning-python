Chapters

Agenda:

Day 1

-   Introduction
-   What is Python?
-   The interactive prompt
-   Variables
-   Data types
-   Working with scripts
    -   IDE - PyCharm, Visual Studio Code
    -   vs code extension - Python
-   Flow of control: if and while
-   Lists and for-loops
-   Breaking out of a loop
-   Search and sort

Day 2

-   Input och output
-   Formatting
-   Functions
-   Dictionaries
-   List comprehensions
-   Classes and objects
-   Inheritance

Day 3

-   Exceptions
-   Regular expressions
-   Modules and packages
-   Debugging
-   Databases
-   GUI-development

Table of content

- [Introduction](#introduction)
- [What is Python?](#what-is-python)
- [The interactive prompt](#the-interactive-prompt)
  - [You can always write help() in the shell.](#you-can-always-write-help-in-the-shell)
- [Exercise 1](#exercise-1)
- [Working with scripts](#working-with-scripts)
- [Use Python with Visual Studio Code](#use-python-with-visual-studio-code)
- [Variables](#variables)
  - [The type() function](#the-type-function)
  - [Variable naming](#variable-naming)
  - [Values and references](#values-and-references)
- [Exercise 2](#exercise-2)
- [Data types](#data-types)
  - [Booleans](#booleans)
  - [Converting things to bool](#converting-things-to-bool)
  - [Numbers](#numbers)
  - [Converting between number formats](#converting-between-number-formats)
  - [Converting To Numbers](#converting-to-numbers)
  - [Strings](#strings)
    - [Example: appending a string](#example-appending-a-string)
    - [Example: prepending a string](#example-prepending-a-string)
    - [Example: repeating a string](#example-repeating-a-string)
    - [Example: substrings](#example-substrings)
    - [Example: replacing substrings](#example-replacing-substrings)
    - [Example: checking whether something is a substring](#example-checking-whether-something-is-a-substring)
  - [String formatting](#string-formatting)
- [Exercise 3](#exercise-3)
- [Flow of control: if and while](#flow-of-control-if-and-while)
  - [Example: check odd or even](#example-check-odd-or-even)
  - [while loops](#while-loops)
  - [Model of computation: input/computation/output](#model-of-computation-inputcomputationoutput)
  - [The main script](#the-main-script)
- [Exercise 4](#exercise-4)
- [Lists and for-loops](#lists-and-for-loops)
  - [Adding things to a list](#adding-things-to-a-list)
  - [Removing things from a list](#removing-things-from-a-list)
  - [Get the length a list](#get-the-length-a-list)
  - [Slicing a list](#slicing-a-list)
  - [For loops](#for-loops)
    - [Example: summing a list of values (manually)](#example-summing-a-list-of-values-manually)
    - [Example: summing a list of values (builtin)](#example-summing-a-list-of-values-builtin)
    - [Ranges](#ranges)
    - [Looping over indexes and values](#looping-over-indexes-and-values)
    - [Example: checking for elements](#example-checking-for-elements)
- [Exercise 5](#exercise-5)
  - [List comprehensions](#list-comprehensions)
  - [Split string](#split-string)
  - [Join list of strings into a big string](#join-list-of-strings-into-a-big-string)
  - [Breaking out of a loop](#breaking-out-of-a-loop)
  - [Get the index of an item in a list](#get-the-index-of-an-item-in-a-list)
- [Exercise 6](#exercise-6)
  - [Example: number guessing game](#example-number-guessing-game)
  - [Sort a list](#sort-a-list)
  - [Reverse a list](#reverse-a-list)
- [Exercise 7](#exercise-7)
- [Input och output](#input-och-output)
  - [Example: finding palindromes in a word list](#example-finding-palindromes-in-a-word-list)
  - [Writing files](#writing-files)
- [Exercise 8](#exercise-8)
  - [Using file as a small database](#using-file-as-a-small-database)
- [Formatting](#formatting)
  - [Other useful formatting tricks](#other-useful-formatting-tricks)
- [Exercise 11](#exercise-11)
- [Functions](#functions)
  - [Creating a Function](#creating-a-function)
  - [Arguments](#arguments)
  - [Number of Arguments](#number-of-arguments)
  - [Arbitrary Arguments, \*args](#arbitrary-arguments-args)
  - [Keyword Arguments](#keyword-arguments)
  - [Arbitrary Keyword Arguments, \*\*kwargs](#arbitrary-keyword-arguments-kwargs)
  - [Default Parameter Value](#default-parameter-value)
  - [Return Values](#return-values)
  - [The pass Statement](#the-pass-statement)
- [Exercise 9](#exercise-9)
- [Dictionaries](#dictionaries)
  - [Looping over the keys of a dictionary](#looping-over-the-keys-of-a-dictionary)
  - [Sorting the keys and looping over them](#sorting-the-keys-and-looping-over-them)
- [Looping over the values of a dictionary](#looping-over-the-values-of-a-dictionary)
  - [Sorting the values and looping over them](#sorting-the-values-and-looping-over-them)
- [Exercise 10](#exercise-10)
- [List comprehensions](#list-comprehensions-1)
  - [List comprehensions: mapping](#list-comprehensions-mapping)
  - [List comprehensions: filtering](#list-comprehensions-filtering)
  - [List comprehensions: joining](#list-comprehensions-joining)
  - [Set comprehensions](#set-comprehensions)
  - [Dictionary comprehensions](#dictionary-comprehensions)
  - [Comprehension Gotchas: Clause Order](#comprehension-gotchas-clause-order)
- [Classes and objects](#classes-and-objects)
  - [Recap: data structures are pretty great](#recap-data-structures-are-pretty-great)
  - [Inheritance](#inheritance)
  - [Three types of method](#three-types-of-method)
- [Exercise 12](#exercise-12)
- [Exceptions](#exceptions)
  - [Raise an exception](#raise-an-exception)
  - [Catch an exception](#catch-an-exception)
- [Regular expressions](#regular-expressions)
  - [Example: finding a particular word in a text](#example-finding-a-particular-word-in-a-text)
  - [Example: finding, case-insensitive](#example-finding-case-insensitive)
- [Exercise 13](#exercise-13)
- [Modules and packages](#modules-and-packages)
- [Debugging](#debugging)
  - [Live demo](#live-demo)
- [Exercise 14](#exercise-14)
- [Databases](#databases)
  - [A brief discussion of databases](#a-brief-discussion-of-databases)
  - [SQLite](#sqlite)
  - [Native Drivers](#native-drivers)
  - [SQLite helper](#sqlite-helper)
  - [SQLite helper examples](#sqlite-helper-examples)
- [GUI-development](#gui-development)
 

## Introduction

Many people find it helpful to learn a scripting language these days. Python is one of the more mature ones out there, with a strong tradition, a helpful community, and a massive set of ready-to-use modules. Thus, increasing your knowledge about Python means getting a further reach in solving many everyday problems.

Programming, for all the uses we can put it to, has its own set of challenges and hard points. Python stands out among languages as unusually sane and beginner-friendly. Despite this, it can be used to solve a wide range of problems, everything from the mundane to the intricate. The course is filled with real-world examples which you can apply directly to your work.

No matter whether Python is your first programming language or you already have some other languages under your belt, this course is an accessible introduction to Python and solving problems with a scripting language.

This course targets Python 3.

## What is Python?

Python is a general-purpose scripting and programming language. It is easy to learn, powerful, and versatile.

Python is commonly used for **developing websites and software, task automation, data analysis, and data visualization**. Since it's relatively easy to learn, Python has been adopted by many non-programmers such as accountants and scientists, for a variety of everyday tasks, like organizing finances.

The "Zen of Python" is captured in a few aphorisms like the following.

Beautiful is better than ugly
Explicit is better than implicit
Simple is better than complex
Complex is better than complicated
Readability counts
For the full list, do this in the interactive shell:

```py
>>> import this
```

## The interactive prompt

Start the interactive shell by typing `python3` in the terminal.

Demo 1: calculator
You're in a restaurant, and the digital checkout system has broken down, so you need to compute the sales tax (20%) and tip (10%) yourself.

```py
>>> price = 215
>>> with_tax = price * 1.20
>>> with_tip = with_tax * 1.10
>>> with_tip
283.8
```

In this case, we could make good use of the `_` variable (representing the result of the last evaluation) to not have to name our intermediate values.

Demo 2: days to christmas
Anyone know how many days until christmas?

Let's use the interactive shell to check.

```py
>>> from datetime import date
>>> today = date.today()
>>> xmas = date(2022, 12, 24)
>>> delta = xmas - today
>>> delta.days
```

date objects can be subtracted from each other. The result is a timedelta object, which we can ask for .days.

### You can always write help() in the shell.

Whenever you wonder what a class or function or method does, you can always use `help()` in the interactive shell.

```py
>>> help(dict)
>>> help(len)
>>> help(list.append)
```

This documentation is great. Later we'll look at how you can write documentation for your own programs, so that others can do help() when they try to understand how to use your library.

## Exercise 1

## Working with scripts

Of course, not everything fits the explorative mode of the interactive shell. As soon as we move on to putting code in files, we find ourselves juggling two concerns:

Does it do what it should? This part is about correctness; have we given the machine the right steps?

Is it readable? Could a colleague come and pick up our work just by reading the code? Could we in six months? This part is about intent.

~~

Cowboy programmers write messy code that works. Purists write clean code that doesn't get used. But you are neither; you're a professional. Your goal is to write clean code that works, keeping correctness and readability in mind at the same time.

## Use Python with Visual Studio Code

To use Python with Visual Studio Code you'll have to do some setup first.

Install VS Code and after that the Python extension.

Open Command Palette [ctrl-shift-p] and write "Python: Select Interpreter". Choose the latest version.

Create a new python file, like `app.py`.
Add `print("Hello World")` to that file.

Press the play button in the upper right corner and see if "Hello World" gets printed in the integrated terminal.

## Variables

### The type() function

Every value belongs to a type of similar values with similar capabilities. You can use type() to query the type of something.

```py
type('forty-two')     # <type 'str'>
type(False)           # <type 'bool'>
type(42)              # <type 'int'>
type(42.0)            # <type 'float'>
type([4, 2])          # <type 'list'>
type({})              # <type 'dict'>
type(max)             # <type 'builtin_function_or_method'>
type(list.append)     # <type 'method_descriptor'>
```

Variables are names bound to values.

```py
>>> x = 42
>>> x
42
```

Variables (as opposed to constants, which Python doesn't have) can change their value at any time. The new value doesn't even have to be of the same type.

```py
>>> x = 'OH HAI'
>>> x
'OH HAI'
```

### Variable naming

Over the years, I've seen students botch up naming completely, naming their variables monkey, cat and gnu because they couldn't think of anything better. I'm counting on you to do better than them. :-)

~

Furthermore, except in very special circumstances, I'm counting on you not to name your variables with these names:

data
value
(Everything is data and values!)

Try to be specific and informative. Use whole words.

### Values and references

Strings, booleans, and numbers are value types; their identity is deeply tied to their value, and never changes. You can't change 5 to something else.

The bigger types of things like functions, lists and objects are known as reference types. A reference can be thought of as an address in memory. Two objects can have exactly the same contents and still be different because they have different references.

~

More seriously, if two different variables are holding on to the same reference, then one variable will "see" the other one's changes. This is known as aliasing, and is a source of tricky bugs.

```py
>>> y = ['OH', 'HAI']
>>> x = y
>>> x[1] = 'NOES'
>>> y
['OH', 'NOES']
```

## Exercise 2

## Data types

### Booleans

Let's start with the simplest type first: a boolean is either True or False. It is often the result of comparisons.

```py
>>> 3 < 4
True
>>> 'books' > 'cakes'
False
>>> 'lorem ipsum'.split() == ['lorem', 'ipsum']
True
```

We can build bigger boolean expressions from smaller ones with `not B`, `B1 or B2`, and `B1 and B2`.

### Converting things to bool

Because the boolean type is so simple, anything can be converted to it.

```py
print(bool(''))      # False   |   print(bool(0))      # False
print(bool('hi'))    # True    |   print(bool(1))      # True
                               |
print(bool([]))      # False   |   print(bool({}))     # False
print(bool([4, 5]))  # True    |   print(bool({'hi'})) # True
```

Do you see the pattern here? "Empty" values of a type convert to `False`, the rest to `True`.

We don't need to convert to `bool` so often. The most common place we'll find boolean evaluation is the condition of an `if` statement; in this case, Python does the conversion for us.

### Numbers

Numbers take three forms in Python:

-   `int` — integers limited by some machine size (32 or 64 bits)
-   `long` — integers which are not
-   `float` — real numbers, saved to some precision
-   `complex` — complex numbers, not automatically cast

Usually, you will find yourself using `int` in your programs. The `float` type is occasionally useful for simulations and iterative problems.

We combine numbers with the usual operators: addition (`+`), subtraction (`-`), multiplication (`*`), and division (`/`). There's also exponentiation (`**`) and modulo (`%`) for those extra-special circumstances.

### Converting between number formats

You can convert freely between all the number formats.

```py
>>> int(42.7)
42
>>> long(1000)
1000L
>>> float(0L)
0.0
```

### Converting To Numbers

You can also convert strings to numbers, but not many other things.

```py
>>> int('404')
404
>>> int([1, 2, 7])
TypeError: int() argument must be
a string or a number, not 'list'
```

Objects can provide their own casts though this can be dangerous.

### Strings

There are several ways we can write a string literal in Python:

```py
'single-quoted'     "double-quoted"

'need to escape "apostrophes" (\') in single-quoted strings'
"and 'quote characters' (\") in double quoted strings"

"""multi line string. can be either single-quoted
or double-quoted.  Usually used as documentation at the
top of functions."""

r'raw string'
```

Python itself tends to output strings with single quotes, but I kinda like the double quotes, because then I can use apostrophes inside of them without having to escape them.

Python raw string treats backslash (`\`) as a literal character. This is useful when we want to have a string that contains backslash and don’t want it to be treated as an escape character.

Both addition (`+`) and multiplication (`*`) works on strings.

```py
> 'This ' + 'that'
'This that'

> 'This ' * 3
'This This This '
```

#### Example: appending a string

We can simply use the += operator to add a string at the end of another.

```py
description = 'comic'
description += '-esque'

print(description)   # 'comic-esque'
```

The longer form, `description = description + '-esque'`, would have worked just as well.

#### Example: prepending a string

Adding a string to the beginning of another is also easy. We again use +.

```py
hobby = 'dancing'
hobby = 'pseudo-' + hobby

print(hobby)         # 'pseudo-dancing'
```

We cannot use `+=` in this case, as that would mean `hobby = hobby + 'pseudo-'`, which would append the string, not prepend it.

#### Example: repeating a string

Sometimes we want to repeat the same string a number of times. We can do this by using multiplication (`*`) on strings.

```py
print('#' * 5)
```

The order here doesn't matter: both `str * int` and `int * str` work.

#### Example: substrings

Strings are sequences of characters. There's a slice syntax that allows us to pull out single characters, or any number of characters from a bigger string.

```py
thing = 'The Andromeda Galaxy'

print(thing[4])      # 'A'
print(thing[:3])     # 'The'
print(thing[4:13])   # 'Andromeda'
print(thing[14:])    # 'Galaxy'
```

Technically, it's only a slice if it has a colon (`:`) in it, and so the `thing[4]` is an indexing, not a slice.

Later, we will see how exactly the same syntax works on lists. Two for one!

#### Example: replacing substrings

You can't change a string once it's been created. (Strings are immutable.) So the slice syntax doesn't help us when we want to replace substrings.

```py
>>> name = 'Edna Norris'
>>> name[:4] = 'Chuck'
[...]
TypeError: 'str' object does not support item assignment
```

Instead, we use `.replace` to produce a new string with the substring replaced.

```py
name = 'Edna Norris'
print(name.replace('Edna', 'Chuck'))   # 'Chuck Norris'
print(name)                            # 'Edna Norris', still
```

#### Example: checking whether something is a substring

There's a cute little operator, in, for checking for substringhood.

```py
>>> name = 'Elvis Presley'
>>> 'is' in name
True
>>> 'Frank' in name
False
```

(There's also `not in`, which checks if something's not a substring.)

### String formatting

The `.format` method on strings fills a dual purpose. It allows us to quickly an easily **build strings** out of small parts, and it allows to specify exactly how these are meant to be formatted and justified.

```py
>>> '{} {}'.format('The', 'Tempest')
'The Tempest'
>>> 'Total: {:d}'.format(400)
'Total: 400'
>>> 'Total: {:7d}'.format(400)
'Total:     400'
>>> 'Total: {:07d}'.format(400)
'Total: 0000400'
>>> 'Speed: [{:7.2f} km/h]'.format(19.3)
'Speed: [  19.30 km/h]'
```

We also have f-strings

```py
>>> h='Hello'
>>> w='World'
>>> f'{h*3} {w}'
'HelloHelloHello World'
```

## Exercise 3

## Flow of control: if and while

### Example: check odd or even

Let's say we want to find out whether an integer is odd or even. We can use an `if` statement for that.

```py
integer = int(input('Enter an integer: '))

if integer % 2:
    print(integer + ' is odd')
else:
    print(integer + ' is even')
```

Notice that we're relying on implicit conversion of `int` to `bool` here. This leads us to a common pattern...

We could be very specific when checking if something is an empty value:

```py
if string == '':
    ...
if collection == []:
    ...
if variable == None:
    ...

```

But usually we'll just rely on the automatic conversion to `bool`:

```py
if not variable:
    ...
```

### while loops

Where `if` statements conditionally run something once or not at all, `while` loops keep repeating their loop body as long as something is `True`.

```py
bottle_count = 10
while bottle_count:
    print('glug glug glug')
    bottle_count -= 1
```

A loop doesn't have to run at all. If `bottle_count` above had been initialized as `0`, there would have been zero iterations.

A loop can run forever. For example, `while True: pass` will run until the end of time, or until the warranty of the computer runs out.

An example: adding minutes to a time
Let's start with a simple but practical example.

We've been tasked with creating a program that takes as input a time-of-day of the form hh:mm, along with a number d of minutes, and emits a new timestamp hh:mm that's d minutes later.

### Model of computation: input/computation/output

The days of batch programming are not behind us. Much of the time, a programming task can be divided into three distinct stages:

```
    input --> [computation] --> output
```

-   The **input** stage often involves parsing, interpreting, normalizing and collating the values before the computation. * The **output** stage needs to deal with formatting, presentation, and writing to screen or disk or the network.
    As a consequence of this subdivision, it is often a really good idea to *not\* do I/O inside the "core" functions where computation happens. That way, the computation functions stay "pure", which helps re-use, testing, and maintenance.

Let's start with a simple but practical example.

We've been tasked with creating a program that takes as input a time-of-day of the form `hh:mm`, along with a number `d` of minutes, and emits a new timestamp `hh:mm` that's `d` minutes later.

Let's try fitting this into our three-part model of computation:

In the **input** stage, we parse the string `'hh:mm'` and extract the hour and minute from it.
In the **computation** stage, we handle the actual addition of `d` to produce a new timestamp.
In the **output** stage, we print the new timestamp in the format `'hh:mm'`.

### The main script

We want to be able to use the program like such:

```sh
$ python add-minutes.py 12:34 10
12:44
```

So this program seems like a good start. (Still need to write `add_time`)

```py
import sys
arguments = sys.argv[1:]

old_time, delta = arguments
hour = int(old_time[0:2])
minute = int(old_time[3:5])
delta = int(delta)
new_time = add_time(hour, minute, delta)
print('{:02d}:{:02d}'.format(new_time[0], new_time[1]))
```

Let participants try solve this problem.

add_time solution:

```py
def add_time(hour, minute, delta):
    while delta:
        if minute == 59:
            hour += 1
            minute = 0
        else:
            minute += 1
        if hour == 24:
            hour = 0
        delta -= 1

    return hour, minute
```

## Exercise 4

## Lists and for-loops

Lists (sometimes called "arrays" in other languages) are sequences of values. They're mutable, so we can change lists during their lifetime.

```py
>>> numbers = [3, 1, 2]
>>> numbers.sort()
>>> numbers
[1, 2, 3]
```

List indexes are zero-based.

```py
>>> numbers[0]
1
>>> numbers[2]
3
```

### Adding things to a list

Assigning directly to an element helps overwrite an element that's already there.

```py
>>> shopping_list = ['onions', 'eggs', 'ham', 'cheese']
>>> shopping_list[0] = 'milk'
>>> shopping_list
['milk', 'eggs', 'ham', 'cheese']
```

Sometimes we want to add to the end of the list, though.

```py
>>> shopping_list.append('bread')
>>> shopping_list
['milk', 'eggs', 'ham', 'cheese', 'bread']
```

Or sometimes insert before some element.

```py
>>> shopping_list.insert(3, 'butter')
>>> shopping_list
['milk', 'eggs', 'ham', 'butter', 'cheese', 'bread']
```

### Removing things from a list

Use `.pop` to remove an element by index.

```py
>>> shopping_list.pop(2)
>>> shopping_list
['milk', 'eggs', 'butter', 'cheese', 'bread']
```

Or `.remove` to remove by a value in the list.

```py
>>> shopping_list.remove('cheese')
>>> shopping_list
['milk', 'eggs', 'butter', 'bread']
```

### Get the length a list

The builtin `len` function returns the number of elements in a list.

```py
>>> len(shopping_list)
4
```

`len` also works on strings.

### Slicing a list

Just as with strings, we can name ranges of indexes in what's called slicing.

```py
>>> rainbow = ['red', 'orange', 'yellow', 'green',
...            'blue', 'indigo', 'violet']
>>> rainbow[:2]
['red', 'orange']
>>> rainbow[2:4]
['yellow', 'green']
>>> rainbow[4:]
['blue', 'indigo', 'violet']
```

The principle is fairly straightforward: you do `list[start:stop]`. The `start` index is always included and the `stop` index is always excluded. If you omit either endpoint, it goes as far as it can.

Negative indexes work from the end.
Python understands `negative` list (and string) indexes. They simply count from the end of the list, starting at `-1`.

```py
>>> rainbow = ['red', 'orange', 'yellow', 'green',
...            'blue', 'indigo', 'violet']
>>> rainbow[:-5]
['red', 'orange']
>>> rainbow[-5:-3]
['yellow', 'green']
>>> rainbow[-3:]
['blue', 'indigo', 'violet']
```

### For loops

Because lists are such perfect containers for holding sequences of similar values, what we most often want to do with lists is to loop through them, searching for something, or changing something, or doing something.

`for` loops do that.

```py
month_lengths = [
    31, 28, 31, 30, 31, 30,
    31, 31, 30, 31, 30, 31,
]

for day_count in month_lengths:
    print(day_count)
```

#### Example: summing a list of values (manually)

Now that we know how to loop over a list of values, we could go on and solve other problems. For example, we could sum a list of integers:

```py
prices = [100, 50, 200, 25]

total = 0
for p in prices:
    total += p
print(total)
```

Well, we can do it like that, and it's only three lines...

#### Example: summing a list of values (builtin)

...but Python graciously provides the sum function, so we don't have to loop.

```py
prices = [100, 50, 200, 25]

total = sum(prices)
print(total)
```

How do we know when Python provides something for us out-of-the-box, so we don't have to go ahead and implement it ourselves?

Here there are no real shortcuts. You just have to learn about the built-in capabilities of Python. Being curious and exploring goes a long way.

#### Ranges

A range in Python is a list of numbers.

```py
>>> print(list( range(5) ))
[0, 1, 2, 3, 4]
```

It might please you to know that ranges work like slices, with a `start`, `stop` and `step` parameter. `start` and `step` are optional.

```py
>>> print(list( range(3, 5) ))
[3, 4]
>>> print(list( range(10, 0, -1) ))
[10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
```

#### Looping over indexes and values

Sometimes we're interested in looping over the indexes of the list, instead of its elements:

```py
names = ['Elvis', 'Frank', 'Tom']

for i in range( len(names) ):
    # ...something with i...
    print(i, names[i])
```

And sometimes we want to loop over both the indexes and the values:

```py
for i, name in enumerate(names):
    # ...something with i and the value...
    print(i, name)
```

#### Example: checking for elements

Want to check whether something is in a list? The in operator strikes again!

```py
>>> names = ['Elvis', 'Frank', 'Tom']
>>> 'Frank' in names
True
>>> 'Harry' in names
False
```

(There's no explicit loop, but the operator will need to _scan through the list_)

## Exercise 5

### List comprehensions

It turns out that we end up building new lists from old ones quite a lot, using `for` loops and `.append`:

```py
values = [2, 3, 5, 7, 11, 13, 17, 19]
squares = []                # (1) initialize
for v in values:            # (2) loop
    squares.append(v * v)   # (3) compute/.append
```

**List comprehensions** aim to capture this pattern, pulling out the relevant parts and making it a bit easier to write.

```py
squares = [v * v for v in values]
```

Filtering with Comprehensions
We should consider using a list comprehension any time our brain goes "ok, so now I just need to build this list..." This is especially true if you are starting with a different list.

You can keep or discard items with a condition.

```py
>>> primes = [p for p in range(2, 20) if is_prime(p)]
>>> primes
[2, 3, 5, 7, 11, 13, 17, 19]
```

Filtering with functions
The things we just did with list comprehensions can also be done with two built-in functions called `map` and `filter`:

```py
squares = list(map(lambda v: v * v, values))

primes = list(filter(is_prime, range(2, 20)))
```

The list comprehensions actually look a bit nicer, and are preferable to use, but it's nice to know `map` and `filter` exist. They are a bit closer to the functional programming tradition and to function composition.

(Python 3 gives back iterators, not lists, so we need the surrounding `list()` calls.)

### Split string

Often we find ourselves wanting to split a string on some separator; that is, make a list of all the things in-between and throw away the separators.

```py
ingredients = 'cheese,milk,flour,tomatoes,celery'

print(ingredients.split(','))
# ['cheese', 'milk', 'flour', 'tomatoes', 'celery']
```

```py
title = 'The Curious Case of the Dog in the Night-Time'

print(title.split(' '))  # ['The', 'Curious', 'Case', ...]
print(title.split())     # ['The', 'Curious', 'Case', ...]
```

The difference between `.split(' ')` and `.split()` is that the first splits on individual spaces, whereas the second splits on any whitespace (newlines, tabs, line feeds), and also removes any empty strings in the result.

```py
>>> 'a   b  c'.split(' ')
['a', '', '', 'b', '', 'c']
>>> 'a   b  c'.split()
['a', 'b', 'c']
```

### Join list of strings into a big string

The opposite of splitting is to join a list of strings into one big string. Often enough, we also want to (re-)introduce some separator as we do so. This is exactly what the `str.join` method does:

```py
countdown = [str(d) for d in reversed(range(1, 10))]
countdown.append('blastoff!')

print('...'.join(countdown))
# 9...8...7...6...5...4...3...2...1...blastoff!
```

When you don't want a separator, just `''.join` the list.

### Breaking out of a loop

There is two ways to end a loop, and a way to skip an iteration.

To skip an iteration we use the `continue` keyword.

```py
names = ['John', 'Jane', 'Tim', 'Tom']

for name in names:
    if name == 'Tim':
        continue
    print(name)

John
Jane
Tom
```

To end a loop we use `break` or `return`.

```py
names = ['John', 'Jane', 'Tim', 'Tom']

for name in names:
    if name == 'Tim':
        break
    print(name)

John
Jane
```

`return` only works in functions, and basically returns the function call which in turn breaks the loop.

Sometimes it's better to use a variable for readability:

```py
still_looking = True
while still_looking:
    ...
    if found_it:
        still_looking = False
```

### Get the index of an item in a list

Searching a list is pretty common. This is such a common operation that it's built-in function:

```py
[4, 8, 7, 2, 9, 7].index(7)                  # 2
['John', 'Jane', 'Tim', 'Tom'].index('Tom')  # 3
```

## Exercise 6

### Example: number guessing game

Let's construct a simple number guessing game, where:

-   The program picks a random three-digit number
-   Until the user guesses right:
    -   The user gets to guess what the number is
    -   The program gives hints as to whether the guess should be higher or lower
-   Something nice is printed, such as 'Yes, you got it!'

```py
import random

print("I'm thinking of a number between 100 and 999.")
goal = random.randint(100, 999)

guessed_it_yet = False
while not guessed_it_yet:
    # ...accept a guess...
    # ...correct, or tell user to go higher/lower...

print('Yes, you got it! It was {}.'.format(goal))
```

That seems to be it. But we've left a few details out of the loop, so let's focus on those.

The loop body has three tasks: to accept the guess, to give hints, and to conclude the loop when the correct number was guessed.

```py
guessed_it_yet = False
while not guessed_it_yet:
    print()
    guess = int(input('Make a guess: '))

    if guess > goal:
        print('Your guess was too high. Go lower.')
    elif guess < goal:
        print('Your guess was too low. Go higher.')
    else:
        guessed_it_yet = True
```

This is a typical case where we can leave out the guessed_it_yet boolean flag and replace it with a break inside the loop.

```py
while True:
    print()
    guess = int(input('Make a guess: '))

    if guess > goal:
        print('Your guess was too high. Go lower.')
    elif guess < goal:
        print('Your guess was too low. Go higher.')
    else:
        break
```

I hesitate to make that change, however. We do save one variable, but on the other hand, it doesn't improve readability much.

It should set off some alarm bells in our heads to see the same three-digit numbers repeated twice like this.

```py
print('I'm thinking of a number between 100 and 999.')
goal = random.randint(100, 999)
```

We should lift them out into constants.

```py
LOWER_LMT = 100
UPPER_LMT = 999

print('... between {} and {}.'.format(LOWER_LMT, UPPER_LMT))
goal = random.randint(LOWER_LMT, UPPER_LMT)
```

It usually pays off to have nice names, and to have the number literals in only one place.

Another small-but nice improvement: we could track the number of guesses that were needed to get the number right. In the set-up code:

```py
# in the set-up code
attempts = 0

while not guessed_it_yet:
    guess = int(input('Make a guess: '))
    attempts += 1
    # ...

# in the wind-down code
print('It took you {} guesses.'.format(attempts))
```

### Sort a list

Here's how you sort a list of values.

```py
items = ['sorted', 'all', 'now', 'items']

# Non-destructive sorting
print(sorted(items)) # ['all', 'items', 'now', 'sorted']
print(items)         # ['sorted', 'all', 'now', 'items']

# Destructive
items.sort()        # sorts in place
print(items)        # ['all', 'items', 'now', 'sorted']
```

### Reverse a list

And this is how you can reverse a list.

```py
items = ['fee', 'foo', 'fum']

# Non-destructive
list(reversed(items))       # ['fum', 'foo', 'fee']
items                       # ['fee', 'foo', 'fum']

# Destructive
items.reverse()             # reverses in place
items                       # ['fum', 'foo', 'fee']
```

## Exercise 7

## Input och output

There are four main entities a program will need to communicate with.

-   **The user**, through the keyboard and the screen.
-   **The file system**, by opening files for reading and writing. The Unix tradition gives you STDIN and STDOUT which can be redirected to files or other processes.
-   **A data store**. We'll look at that tomorrow.
-   **The network**. Outside the scope of this course.

### Example: finding palindromes in a word list

Let's take a word list and find all the palindromes in it. To recap, a palindrome is a string that remains the same when reversed.

```py
>>> 'deified'[::-1]
'deified'
```

There are a lot of one-letter words in the word list. They're technically palindromes, but let's ignore them because they're not that interesting.

The code for this is relatively straightforward. The really new thing here is the with statement, to manage resources.

```py
with open('files/words') as f:
    for line in f:
        if len(line) == 1:
            continue
        if line[::-1] == line:
            print(line)
```

Sadly, when we run this program, it turns up... nothing. Why is that?

We need to use `.rstrip` because lines includes their final line break.

```py
with open('files/words') as f:
    for line in f:
        line = line.rstrip()
        if len(line) == 1:
            continue
        if line[::-1] == line:
            print(line)
```

Actually `.rstrip` removes all whitespace at the end of the string, but it serves our purposes here, removing the line breaks.

### Writing files

A file can be opened either for reading or writing. It opens for reading by default, but we can pass a second argument, 'w' to our open call to open it for writing instead.

We can then use the write method to write to the file.

```py
with open('output.txt', 'w') as f:
    for n in range(10):
            f.write('Line #{:d}\n'.format(n))
```

The with statement we used in our file I/O examples is a way of managing resources in Python. We could replace the following code:

```py
with open('file') as f:
    do_work()
```

With this:

```py
f = open('file')
do_work()
f.close()
```

What if an error pops out within do_work though? with statement guarantees that the file will still get closed no matter what.

## Exercise 8

### Using file as a small database

By utilizing the `json` module you can save entire dictionaries, of even lists containing these in a text-file.

```py
# file modes:
# x - create file
# r - read file
# w - overwrite text in file
# a - append text in file

# create file if it doesn't exist
try:
  open('users.txt', 'x')
except:
  # error if file already exists
  pass

# append text to file (creates file if it doesn't exist)
# with open('users.txt', 'a') as file:
#   file.write('\nSven')

# import the json module
import json

# list containing dictionaries
users = [
  {
    'name': 'Johan',
    'age': 32
  },
  {
    'name': 'Elsa',
    'age': 26
  }
]

# 'with' is a context handler that
# automatically closes the file when done
with open('users.txt', 'w') as file:
  # convert object to json string
  users_json = json.dumps(users)
  # save users as a json-string in the file
  file.write(users_json)


# read content of file
with open('users.txt', 'r') as read_file:
  # read the file into a string variable
  read_users_json = read_file.read()
  # parse json back to a list of dictionaries
  read_users = json.loads(read_users_json)


print(read_users)
```

## Formatting

Without formatting, doing any kind of output is kinda painful -- with formatting, difficult things turn easy.

Often we have common formats, or have a need for common padding tasks. Formatting helps with both of these tasks.

There are two main string formatting syntaxes, either with '.format':

```py
name = 'World'
'Hello {}!'.format(name)
```

or with f-strings (since Python 3.6)

```py
name = 'World'
f'Hello {name}'
```

There are extra formatting options that can be used inside the brackets.

```py
{:s}    string

{:d}    Base-10 integer
{:b}    Base-2  integer
{:x}    Base-16 integer

{:f}    Floating-point number
```

```py
>>> '{:<30}'.format('left aligned')
'left aligned                  '
>>> '{:>30}'.format('right aligned')
'                 right aligned'
>>> '{:^30}'.format('centered')
'           centered           '
>>> '{:*^30}'.format('centered')
'***********centered***********'
```

similar syntax with f-strings:

```py
>>> var='left aligned'
>>> f'{var:>30}'
'                  left aligned'
```

### Other useful formatting tricks

Using the comma as a thousands separator:

```py
>>> '{:,}'.format(1234567890)
'1,234,567,890'
```

Expressing a percentage:

```py
>>> points = 19.5
>>> total = 22
>>> 'Correct answers: {:.2%}'.format(points/total)
'Correct answers: 88.64%'
```

We can also change order of our parameters (useful when supporting multiple languages where the order of words may change)

```py
>>> '{} is {}'.format('Luke', 'clever')
'Luke is clever'

>>> '{1} {0} is'.format('Luke', 'clever')
'clever Luke is'
```

And we can name elements instead of using positional arguments

```py
>>> '{last_name}, {first_name} {last_name}' \
    .format(first_name='James', last_name='Bond')
'Bond, James Bond'
```

which combines nicely with dictionary unwrapping:

```py
>>> agent={'first_name': 'James', 'last_name': 'Bond'}
>>> '{last_name}, {first_name} {last_name}'.format(**agent)
'Bond, James Bond'
```

## Exercise 11

## Functions

A function is a block of code which only runs when it is called.

You can pass data, known as parameters, into a function.

A function can return data as a result.

### Creating a Function

In Python a function is defined using the def keyword.

To call a function, use the function name followed by parenthesis.

```py
def my_function():
  print("Hello from a function")

my_function()
```

### Arguments

Information can be passed into functions as arguments.

Arguments are specified after the function name, inside the parentheses. You can add as many arguments as you want, just separate them with a comma.

```py
def my_function(name):
  print(name + " Andersson")

my_function("Emil")
my_function("Tobias")
my_function("Linus")
```

### Number of Arguments

By default, a function must be called with the correct number of arguments. Meaning that if your function expects 2 arguments, you have to call the function with 2 arguments, not more, and not less.

```py
def my_function(first_name, last_name):
  print(first_name + " " + last_name)

my_function("Emil", "Ericsson")
```

### Arbitrary Arguments, \*args

If you do not know how many arguments that will be passed into your function, add a \* before the parameter name in the function definition.

This way the function will receive a tuple of arguments, and can access the items accordingly.

```py
def my_function(*kids):
  print("The youngest child is " + kids[2])

my_function("Emil", "Tobias", "Linus")
```

### Keyword Arguments

You can also send arguments with the key = value syntax.

This way the order of the arguments does not matter.

```py
def my_function(child3, child2, child1):
  print("The youngest child is " + child3)

my_function(child1 = "Emil", child2 = "Tobias", child3 = "Linus")
```

### Arbitrary Keyword Arguments, \*\*kwargs

If you do not know how many keyword arguments that will be passed into your function, add two asterisk: \*\* before the parameter name in the function definition.

This way the function will receive a dictionary of arguments, and can access the items accordingly.

```py
def my_function(**kid):
  print("His last name is " + kid["last_name"])

my_function(first_name = "Tobias", last_name = "Andersson")
```

### Default Parameter Value

The following example shows how to use a default parameter value.

If we call the function without argument, it uses the default value.

```py
def my_function(country = "Norway"):
  print("I am from " + country)

my_function("Sweden")
my_function("India")
my_function()
my_function("Brazil")
```

### Return Values

To let a function return a value, use the return statement.

```py
def add_two_numbers(a, b):
  return a + b

print(add_two_numbers(3, 2))
print(add_two_numbers(5, 12))
print(add_two_numbers(9, 32))
```

### The pass Statement

Function definitions cannot be empty, but if you for some reason have a function definition with no content, put in the pass statement to avoid getting an error.

```py
def my_function():
  pass
```

## Exercise 9

## Dictionaries

Creating a dictionary is as simple as creating a list, really.

```py
person = {}
```

Of course, we may want to initialize a dictionary with elements. We do it like this:

```py
person = { 'first_name': 'John', 'last_name': 'Doe', 'age': 33 }
```

Accessing entries in a dictionary
The syntax to access a dictionary is exactly the same as with lists.

```py
person['first_name']
```

It's just that dictionary keys tend to be strings rather than integers. (And they don't have to be strings, they can be a lot of other types.)

There's no slice syntax for dictionaries.

Dictionaries do fast lookups, just as lists with their indexes.

Adding something anywhere in a dictionary is also fast.

```py
person['age'] = 34
person['country'] = 'England'
```

Occasionally you'll need to loop over all the entries in a dictionary. If that's all you do with it, though, consider whether it's actually a dictionary you want, and not some kind of list.

> "Doing linear scans over an associative array is like trying to club someone to death with a loaded Uzi." — Larry Wall

### Looping over the keys of a dictionary

Just looping over a hash gives us the keys, in (arbitrary) storage order.

```py
for name in phone_numbers:
    print(name)

# Rose
# Philip
# Andrew

# Same as this:

for name in phone_numbers.keys():
    print(name)
```

### Sorting the keys and looping over them

If we actually want the dict keys in sorted order, we have to say so.

```py
for name in sorted(phone_numbers):
    print(name)

# Andrew
# Philip
# Rose
```

## Looping over the values of a dictionary

Similarly, if we loop over the values, we get the values in storage order.

```py
for number in phone_numbers.values():
    print(number)

# 555-274102
# 555-204238
# 555-296432
```

### Sorting the values and looping over them

And we sort the dict values if we care about the order they come out.

```py
for number in sorted(phone_numbers.values()):
    print(number)

# 555-204238
# 555-274102
# 555-296432
```

## Exercise 10

## List comprehensions

List comprehensions provide a way to transform one list into another in a declarative way.

This is in many ways similar to what you can do with SQL with relations in a database server, or languages like LINQ in .Net.

### List comprehensions: mapping

Suppose we have a function like this:

```py
def pow(x, n): # x**n
    return x**n
```

If I want to generate a list of the perfect cubes from 1 to 64, I could:

```py
cubes = [ pow(x, 3) for x in range(1, 5) ]; # 5 is excluded
```

### List comprehensions: filtering

You can also do filtering in the same way:

```py
odd = [ x for x in range(1, 100) if x % 2 ]
You can combine in the same way:

oddsquare = [ x**2 for x in range(1, 10) if x % 2]
```

### List comprehensions: joining

We could take a list of some keys and output a set of tuples of the key and a value from a dictionary:

```py
nummap = {'a': 123, 'b': 234, 'c': 345, 'd': 456}
chars = ['a', 'd']
subset = [(x, nummap[x]) for x in chars]
```

### Set comprehensions

If we simply replace the square brackets with curly ones we get a set out. This means that unlike with a list comprehension, order is no longer preserved, and duplicates are omitted.

For example, suppose I have the following list:

```py
my_list = [1, 2, 2, 3, 3, 4, 4, 5]
```

Then the following are almost equivalent:

```py
set(my_list)
{ x for x in my_list }
```

### Dictionary comprehensions

You can also create dictionaries using a similar syntax:

```py
{ x : x**2 for x in range(1, 5) }
```

This is quite useful in joining as well

### Comprehension Gotchas: Clause Order

Comprehensions have a few areas of behavior that can bite you.

First is that ordering of loop and and conditional expressions follow an outer -> inner ordering. So if you want to flatten an array you would do something like

```py
[ item for subarray in array for item in subarray ]
```

This syntax takes some getting used to, but it can also make debugging harder.

## Classes and objects

### Recap: data structures are pretty great

In Python, you are already in an enviable position with your different data containers, tailored for your needs:

```py
l = [1, 2, 3] # array
t = (1, 2, 3) # tuple
d = { 'two': 'deux' } # dict
s = { 'a', 'b', 'c' } # set
```

But...

But sometimes, we need just a little bit more. We need to create our own vocabulary, a mini-language inside the language.

```py
employee = {
'name': 'Dave',
'role': 'Developer',
}

print(employee['name']) # Dave
print(employee['role']) # Developer
```

This is sufficient, but there's a better way.

We can do better than theat. There's a way to write it shorter with the same result.

```py
employee = Employee('Dave', 'Developer')
print(employee.name) # Dave
print(employee.role) # Developer
```

Two things are nicer:

-   We're constructing an `Employee` object, instead of filling out keys and values in a dict.
-   We're using attribute access (`employee.name`) instead of dictionary indexing (`employee['name']`).

Here's the class declaration that makes the object in the previous slide work:

```py
class Employee:
    def __init__(self, name, role):
        self.name = name
        self.role = role

# Now this works:
employee = Employee('Dave', 'Developer')
print(employee.name)        # Dave
```

We'll get into details soon, but a few comments:

-   A class declaration has a name (Employee in this case).
-   It can also declare methods; these are functions, so they're defined with the def keyword.
-   `__init__` clearly has something to do with object initialization.

In `__init__` and in all normal methods, self tends (by convention) to be the name of the first parameter:

```py
class Employee:
    def __init__(self, name, role):
        self.name = name
        self.role = role

    def report(self):
        return '{} the {}'.format(self.name, self.role)
```

`self`, of course, represents the object the method was called on.

In method calls, the `self` parameter is not given:

```py
employee.report()   # Dave the Developer
```

### Inheritance

To make a class inherit from some base type, enclose the base type in parentheses as part of the class declaration.

```py
class Employee:
    # ...

class Accountant(Employee):
    pass

accountant = Accountant('Agnes', 'Accountant')
accountant.report()   # Agnes the Accountant
```

You can customize the `__init__` method in a subclass, but then you have to pass the arguments related to the parent class to its `__init__`.

A class can access its parent with the `super` keyword.

```py
class Accountant(Employee):
    def __init__(self, name, role, salary):
        super().__init__(name, role)
        self.salary = salary

accountant = Accountant('Agnes', 'Accountant', 50000)
accountant.report()   # Agnes the Accountant
accountant.salary   # 50000
```

### Three types of method

You can annotate methods so that they behave differently when they are called.

```py
class E:
    def m1(self, a, b, c):
        # `e.m1(a, b, c)`
        # has access to the instance, `self`

    @classmethod
    def m2(klass, a, b, c):
        # `E.m2(a, b, c)` (or `e.m2(a, b, c)`)
        # has access to the class, but not the instance
        # examples: factory methods like int.frombytes and dict.fromkeys

    @staticmethod
    def m3(a, b, c):
        # `E.m3(a, b, c)` (or `e.m3(a, b, c)`)
        # has access to neither instance or class
        # examples: everything in `math`
```

## Exercise 12

## Exceptions

Python exceptions are intended to be heavily used, typically in 4 cases:

1. A serious problem has been detected and execution cannot safely continue
1. A precondition check has failed (another programmer called a function wrong or otherwise the function call is invalid)
1. A user submitted a request that cannot be completed
1. Flow otherwise needs to be interrupted (avoid these)

### Raise an exception

```py
def crash():
    raise Exception("Crash time")

crash()

Traceback (most recent call last):
  [...]
  in crash
    raise Exception("Crash time")
Exception: Crash time
```

### Catch an exception

```py
try:
    crash()
except Exception as e:
    print("error:", e)

error: Crash time
```

## Regular expressions

Regular expressions provide a simple way to match patterns in text. They do not handle more complex structures well than simple patterns (do not try to parse HTML with a regex!).

In Python we use raw strings to avoid duplicating backslashes.

```py
r'\d{2}-\d{2}-\d{4}'
instead of

'\\d{2}-\\d{2}-\\d{4}'
```

### Example: finding a particular word in a text

Here the regex variable becomes an "engine" that can match the substring "interesting" in any string.

```py
import re
regex = re.compile('interesting')
regex.search('what an interesting question!')   # a match object
```

You don't have to compile regexps before using them, but it's a good habit to adopt. Compiling the regex takes a little bit of time, and it makes sense not to have to re-do that work in every iteration in a loop, say.

### Example: finding, case-insensitive

When we compile a regular expression we can set the ignore case flag:

```py
import re
regex = re.compile('interesting', re.IGNORECASE)
regex.search('what an inteREsting question!')
```

## Exercise 13

## Modules and packages

Consider this file `angrybirds.py`:

```py
def shoot():
    print('wheee!')
```

Now, from any other program, or from the REPL, we can import this file as a module, and use its one function:

```py
import angrybirds
angrybirds.shoot()      # wheee!
dir(angrybirds)         # [... , 'shoot']
```

When you import the module, Python will also compile it into `angrybirds.pyc`, saving itself the trouble of compiling it the next time.

Note that with the above form `shoot` ends up in its own module namespace `angrybirds`.

If we just want to import `shoot` into the `__main__` namespace, we do this:

```py
from angrybirds import shoot
shoot()                 # wheee!
dir(angrybirds)         # ERROR: name 'angrybirds' is not defined
```

Python uses a list in the variable `sys.path` when it goes looking for modules. `sys.path` is a combination of these three locations:

-   the directory containing the input script (or the current directory).
-   `PYTHONPATH` (a list of directory names, with the same syntax as the shell variable PATH).
-   the installation-dependent default.

After initialization, Python programs can modify `sys.path`.

## Debugging

Python has a module pdb that you can import into your program to insert debugging capability wherever you need.

```py
import pdb

...

pdb.set_trace()     # program will pause here
```

### Live demo

## Exercise 14

## Databases

### A brief discussion of databases

In many programs we need to persist things across many runs of a program, or even handle resources across concurrent runs. For small programs writing files and storing them on the file system may be sufficient but for larger programs we need somewhere to store data in a more ordered format.

### SQLite

SQLite comes supported by Python out of the box and is an embedded C library which gives you an ACID-compliant small SQL database without the overhead of a separate server.

The sqlite3 module provides support for sqlite. There are no other dependencies.

SQLite also can be tightly integrated with your application. You can even register python function to extend SQL (but this limits portability).

### Native Drivers

Many databases also have native drivers for Python.

For example, PostgreSQL has the Psychopg, which supports two phase commit, asynchronous notifications, and much more.

When doing advanced work with databases, it is often necessary to go with native drivers.

Popular drivers:

-   PostgreSQL: Psychopg
-   MySQL: mysql-connector-python
-   MongoDB: pymongo

### SQLite helper

```py
import sqlite3

# set the name of the database here
database_name = 'data.db'

def query(query, values = {}):
  '''
  Generic function that either gets or updates the database, based on what the query starts with.

  :param: query: The SQL-query to execute.
  :param: values: The values to be used with the query. (default = {})
  :return: The results from a SELECT as a list of Rows, or the autoincremented 'id' from an INSERT
  '''
  if query.upper().strip().startswith('SELECT'):
    return get(query, values)
  else:
    return run(query, values)


# helper function to update database
def run(query, values = {}):
  '''
    Helper function to update database.

    :param: query: The SQL-query to execute.
    :param: values: The values to be used with the query. (default = {})
    :return: The autoincremented 'id' from an INSERT
  '''
  # connect to database (creates if not exists)
  conn = sqlite3.connect(database_name)
  # open a cursor to the database
  cur = conn.cursor()
  # By default the FOREIGN KEY CASCADE is a no-op
  # so we have to manually enable it when using DELETE
  if query.upper().strip().startswith('DELETE'):
    cur.execute('PRAGMA foreign_keys = ON')
  # run query with values and execute
  result = cur.execute(query, values)
  # must commit queries that does changes to the database
  conn.commit()
  # close connection
  conn.close()
  # return autoincremented id
  return result.lastrowid


def get(query, values = {}):
  '''
    Helper function to get data from database.

    :param: query: The SQL-query to execute.
    :param: values: The values to be used with the query. (default = {})
    :return: The results from the query as a list of Rows
  '''
  # connect to database (creates if not exists)
  conn = sqlite3.connect(database_name)
  # convert results to dict-like objects
  conn.row_factory = sqlite3.Row
  # open a cursor to the database
  cur = conn.cursor()
  # run query with values and execute as a prepared statement
  cur.execute(query, values)
  # get results from executed query
  results = cur.fetchall()
  # close connection
  conn.close()
  # return results as a list of Rows
  return results
```

### SQLite helper examples

```py
# import helper function from our database module
from database import query

# create table users if it doesn't exist
query('''
  CREATE TABLE IF NOT EXISTS users (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name STRING NOT NULL,
    age INTEGER NOT NULL
  )
''')


# create a user
query('''
  INSERT INTO users VALUES(NULL, 'Elsa', 24)
''')

# example using input from terminal to get users from database
search_name = input('Search by name: ')

# use the input string with the query to filter with LIKE
# note: the way this works will replaced
users_by_name = query('''
  SELECT * FROM users WHERE name LIKE :search
''',
  { 'search': f'%{search_name}%' }
)

for user in users_by_name:
  print(user['name'])


# create user from a dict
user = {
  'name': 'Loke',
  'age': 7
}

# insert with the dict and get the autoincremented 'id'
insert_result = query('INSERT INTO users VALUES(NULL, :name, :age)', user)

print(insert_result)

users = query('''
  SELECT * FROM users
''')

for user in users:
  print(user['name'])
```

## GUI-development

With large-enough or complicated-enough programs, a fixed path is not enough. We throw up our hands and say "the user is in control, not the program". User actions, such as button clicks and menu choices, direct what happens next.

We call this **inversion of control**.

-   tkinter - built into Python (on Windows and Mac if using installer from python.org)
    -   install tkinter manually: `sudo apt-get install -y python3-tk`
-   customtkinter:
    -   github: https://github.com/TomSchimansky/CustomTkinter
    -   docs: https://github.com/TomSchimansky/CustomTkinter/wiki
    -   install: `pip3 install customtkinter`
-   PyQt
-   Kivy
-   PyGame
 