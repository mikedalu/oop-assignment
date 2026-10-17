# Python OOP Assignment: Library Book Tracker

**Objective:** Build a simple Python application to manage a digital library. In this assignment, you will build two interacting classes (`Book` and `Library`) to practice core Object-Oriented Programming (OOP) concepts: **Classes & Objects**, **Instance Attributes & Methods**, **Encapsulation**, and **Collection Management**.

---

## 📖 Scenario

You are tasked with building the backend software for a local community library. The library needs a way to organize its books, allow members to borrow and return books, and easily view which titles are currently available.

---

## 🛠️ Requirements & Specifications

### 1. The `Book` Class

Create a class to represent individual books.

- **Attributes (`__init__`):**
  - `title` (string): The title of the book.
  - `author` (string): The author's full name.
  - `__is_checked_out` (boolean): A **private attribute** initialized to `False` by default (books are available when first added).
- **Methods:**
  - `borrow_book(self)`: Checks if the book is available. If `__is_checked_out` is `False`, set it to `True` and print a success message. If it is already checked out, print a message stating that it's currently unavailable.
  - `return_book(self)`: Sets `__is_checked_out` back to `False` and prints a confirmation message.
  - `is_available(self)`: Returns `True` if the book is available for borrowing, otherwise `False`.
  - `__str__(self)`: Returns a human-readable representation of the book (e.g., `"'1984' by George Orwell [Available]"`).

---

### 2. The `Library` Class

Create a class to manage a collection of `Book` objects.

- **Attributes (`__init__`):**
  - `name` (string): The name of the library.
  - `books` (list): Starts as an empty list `[]` to store `Book` instances.
- **Methods:**
  - `add_book(self, book)`: Adds a given `Book` object to the library's `books` list.
  - `show_all_books(self)`: Prints a list of every book in the library along with its current status.
  - `show_available_books(self)`: Loops through `books` and prints only those that are currently available.
  - `find_by_author(self, author_name)`: Searches for and prints all books written by the specified author.

---

## 🚀 Starter Code Template

Use the template below to structure your code:

```python
class Book:
    def __init__(self, title, author):
        self.title = title
        self.author = author
        # Encapsulation: Keep checkout status private
        self.__is_checked_out = False

    def borrow_book(self):
        # TODO: Implement borrow logic
        pass

    def return_book(self):
        # TODO: Implement return logic
        pass

    def is_available(self):
        # TODO: Return True if available, False if checked out
        pass

    def __str__(self):
        # TODO: Return formatted string representation
        pass


class Library:
    def __init__(self, name):
        self.name = name
        self.books = []

    def add_book(self, book):
        # TODO: Append book object to self.books
        pass

    def show_all_books(self):
        # TODO: Print all books in the library
        pass

    def show_available_books(self):
        # TODO: Print only available books
        pass

    def find_by_author(self, author_name):
        # TODO: Search and print books matching author_name
        pass
```
