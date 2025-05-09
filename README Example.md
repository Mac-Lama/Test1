# 📚 Library Management System

A console-based Java application for managing a personal library. This system allows users to add, remove, sort, and search for books stored in memory and persisted to a file. The project demonstrates core object-oriented programming principles such as inheritance, polymorphism, interfaces, recursion, and file I/O.

---

## ✨ Features

- 📖 **Add Books** – Add either a Fiction book or Textbook with full details
- ❌ **Remove Books** – Remove books by ISBN
- 📄 **Display Books** – View all books sorted by title or author
- 🔍 **Search Books** – Recursively search for a book by title
- 💾 **Persistent Storage** – Books are saved and loaded from `books.txt`
- 🧠 **OOP Principles Used**:
  - Inheritance (`Book`, `FictionBook`, `Textbook`)
  - Polymorphism (processing books through the base class)
  - Interface (`Comparable<Book>`) for sorting
  - Recursion for title-based search
  - Exception handling for file and input errors

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
           | +compareTo()   |
           | +equals()      |
           | +toString()    |
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
```

---

## 🛠️ How to Compile & Run

### ✅ Requirements
- Java Development Kit (JDK) 8 or higher

### 📂 File Structure

- `Book.java` – Abstract base class
- `FictionBook.java` – Subclass representing fiction books
- `Textbook.java` – Subclass representing textbooks
- `BookManager.java` – Main class (contains `main()` method)

### 🔧 Compile the Program

Ensure all files are in the same directory, then run:

```bash
javac *.java
```

### ▶️ Run the Program

```bash
java BookManager
```

---

## 🕹️ Program Usage

Upon launch, the program presents the following menu:

```
1) Add  2) Remove  3) Display  4) Search  5) Exit
Choose:
```

### Menu Options:

- **Add** – Choose book type (Fiction/Textbook) and provide details
- **Remove** – Remove a book by entering its ISBN
- **Display** – Display all books sorted by Title or Author
- **Search** – Recursively search for a book by title
- **Exit** – Saves the books to `books.txt` and exits

---

## 💾 Data Persistence

Books are stored in a file called `books.txt`. Data is automatically loaded on startup and saved on exit.

### Example `books.txt` Content

```plaintext
Fiction|Dune|Frank Herbert|1965|9780441013593|Science Fiction
Textbook|Java Programming|Joyce Farrell|2019|9781337397070|Computer Science|9th Edition
```

Each entry begins with the type (`Fiction` or `Textbook`), followed by the relevant fields.

---

## ⚙️ Implementation Highlights

- 🔁 **Recursive Search**: Implemented via a linear recursive method in `BookManager`
- 📚 **ArrayList**: Used for dynamic in-memory book management
- ❗ **Exception Handling**: Robust input and file error handling
- 🔤 **Case-insensitive Matching**: Used for sorting and searching
- 🔑 **ISBN-Based Uniqueness**: Book identity is based on ISBN

---

## 🧪 Sample Interaction

```
1) Add  2) Remove  3) Display  4) Search  5) Exit
Choose: 1
Type (1) Fiction (2) Textbook: 1
Title: The Hobbit
Author: J.R.R. Tolkien
Year: 1937
ISBN: 9780547928227
Genre: Fantasy
Added: The Hobbit | J.R.R. Tolkien | 1937 | ISBN:9780547928227 | Genre:Fantasy
```

---

## 👨‍💻 Author

*Your Name Here*

---
