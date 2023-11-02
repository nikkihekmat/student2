---
comments: True
layout: post
title: Daily Plan
description: my daily plan for the week
type: hacks
courses: {'compsci': {'week': 7}}
---

## Relational Operators

- A boolean value is either true or false
- Typically yes or no questions like “do I have a dog?”
- So when you write an expression to evaluate, you need to use different types of relational operators determining on the questions that we’re trying to ask
    - Ex: when trying to test to see whether or not two values or two variables are equal, then you use the equal sign to check whether or not two values or two variables contain the same value
        - a = b [equal to] numStudents = 30
        - This checks whether the value is also equal to 30
- You can also use the not equal sign to evaluate whether or not two values are not equal to each other
    - a ≠ b [not equal to] count ≠ 10
- We can also use the greater than or less than symbol to check whether or not something is greater than or less than then the other
    - a > b [greater than] grade > 70
- ou can also use the greater/less than or equal to
    - a ≥ b [greater than or equal to] numPets ≥  0


```python
num1 = 5  
num2 = 7  

are_equal = num1 == num2

print(are_equal)  # This will print False in this example
```

    False



```python
#Popcorn Hack

num1 = 5
num2 = 5

are_equal = num1 == num2

print(are_equal)

```

    True



```python
num1 = 5  
num2 = 7  

are_not_equal = num1 != num2

print(are_not_equal)  # This will print True in this example
```


```python
num1 = 8  
num2 = 7  

is_less_than = num1 < num2

print(is_less_than)  # This will print True in this example
```

    False



```python
num1 = 5  
num2 = 7  

is_greater_than = num1 > num2

print(is_greater_than)  # This will print False in this example
```

    False


# Logical Operators
- NOT condition: flips what is currently stored in the variable without impacting the variable/condition itself
- AND condition: checks both conditions to produce one single Boolean true or false
- OR condition: checks whether or not one of the conditions is true or false
- These logical operators can be used with boolean expressions to produce a single Boolean value


```python
# not condition
isRaining = False
result = not isRaining
print(result)
```

    True



```python
# and conditions
grade = 85
result = grade > 70 and grade < 100
print(result)
grade = 59
result = grade > 70 and grade < 100
print(result)
```

    True
    False



```python
# or conditions
score = 175
highScore = 150
lives = 2
result = (score > highScore) or (lives > 3)
print(result)
score = 175
highScore = 150
lives = 2
result = (score < highScore) or (lives > 3)
print(result)
```

    True
    False


## Popcorn Hack
- Create a code segment with an OR operator that is True. With the same score, change the conditions and create another expression that prints False instead of True.


```python
score = 40
highScore = 50
lives = 5
result = (score > highScore) or (lives > 3)
print(result)

score = 40
highScore = 50
lives = 5
result = (score > highScore) or (lives < 3)
print(result)
```

    True
    False


# Relational & Logical Operators

- Boolean values are either true or false
- relational operators: =,≠, >, <, ≥, and ≤


```python
# call back to relational operators
a = b
a ≠ b
a > b
a < b
a ≥ b
a ≤ b

```

These are used to test the relationship between two variables, expressions, or values. A comparison between a relational operator evaluates to a Boolean value. 


```python
# call back to logical operators
result = not isRaining # not condition

result = (score > highScore) or (lives > 3) # or condition

result = grade > 70 and grade < 100 # and condition
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[9], line 2
          1 # call back to logical operators
    ----> 2 result = not isRaining # not condition
          4 result = (score > highScore) or (lives > 3) # or condition
          6 result = grade > 70 and grade < 100 # and condition


    NameError: name 'isRaining' is not defined


## Different Expressions, Same Results

- age ≥ 16
- age > 16 or age = 16
- NOT age < 16


## Example


```python
num = 7
isEven = num % 2 == 0
range = (num > 5) and (not num > 10)
display (isEven or range)

