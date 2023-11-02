---
comments: True
layout: post
title: JavaScript Basics Test
description: JS Basics Test due Thursday 9/28
type: hacks
courses: {'compsci': {'week': 6}}
---

# Hack 1: HTML

<h3> Helpful Sites to Find Popular Books </h3>

<div> 
    <p>Barnes and Nobles will feature the most popular books in every genre on their website, making it easy for you to start your reading journey on the right foot!</p>
    <a href="https://www.barnesandnoble.com/b/books/_/N-1fZ29Z8q8"> <button>Barnes and Nobles Top 100 Books</button> </a>
</div>

<div>
    <a href="https://www.nytimes.com/spotlight/books-to-read"> The New York Times Bestseller List </a>
    <a href="https://www.goodreads.com/"> Goodreads </a>
    <p>The New York Times ranks books on their bestseller list, making it a valuable source for finding a great new read. Goodreads is also popular, as it's a platform where thousands of readers can rate books in an online forum; though, you do need an account.</p>
</div>

<div>
    <p>Here are the top recommended books from the major publishing houses in the US.</p>
    <a href ="https://www.penguinrandomhouse.com/books/best-sellers/"> Penguin Random House Fiction Bestsellers</a>
    <a href ="https://www.simonandschuster.com/search/books/Bestsellers/_/N-i9v/Ne-pgx"> Simon and Schuster Bestsellers</a>
</div>

# Hack 2: Data Types


```python

%%js

var me = { 
    name: "nikki",
    age: 17,
    current classes: ["AP Literature","AP Human Geography","AP US Government and Politics","AP Computer Science Principles,"],
    interests: ["reading","creative writing","social justice","Middle Eastern representation"],
    number of siblings: 1,
    books: "The Other Side of the Forest, currently due in the Spring of 2024"
    }

console.log(me)

me.interests.append("animals")
console.log(me)
console.log(me["interests"])

console.log("My age next year: "+(me["age"]+1))

console.log(typeof me["name"])
console.log(typeof me["age"])
console.log(typeof me["number of siblings"])
```


    <IPython.core.display.Javascript object>


# Hack 3: DOM


```python
%%html

<h3> Helpful Sites to Find Popular Books </h3>

<div> 
    <p id="la">Barnes and Nobles will feature the most popular books in every genre on their website, making it easy for you to start your reading journey on the right foot!</p>
    <a href="https://www.barnesandnoble.com/b/books/_/N-1fZ29Z8q8"> <button id="btn">Barnes and Nobles Top 100 Books</button> </a>
</div>

<div>
    <a href="https://www.nytimes.com/spotlight/books-to-read"> The New York Times Bestseller List </a>
    <a href="https://www.goodreads.com/"> Goodreads </a>
    <p>The New York Times ranks books on their bestseller list, making it a valuable source for finding a great new read. Goodreads is also popular, as it's a platform where thousands of readers can rate books in an online forum; though, you do need an account.</p>
</div>

<script>
    document.getElementById("btn").addEventListener("click", function() {
    var links = document.getElementsByTagName("a");
    for (let i = 0; i < links.length; i++) {
      links[i].href = "https://www.nytimes.com/spotlight/books-to-read"; 
    }
    document.getElementById("la").innerHTML = "Switched!";
  });
</script>
```



<h3> Helpful Sites to Find Popular Books </h3>

<div> 
    <p id="la">Barnes and Nobles will feature the most popular books in every genre on their website, making it easy for you to start your reading journey on the right foot!</p>
    <a href="https://www.barnesandnoble.com/b/books/_/N-1fZ29Z8q8"> <button id="btn">Barnes and Nobles Top 100 Books</button> </a>
</div>

<div>
    <a href="https://www.nytimes.com/spotlight/books-to-read"> The New York Times Bestseller List </a>
    <a href="https://www.goodreads.com/"> Goodreads </a>
    <p>The New York Times ranks books on their bestseller list, making it a valuable source for finding a great new read. Goodreads is also popular, as it's a platform where thousands of readers can rate books in an online forum; though, you do need an account.</p>
</div>

<script>
    document.getElementById("btn").addEventListener("click", function() {
    var links = document.getElementsByTagName("a");
    for (let i = 0; i < links.length; i++) {
      links[i].href = "https://www.nytimes.com/spotlight/books-to-read"; 
    }
    document.getElementById("la").innerHTML = "Switched!";
  });
</script>



# Hack 4: JavaScript


```python
%%js

console.log("If statements + Operators")
var a = 17
var b = 37

if (a > b) {
    console.log("a is more than b")

} else if (a == b) {
    console.log("a is the same as b")

} else  {
    console.log("a is less than b")
}
```


    <IPython.core.display.Javascript object>


# Hack 5: JS Debugging


```python
%%js

# Segment 1: Alphabet List

var alphabet = "abcdefghijklmnopqrstuvwxyz";
var alphabetList = [];

alphabetList = alphabet.split()

for (var i = 0; i < 25; i++) {
	alphabetList.push(alphabetList[i]i);
}

console.log(alphabetList);

# What I changed . . .

## changed iterator from 1 to 25 to match the length of the alphabet
## changed push instruction to add the letter at the iterator position to the list instead of the iterator itself 

```


    <IPython.core.display.Javascript object>



```python
%%js

# Segment 2: Numbered Alphabet

var alphabet = "abcdefghijklmnopqrstuvwxyz";
var alphabetList = [];
var letterNumber = 0

for (var i = 0; i < alphabet.length; i++) {
	alphabet.push(alphabet[i]);
	letterNumber += 1
 
 	if (i == 4) {
		console.log(alphabetList(i) + " is letter number " + letterNumber +" in the alphabet")
	}
}

// Should output:
// "e" is letter number 5 in the alphabet

# What I changed . . .

## changed value of the variable letterNumber from 5 to 0; allows it to print all letters from a-z with their corresponding positions by using alphabetList.push(alphabet[i]) and increasing letterNumber by 1 everytime the loop ran
## by further restricting what is printed using an if statement to guarantee that i == 4, able to only print that e is letter number 5 in the alphabet
```


    <IPython.core.display.Javascript object>



```python
%%js

# Segment 3: Odd Numbers

let odds = [];
let i = 1;

while (i <= 10) {
  odds.push(i);
  i += 2;
}

console.log(odds);

## What I changed . . .

# changed evens to odds
# changed i to 1 so that when you add 2 each time to 1 it give you an odd list than an even list
```

# Review Ticket

Eashan Reddy

- expanded on extra websites for first hack
- went above and beyond by organizing everything in one page neatly
- met expectations for other tasks
- deserves at least a 94% 
