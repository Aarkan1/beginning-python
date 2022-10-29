Contains solutions for exercises:
- 1 - 18
- 32 - 44
- 68 - 77

Modules and helpers used in the solutions.

```py
import math
import random

# create list with random numbers
numbers = random.sample(range(-100, 100), 50)
```

## Algoritmer
```py
#  1.
def solultion_1(num):
  print(num**2)

# solultion_1(3)

#  2.
def solution_2(sale):
  salary = 8000
  output = sale * 0.09
  print(salary + output)

# solution_2(20000)

#  3.
def solution_3(hours):
  minutes = hours * 60
  seconds = minutes * 60
  print(f'minutes: {minutes}, seconds: {seconds}')

# solution_3(3)

#  4.
def solution_4(num1, num2, num3):
  print((num1 + num2 + num3) / 3)

# solution_4(2, 4, 6)

#  5.
def solution_5(sek):
  dollar = sek / 6
  pund = sek / 10
  print(f'dollar: {dollar}, pund: {pund}')

# solution_5(15)

#  6.
def solution_6(a, x):
  print(a * x**3 + 7)

# solution_6(3, 2)

#  7.
def solution_7(litre, price, discount):
    before_discount = litre * price
    after_discount = before_discount - before_discount * (discount * 0.01)
    print(f'Before discount: {before_discount}, after: {after_discount}')

# solution_7(50.2, 12.5, 10)

#  8.
def solution_8(x, y):
  print('area:', x * y)
  print('circumference:', (x * 2) + (y * 2))

# solution_8(3, 4)

#  9.
def solution_9(radius):
  diameter = radius * 2
  circumference = diameter * math.pi
  area = radius**2 * math.pi

  print('diameter:', diameter)
  print('circumference:', circumference)
  print('area:', area)

# solution_9(12)

# 10.
def solution_10(f):
  print('Celcius:', 5 * (f - 32) / 9)

# solution_10(72)
```

## Villkor

```py
# 11.
def solution_11(num1, num2):
  if num1 > num2:
    print('num1 is greater than num2')

# solution_11(3, 2)

# 12.
def solution_12(num1, num2):
  if num1 > num2 * 2:
    print('Too big!')

# solution_12(12, 4)

# 13.
def solution_13(num):
  if num % 2 == 0:
    print('Even')

# solution_13(4)

# 14.
def solution_14(num):
  even = num % 2 == 0
  print('Is even:', even)

# solution_14(5)

# 15.
def solution_15(num1, num2):
  even = num1 % num2 == 0
  print('Is even:', even)

# solution_15(9, 3)

# 16.
def solution_16(items, price):
  discount = 0.1
  min_sum = 1000

  before_discount = items * price
  after_discount = before_discount - (before_discount * discount)

  if before_discount > min_sum:
    print('Price to pay after discount:', after_discount)
  else:
    print('Price to pay:', before_discount)

# solution_16(5, 300)

# 17.
def solution_17(num1, num2):
  if num2 == 0:
    print("Error, can't divide by 0")
  else:
    print(num1 / num2)

# solution_17(8, 0)

# 18.
def solution_18(x, y):
  a = 5

  if x > (5 + y):
    a = 2
  
  print(a)

# solution_18(15, 8)
```

