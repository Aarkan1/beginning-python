## Exercise 12: objects and classes

> * In a new file, define a class `Schedule` with just a `pass` statement as its
>   body.

```python
class Schedule:
    pass
```

> * After the class declaration, make an instance of the class with `s = Schedule()`

```python
s = Schedule()
```

> * Replace the `pass` statement with a `def book(self, name):` and have the method
>   `print('Booked {}'.format(name))`

```python
class Schedule:
    def book(self, name):
        print('Booked {}'.format(name))
```

> * After the line that initialized `s`, call `s.book('appointment 1')`

```python
s = Schedule()
s.book('appointment 1')
```

> * In the class declaration, but above the method, add a declaration `bookings = []`

```python
class Schedule:
    bookings = []

    def book(self, name):
        print('Booked {}'.format(name))
```

> * Now make the `book` method actually `.append` `name` to `self.bookings`

```python
class Schedule:
    bookings = []

    def book(self, name):
        self.bookings.append(name)
```

> * If you have time, add a way for the method to refuse a booking if there are
>   already 3 bookings in `bookings`. Make the method print its refusal.

```python
class Schedule:
    bookings = []

    def book(self, name):
        if len(self.bookings) >= 3:
            print('nope')
        else:
            self.bookings.append(name)
```

> * Try it out by trying to make four bookings instead of just one.

```python
s = Schedule()
s.book('appointment 1')
s.book('appointment 2')
s.book('appointment 3')
s.book('appointment 4') # nope
```

> * What's the problem with initializing `bookings` the way we do? How should we
>   really initialize it?

The problem comes when we have two `Schedule` objects, and it turns out they
share a single `bookings` list internally:

```python
s1 = Schedule()
s1.book('appointment 1')
s1.book('appointment 2')
s1.book('appointment 3')

s2 = Schedule()
s2.book('appointment 4') # nope (!)
```

The reason is that the line `bookings = []` in the `Schedule` class installs a
_single_ list on the _class_ level, not per `Schedule` instance. In order to
get one `bookings` list per instance, like we expect, we want to do the
initialization in the `__init__` method, which runs after an instance has been
created:

```python
class Schedule:
    def __init__(self):
        self.bookings = []

    # `book` method is the same
```
