---
comments: True
layout: post
title: Daily Plan
description: my daily plan for the week
type: hacks
courses: {'compsci': {'week': 7}}
---

### Pseudo Code vs. a Python Algorithm
Pseudo Code is essentially describing/writing code in a more "human-written" format rather than formally/actually "coded" format.

Below, see examples highlighting the key difference(s) between a coded (Python) algorithm against a College Board Pseudo Code example.

![College_Board_Algorithms_Diagram.png](College_Board_Algorithms_Diagram.png)

**College Board Pseudo Code example**

Below is an algorithm to find the largest number in a list of positive numbers.
1. Set largest number to 0
2. Get next number in the list
3. If number is larger than largestNumber then set largestNumber to number
4. If there are more numbers in list, go back to step 2
5. Display largest number

```python
largestNumber = 0

numberList = [5, 8, 3, 12, 7, 10]

for number in numberList:
    if number > largestNumber:
        largestNumber = number

print("Largest number:", largestNumber)
```

    Largest number: 12


## 3.3 - Mathematical Expressions/Operations in Algorithms

Mathematics in algorithms may involve many of the basic actions we all know to be part of the Order of Operations. This includes basic addition (a + b), subtraction (a - b), multiplication (a * b), and division (a / b).

However, there is also a likely unfamiliar action named Modulus (in Python: a % b).

MOD: (a / b -> whatever remains).

NOTE: in PEMDAS, MOD is held at the same level as multiplication and divison.


```python
# arithmetic operations
# (a + b)
num1 = 4
num2 = 7
print(num2 + num1)

# (a - b)
num1 = 3
num2 = 9
print(num2 - num1)
```

    11
    6



```python
# order of operations example below with grades
# remember PEMDAS
num1 = 12
num2 = 25
num3 = 14
answer = num1 / 4 * num3 + 9
print(answer)
```

    51.0


## Popcorn Hack #1
Create YOUR OWN order of operations problem like the one above using any values and operations in any order (ex: addition, multiplication, MOD).

Hint: remember to define your values, as seen above.


```python
# use this code cell to make your own calculation!

num1 = 42
num2 = 23
num3 = 4

answer = num1 * num3 / num2 + 102
print(answer)

```

    109.30434782608695


### Fibonacci and Factorial

What is a sequence of **FIBONACCI?**

A Fibonacci sequence is a series of numbers in which each number is the sum of the two preceding ones. It commonly starts with 0 and 1, and the sequence continues infinitely. The first few numbers in the Fibonacci sequence can be seen below.

0, 1, 1, 2, 3, 5, 8, 13, 21, 34,...

Fibonacci function example:


```python
def fibonacci(n):
    if n <= 0:
        return []
    elif n == 1:
        return [0]
    elif n == 2:
        return [0, 1]
    else:
        fib_sequence = [0, 1]
        while len(fib_sequence) < n:
            next_number = fib_sequence[-1] + fib_sequence[-2]
            fib_sequence.append(next_number)
        return fib_sequence

n = 10
result = fibonacci(n)
print(result)
```

    [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]


What is **FACTORIAL?**

In mathematics, the factorial of a non-negative integer, denoted by the symbol "!", is the product of all positive integers from 1 to that integer. The notation is typically a number with "!" after (ex: n!)

Example of factorial: 5! = 5 x 4 x 3 x 2 x 1 = 120

Factorial function example:


```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)

n = 6
result = factorial(n)
print(f"{n}! = {result}")
```

    6! = 720


## Popcorn Hack #2
Complete the following tasks.
Fill in the blank numbers in the segment of a Fibonacci sequence below:

[3, 5, 8, 13, 21, 34, 55, 89, 144]

Write the answer to the following factorials:

- 4! = 24
- 6! = 720
## 3.4 - Strings

What is a string?

- Strings are ordered sequences of characters
    - Ex: characters can be numbers, letters, special characters like underscores, or even spaces
- Substring: a substring can be described as part of an already existing string
- String concatenation: joins two or more strings end-to-end to make a new string
- Note that each programmming language has its own procedures, methods, or functions for strings
    - We will be covering Python

Let's look at some of the string examples below.

Below is "len(str)". This command counts the number of characters in a word (str) and returns that number. For example, for the word "happy" ("len('happy')"), the value returned would be 5.


```python
# len example:

string = "Hello, World!"
stringLength = len(string)
print(f"The string length is {stringLength} characters.")
```

    The string length is {stringLength} characters.


Below is "concat(str1, str2)". This returns a single string consisting of "str1" immediately followed by the characters of the second string ("str2"). For example, "concat('AP', 'class')" would return "APclass".


```python
# concat example:

string1 = "Hel"
string2 = "lo!"

# concatenation seen right below

result = string1 + string2
print(result)
```

    Hello!


Below is a substring "substring(str1, start, length)". This returns a substring of consecutive characters from "str1", starting with the character at position "start" and containing "length" characters. For example, "substring('APCSPrinciples', 3, 6)" would return "CSPrin".


```python
# substring example:

string = "Hello, World!"
substring = string[2:10]
print(substring)
```

    llo, Wor


### Palindromes

The most commonly known definition of a palindrome is represented as being a word or phrase that is spelt the same both forward and backward.

For example, the word "racecar" is a palindrome, because the word is the same whether you read it from left to right or vice versa.


```python
# palindrome example

def is_palindrome(s):
    s = s.lower().replace(" ", "").replace(",", "").replace("!", "")
    return s == s[::-1]

word = "racecar"
print(f"{word} {'is' if is_palindrome(word) else 'is not'} a palindrome.")
```

    racecar is a palindrome.


## Popcorn Hack #3
Decide if the following code cell is a "len(str)", a concatenation, or a substring.


```python
# len, concat, or substring?

thing1 = "creative"
thing2 = "writer"
result = thing1 + thing2
print(result)

# type your answer HERE: CONCAT
```

    creativewriter


# Homework Hacks

### Hack #1
1. Concatenate your first and last name and print it (full name).

2. Select/write a random sentence of your choice (be creative; it can be whatever you want it to be) and calculate the number of characters in it and display that as the result.


```python
# put your work for Hack #1 in here below:
thing1 = "Nikki"
thing2 = "Hekmat"
result = thing1 + thing2
print(result)

string = "Harry Potter is quite literally the best franchise in the world."
stringLength = len(string)
print(f"The string length is {stringLength} characters.")
```

    NikkiHekmat
    The string length is 64 characters.


### Hack #2
Similarly to the first Popcorn Hack, create your own order of operations problem (PEMDAS) in a code cell, but this time using modulus/MOD (a % b).

**Try to make your answer not have a decimal in it.**


```python
# put your work for Hack #2 in here below:

num1 = 12
num2 = 4
num3 = 40

answer = num1 % num2 + num3
print(answer)

```

    40

