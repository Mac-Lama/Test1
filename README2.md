# Personal Library Management System

This system allows users to add, remove, sort, and search for books stored in memory / a file. The project allows the user to:
  - Add a new book to the collection/database, based on whether it is a textbook or a fiction book.
  - Remove a book using the ISBN.
  - See a display of the books, and choose whether to sort by title or author.
  - Search for a book by title using a recursive search algorithm.
  - Store books in the memory using an ArrayList.
  - Persist the books in a file using file I/O.
      - When the application restarts, it loads from the filesystem.

This system also:
  - Uses exception handling to catch invalid input or file errors.
  - Implements the Comparable interface for sorting.

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
