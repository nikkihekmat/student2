---
comments: True
layout: post
title: Passion Project Code
description: the code that I contributed to my group's passion project
type: hacks
courses: {'compsci': {'week': 12}}
---

### <center> Genre Information Page </center>

<body> <br>
    <center>
    <a class="button-link" href="http://127.0.0.1:4100/frontend_shared//2023/10/16/Book_Genres_IPYNB_2_.html"> Genre Information</a>
    </center>
</body>

- just use of markdown

<br>

### <center> Find Your Next Read Page </center>

<body> <br>
    <center>
    <a class="button-link" href="http://127.0.0.1:4100/frontend_shared/basics/nextread"> Find Your Next Read</a>
    </center>
</body>

```
<h1>Helpful Sites to Find Popular Books</h1>

<div>
    <p>Barnes and Noble will feature the most popular books in every genre on their website, making it easy for you to start your reading journey on the right foot!</p>
    <a href="https://www.barnesandnoble.com/b/books/_/N-1fZ29Z8q8"><button> Barnes and Nobles Top 100 Books </button></a>
</div>

<div>
    <p>The New York Times ranks books on their bestseller list, making it a valuable source for finding a great new read.</p>
    <a href="https://www.nytimes.com/spotlight/books-to-read"><button> The New York Times Bestseller List </button></a>
</div>

<div>
    <p>Goodreads is also popular, as it's a platform where thousands of readers can rate books in an online forum; though, you do need an account.</p>
    <a href="https://www.goodreads.com/"><button> Goodreads</button></a>
</div>

```
<br>

### <center> Blind Book Date Page </center> 
 
<body> <br>
    <center>
    <a class="button-link" href="http://127.0.0.1:4100/frontend_shared/basics/blinddate">Blind Book Date</a>
    </center>
</body> 

```
<html>

<head>
    <title>Random Book Generator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f2f2f2;
            padding: 20px;
        }

        .book-box {
            background-color: #fff;
            border-radius: 5px;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
        }

        .new-book {
            background-color: #007BFF;
            color: #fff;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
        }

        .new-book:hover {
            background-color: #0056b3;
        }
    </style>
</head>

<body>
    <div id="book-box">
        <h1>Random Book Generator</h1>
        <p id="book">Click the button to get a random book recommendation.</p>
        <button id="new-book">New Book</button>
    </div>

    <script>
        const books = [
            "To Kill a Mockingbird by Harper Lee",
            "1984 by George Orwell",
            "The Hobbit by J.R.R. Tolkien",
            "Harry Potter and the Sorcerer's Stone by J.K. Rowling",
            "The Lord of the Rings by J.R.R. Tolkien",
            "The Love Hypothesis by Ali Hazelwood",
            "The Spanish Love Deception by Elena Armas",
            "The Alchemist by Paulo Coelho"
        ];

        const bookElement = document.getElementById("book");
        const newBookButton = document.getElementById("new-book");

        newBookButton.addEventListener("click", function () {
            if (books.length === 0) {
                bookElement.textContent = "No books available.";
            } else {
                const randomIndex = Math.floor(Math.random() * books.length);
                bookElement.textContent = "How about reading: " + books[randomIndex];
            }
        });
    </script>
</body>

</html>
```

<br>

### <center> Major Database Work </center>

- I essentially lead the initiative of logging 95 books in our database