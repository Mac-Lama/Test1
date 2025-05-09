# Personal Library Management System

This system allows users to add, remove, sort, and search for books stored in memory / a file. 

---

## Features

-  **Add Books** – Add either a Fiction book or Textbook with full details
-  **Remove Books** – Remove books by ISBN
-  **Display Books** – View all books sorted by title or author
-  **Search Books** – Recursively search for a book by title
-  **Persistent Storage** – Books are saved and loaded from `books.txt`
-  **OOP Principles Used**:
    - Inheritance (`Book`, `FictionBook`, `Textbook`)
    - Polymorphism (processing books through the base class)
    - Interface (`Comparable<Book>`) for sorting
    - Recursion for title-based search
    - Exception handling for file and input errors

---

## UML Diagram

```plaintext
           ------------------
           |  <<abstract>>  |
           |     Book       |
           ------------------
           | - title        |
           | - author       |
           | - year         |
           | - isbn         |
           ------------------
           | +getTitle()    |
           | +getAuthor()   |
           | +getYear()     |
           | +getIsbn()     |
           | +compareTo()   |
           | +equals()      |
           | +toString()    |
           | +toDataString()|
           ------------------
                    |
        --------------------------
        |                        |
------------------      -----------------
|  FictionBook    |     |   Textbook     |
------------------      ------------------
| - genre         |     | - subject      |
|                 |     | - edition      |
------------------      -------------------
| +getGenre()     |     | +getSubject()   |
| +toString()     |     | +getEdition()   |
| +toDataString() |     | +toString()     |
-------------------     | +toDataString() |
                        -------------------
```

---

## How to Run

1. Run the program in the `BookManager.java` file
2. Choose between the prompted options:
   
           1) Add - Choose book type (Fiction/Textbook) and provide details
           2) Remove - Remove a book by entering its ISBN
           3) Display – Display all books sorted by Title or Author
           4) Search - Recursively search for a book by title
           5) Exit – Saves the books to `books.txt` and exits
   
---

## Data Saving

Books are uploaded and saved in a file called `books.txt`. Data is automatically loaded on startup and saved on exit.

---

## Sample

```
1) Add  2) Remove  3) Display  4) Search  5) Exit
Choose: 1
Type (1) Fiction (2) Textbook: 1
Title: Ready Player One
Author: Ernest Cline
Year: 2011
ISBN: 97803078877443
Genre: Science Fiction
Added: Ready Player One | Ernest Cline | 2011 | ISBN: 97803078877443 | Genre: Science Fiction
```

---