```


    True



```python
# practice
name = "Hannah"
age = 17
display ((not (name == "Hannah")) or (age < 20))
```


    True


## Popcorn Hack

Create a Boolean expression using your favHobby as a variable and the number of classes you are taking as the second variable.
- Must have:
- favHobby and number of classes --> 2 variables
- display expression; NOT and OR logical operators
- one false expression and one true expression = overall true


```python
# start with
favHobby = "writing" 
numClasses = 4
display((not (favHobby == "writing")) or (numClasses < 6))
```


    True


# learning objective: write algorithms that uses selection without using a programming language
## vocab
selection: determines which part of an algorithm are executed based on condition being true or false
algorithm: a finite set of instructions that accomplish a specific task
### ex determine if a number is in range
- get number from user
- is number greater than - and less than 10
- if yes display number
- if no display goodbye

# participation hack:
give me different ways you would determine if a kid needs to go to tutoring

- if a kid plays too many sports, then they'll need tutoring 
- if a kid's grades are dropping, then they'll need tutoring

# writing conditionals
### format
if (condition) :
    <block of statements>
- if the condition evaluates to true then the block of statements occurs
- if not then no action is taken
or
if (condition) :
    <first block of statements>
else:
    <second block of statements>
-  if the condition is true then first block is executed if false then the second black or else statement is executed

## Example -- multiple of 3?


```python
number = 9
if number % 3 == 0 :
    print ("multiple of 3")
else:
    print ("not multiple of 3")
```

    multiple of 3


# Popcorn Hack
calculate the sum of two numbers -> if the sum is greater than 100 display 100, otherwise display the sum.


```python
num1 = 40
num2 = 70
sum = num1 + num2
if sum > 100 :
    print ("sum greater than 100")
else: 
    print("sum not greater than 100")
    
```

    sum greater than 100


help you guys get started:
num 1 =
num 2 =
sum = num 1 + num 2
if ():
else :

# We can do conditional statements using if blocks that just choose or do one particular outcome based off of a condition
# Or you can do if-else blocks to choose from two different outcomes

IF (condition)
{
	<block of statements>
}
ELSE
{
	<second block of statements>
}
The else only activates if the “if condition” is FALSE

# Example 1: if-elif-else block


```python

y = 7
if y > 10:
    print("y is greater than 10")
elif y == 10:
    print("y is equal to 10")
else:
    print("y is less than 10")

```

    y is less than 10


- conditional statements, or “if-statements,” affect the sequential flow of control by executing different statements based on the value of a boolean expression
- The if/else statement executes a block of code if a specified condition is true. If the condition is false, another block of code can be executed.
- we use an if-elif-else block to check the value of the variable y. It first checks if y is greater than 10, then if it's equal to 10, and finally, if neither of these conditions is met, it executes the code inside the else block.

## Homework:

## Hack 1
Write two Boolean expressions to check if the average grades of student1, student2, and student3 is at least 85. Write one expression that is false and one that is true.
## Hack 2
You can't go outside if the temperature is less than 20 **AND** the weather is stormy. Write the Boolean expression for the scenario.
Screenshot your work and put it on a Google document. Share the link with Ellie Rozenkrants on Slack by Oct 12 11:59 PM.



```python
# Hack 1 Expression 1

student1 = 85
student2 = 85
student3 = 85

sum = student1 + student2 + student3

count = 3

result = (sum/count >= 85) or (sum/count < 85)
print(result)

# Hack 1 Expression 2

student1 = 85
student2 = 85
student3 = 85

sum = student1 + student2 + student3

count = 3

result = (sum/count > 85) or (sum/count < 85)
print(result)


```

    True
    False



```python
# Hack 2

temperature = 15
is_stormy = True  

can_go_outside = (temperature >= 20) and (not is_stormy)

if can_go_outside:
    print("You can go outside.")
else:
    print("Stay indoors.")

```

    Stay indoors.

