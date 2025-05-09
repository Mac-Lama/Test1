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
           1) Add  
           2) Remove  
           3) Display  
           4) Search  
           5) Exit
