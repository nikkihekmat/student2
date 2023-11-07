---
comments: True
layout: post
title:  Student Teaching Notes
description: collective notes from the student teaches 
type: hacks
courses: {'compsci': {'week': 7}}
---

# Overall
- refer to hacks of each assignment for great examples of content absorbed 
- This page is more of a summary of each lesson because I learn better by knowing the general information of something and then seeing the examples in depth first hand. For me all the content in the student lessons was valuable to me, so I can't really pull apart the most important things to remember.

### Data Abstraction
- learned how to write a variable 
- ex: num = 1
- learned how to call to different variables, how they can override each other in a puzzle format

A data type is a type of variable, and these are 3 of the 4 main types: 
- integer: a mathematical number
- boolean: a yes/no or true/false statement
- text (or string): for any text-based variable (including phone numbers)

## Algorithms
- can type in standard mathematical operations with some twists
- learned a bit about psuedo code 

    **Psuedo code example with action code in ALL CAPS:**

    ```
    SET largestNumber to 0
    Create a list of numbers
    Iterate through each number in the list
        FOR number in numberList
            IF number is larger than largestNumber THEN set largestNumber to number
            IF there are more numbers in list, THEN go back to step 2
            END IF
            END IF
        END FOR
    PRINT largestNumber
    ```

    **College board exmaple of psuedo code WITHOUT action code in ALL CAPS:**

    ```
    1. Set largest number to 0
    2. Get next number in the list
    3. If number is larger than largestNumber then set largestNumber to number
    4. If there are more numbers in list, go back to step 2
    5. Display largest number
    ```
    **Actual code for comparison:**

    ```
    largestNumber = 0

    numberList = [5, 8, 3, 12, 7, 10]

    for number in numberList:
        if number > largestNumber:
             largestNumber = number

    print("Largest number:", largestNumber)
    ```

## Boolean If
- true/false operation
- relational and logical operators 
- learned how to call back to operators 
- learned how to establish simple conditionals

    **psuedo code vs regular code**
    - I'm making it this way for now for better comprension on my part 
    ```
    num = 7                 // Assign the value 7 to the variable 'num' 
    isEven = num % 2 == 0   // Check if 'num' is even and store the result in 'isEven'
    range = (num > 5) and (not num > 10)  // Check if 'num' is greater than 5 and not greater than 10, and store the result in 'range'
    display(isEven or range)  // Display the result of the logical OR operation between 'isEven' and 'range'
    ```

## Developing Algorithms
- can use algorithms to organize lists
- can calculate mean, median, and mode

Type of algorithm:
 ```
Display "What did you get on your test?"
Read testScore from the user as an integer

IF testScore > 90:
    Display "You got an A!"
END IF

IF testScore > 70:
    Display "Congratulations. You didn't fail."
END IF

IF testScore < 70:
    Display "You failed."
END IF 
 ```

## DTMA
- binary and sequential search 
- if/else statemnts

    **Accessing Elements in a List**
    ```
    1. define a list
    2. print an element from the list
    ```

    **Storing Element at an Index to a Variable**

    ```
   1. set element to the third element in a list
   2. print the element 
    ```

    **Setting an Element at an Index to a Variable**

    ```
   1. set element to 4
   2. call on the 5th element from a list
   3. print the fifth element
    ```

    **Insert a Value at a Certain Index**

    ```
   1. Insert the value 10 at index 3 in the list aList.
   2. Print the value at index 3 of aList.
    ``` 

    **Adding another value to the list (append)**

    ```
   1. Append the value 5 to the end of the list aList.
   2. Print the contents of aList.
    ``` 

    **Removing a value from the List at a Specific Index**

    ```
   1. Remove the value 2 from the list aList.
   2. Print the contents of aList.
    ``` 

    **Accessing the Length of a list**

    ```
   1. Print the length of the list aList.
    ``` 

## Developing Procedures
- sorting things into classes
- too complicated for me to show in psuedo code and actually comphrehend--refer to student teach notebook

## Libraries
- libraries are stored modules of data that you have to download in order to call upon
- one example is calling upon operations from a math library 

1. Modules: Libraries in Python consist of modules, which are individual Python files containing functions, classes, and variables related to a specific set of tasks or a particular domain. You can import these modules into your own Python code to access their functionality.

2. Standard Library: Python comes with a comprehensive standard library that includes modules for various tasks, such as working with files, networking, data processing, and more. These modules are readily available and do not require installation.

3. Third-party Libraries: In addition to the standard library, there is a vast ecosystem of third-party libraries created by the Python community. These libraries cover a wide range of domains, including web development, data analysis, machine learning, game development, and more. Some popular third-party libraries include NumPy, Pandas, Matplotlib, TensorFlow, Django, Flask, and many others.

    ```
    Import the square root function from the math module.
    Import the random module.

    Set the variable num to 64.
    Print the square root of num.

    Create a list called numList with elements [1, 2, 3, 4, 5, 6].
    Print a random choice from numList.

    ```

- APIs define the methods and functions that are available for developers to interact with a library. They specify how to make requests, provide inputs, and receive outputs, creating a clear and consistent way to use library features.

    **Types of Libraries**

    -  Requests: Simplifies working with HTTP servers, including 'request'-ing data from them, and recieving it
    - Pillow: Simplifies image processing
    - Pandas: Simplifies data analysis & manipulation
    - Numpy: Vastly quickens functionality of arrays up to 50 times faster than regular python list
    - Scikit-Learn: Implements machine learning models and statistical modelling
    - Tensorflow: Data automation, model tracking, performance monitoring, and model retraining
    - Matplotlib: Creates static, animated, and interactive visualizations in Python

## Simulations 
- algorithmic efficiency 
- different types of quick counting

- A simulation, in context of computer science, is a digital representation of a situation in the real world.
- Examples:
    - Experiments: When an experiment is to dangerous to perform in the real world or too expensive, a simulation can be made of it and be performed digitally.
    - Training and Education: Simulations such as flight simulators and medical simulation can be very practical in aiding dangerous proffesions to receive training.
    - Video Games: Some video games try to aim to be as releastic as possible with physics and graphics to try to simulate the real world.

    **Dice Roll**

    ```
    Import the random module.

    Define a function named roll_die:
     - The function returns a random integer between 1 and 6.
    
    Assign the result of calling the roll_die function to a variable named "result."
    Print "Roll:" followed by the value of the "result" variable. 
    ```

    **Bubble Sort vs. Quick Sort**

    - Bubble sort is a simple but inefficient sorting algorithm with O(n^2) time complexity
    - Quicksort is a more efficient divide-and-conquer sorting algorithm with an average time complexity of O(n log n)
    - Quicksort typically preferred choice for practical sorting