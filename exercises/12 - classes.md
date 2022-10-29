## Exercise 12: objects and classes

* In a new file, define a class `Schedule` with just a `pass` statement as its
  body.
* After the class declaration, make an instance of the class with `s = Schedule()`
* Run the program to make sure it works.
* Replace the `pass` statement with a `def book(self, name):` and have the method
  `print('Booked {}'.format(name))`
* After the line that initialized `s`, call `s.book('appointment 1')`
* In the class declaration, but above the method, add a declaration `bookings = []`
* Now make the `book` method actually `.append` `name` to `self.bookings`
* If you have time, add a way for the method to refuse a booking if there are
  already 3 bookings in `bookings`. Make the method print its refusal.
* Try it out by trying to make four bookings instead of just one.
* What's the problem with initializing `bookings` the way we do? How should we
  really initialize it?
