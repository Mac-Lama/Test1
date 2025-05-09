# Test1

# 📚 Library Management System

A console-based Library Management System that allows users to manage a personal library by adding, removing, searching, and sorting books. This project demonstrates core object-oriented programming principles such as inheritance, polymorphism, interfaces, recursion, and file I/O in Java.

---

## ✨ Features

- Add new books (Fiction or Textbook) with detailed information
- Remove books by ISBN
- Display all books sorted by **title** or **author**
- Recursive search for books by title
- In-memory storage using `ArrayList`
- Persistent storage using file I/O
- Error handling for invalid input and file operations
- Demonstrates:
  - Inheritance (`Book`, `FictionBook`, `Textbook`)
  - Polymorphism (handling different book types generically)
  - Interface implementation (`Comparable<Book>` for sorting)
  - Recursion (title-based search)
  - Abstract classes and method overriding

---

## 🧱 Class Design Overview

### UML Diagram (Simplified)

```plaintext
           +----------------+
           |   <<abstract>> |
           |     Book       |
           +----------------+
           | - title        |
           | - author       |
           | - year         |
           | - isbn         |
           +----------------+
           | +getTitle()    |
           | +getAuthor()   |
           | +getYear()     |
           | +getIsbn()     |
           | +toString()    |
           | +compareTo()   |
           | +equals()      |
           | +toDataString()|
           +--------+-------+
                    ^
        +-----------+------------+
        |                        |
+----------------+     +----------------+
|  FictionBook    |     |   Textbook     |
+----------------+     +----------------+
| - genre         |     | - subject      |
|                 |     | - edition      |
+----------------+     +----------------+
| +getGenre()     |     | +getSubject()  |
| +toString()     |     | +getEdition()  |
| +toDataString() |     | +toString()    |
+----------------+     | +toDataString() |
                       +----------------+