## Loopar
```py
#32
for i in range(2, 102, 2):
    #start at 2, end at 102 (non inclusive), skip 2
    print(i)

#33
for i in range(100, -2, -2):
    #start at 100, end at -2 (non inclusive, skip 2 backwards)
    print(i)

#35
def number_squared():
    '''
    start at 1, end at 10 (non inclusive)
    multiply number by itself
    '''
    for i in range(1, 10):
        print(i**2)

#36
def interest():
    '''
    ask for interest rate
    for every year, accrue the interest (currect balance multiplied by interest (user input divided by 100)) to the total balance
    '''
    interest = input("Please enter interest rate: ")
    account_balance = 1000
    for i in range(10):
        account_balance += (account_balance(int(interest)/100))

#37
def number_printer():
    '''
    create an list to store the numbers
    ask user how many numbers they wish to input
    for the amount of numbers, ask for a number and add it to the list
    print the numbers list
    '''
    user_numbers = []
    amount_of_numbers = input('How many numbers do you want to input? ')
    for i in range(int(amount_of_numbers)):
        number = input('Enter number: ')
        user_numbers.append(int(number))
    print(user_numbers)
    
#39
def taxation():
    '''
    while user input does not equal zero, ask for a number
    add user input, plus itself times 0.25, to the taxed number
    if the user input does not equal zero, print the taxed number
    '''
    user_number = 1
    while int(user_number) != 0:
        user_number = input('Enter a number: ')
        taxed_number = int(user_number) + (int(user_number) * 0.25)
        if int(user_number) != 0:
            print(taxed_number)

#41
def add_one_through_fifty():
    total = 0
    for i in range(51):
        total += i
    print(total)

#42
def add_twenty_numbers():
    total = 0
    for i in range(20):
        number = input('Enter a number: ')
        total += int(number)
    print(total)

#43
total = 0
for i in range(2, 32, 2):
    total += i
print(total)

#44
user_input = input('Enter amount of numbers to add: ')
total = 0
for i in range(int(user_input)):
    user_number = input('Enter number to be added to total: ')
    total += int(user_number)
print(total)
```

## Listor
```py
#68
def double(lst):
    '''
    receive a list (numbers)
    go through every index (length of list [i])
    double the number at index [i]
    '''
    for i in range(len(lst)):
        lst[i] *= 2

#69
def add_two_every_other(lst):
    '''
    receive a list (numbers)
    go through every other index (start at 0, for the length of the list, skip 2 spots)
    add 2 to the number at index[i]
    '''
    for i in range(0, len(lst), 2):
        lst[i] += 2

#70
def find_positive(lst):
    '''
    receive a list (numbers)
    go through the list, if the number is bigger than 0, add 1 to the counter
    print counter
    '''
    counter = 0
    for number in numbers:
        if number > 0:
            counter += 1
    print("Amount of positive numbers: ", counter)

#71
def compare_to_first(lst):
    '''
    receive a list (numbers)
    go through the list, starting at index 1 and for the lenght of the list
    if the number is bigger than index 0, add 1 to counter
    print counter
    '''
    counter = 0
    for i in range(1, len(lst)):
        if lst[i] > lst[0]:
            counter += 1
    print(counter)
    
#73
def add_all_and_find_average(lst):
    '''
    receive a list (numbers)
    go through the list and add every number to total
    the average equals the total divided by the amount of numbers (length of the list)
    print total and average
    '''
    total = 0
    for number in lst:
        total += number
    average = total / len(lst)
    print(f'Total is: {total} and average is {average}')

#74
def find_min_and_max(lst):
    '''
    receive list (numbers)
    print the smallest and largest numbers found in the list
    '''
    print(f'The smallest numbers is {min(lst)} and the largest is {max(lst)}')

#75
def find_totals(lst):
    '''
    receive a list (numbers)
    go through the list, if the number is positive add it to total_positive, otherwise if its negative add it to total_negative
    print the total_positive and the total_negative
    '''
    total_positive = 0
    total_negative = 0
    for number in lst:
        if number > 0:
            total_positive += number
        elif number < 0:
            total_negative += number
    print(f'Total of positive numbers is {total_positive} and total of negative numbers is {total_negative}')


#76
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
def reverse_order(lst):
    '''
    receive a list (numbers)
    create a new list and copy the received list starting at the end (index -1)
    '''
    rev_lst = []
    rev_lst.append(lst[::-1])
    print(rev_lst)

#77
def print_numbers_backwards():
    '''
    ask user for 10 numbers and add (insert) the number to index 0 in your array
    print array
    '''
    numbers = []
    for i in range(10):
        number = input('Enter a number: ')
        numbers.insert(0, number)
    print(numbers)

```