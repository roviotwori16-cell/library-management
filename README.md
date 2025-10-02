````markdown
# Online Library Management System (OOP - C++)

## Project Overview
This project is part of **BSD 122 Object-Oriented Programming 1 (Assignment 1)**.  
The task is to design and implement an **Online Library Management System** in **C++** using **Object-Oriented Programming (OOP) principles**.

The system models three main entities:
- **Book** – represents each book in the library.
- **User** – represents library members who can borrow and return books.
- **Library** – manages books, users, borrowing, and returning.

The project demonstrates encapsulation, modular design, and test-driven development with both **positive and negative test scenarios**.

---

## Features
- Add and remove books (with ISBN-based uniqueness).
- Search for books by:
  - Title (partial match)
  - Author (partial match)
  - ISBN (exact match)
- Register new users.
- Borrow books (if available and not already borrowed by the same user).
- Return borrowed books.
- Prevent invalid actions such as:
  - Borrowing more copies than available.
  - Returning books not borrowed.
  - Removing books while copies are borrowed.
- Automated test suite included (`runTests()` function).
- Prints a final library summary after tests.

---

## How to Build & Run

### 1. Clone the Repository
```bash
git clone <your-repository-url>
cd OnlineLibrarySystem
````

### 2. Compile the Code

Use `g++` with C++17 or later:

```bash
g++ -std=c++17 -O2 LibraryManagement.cpp -o library
```

### 3. Run the Program

```bash
./library
```

This will:

* Execute automated test cases.
* Print test results.
* Show the final state of the library (books and users).

---

## Example Test Output

```
Running tests...
PASS: User registration
PASS: Adding books
PASS: Search by title
PASS: borrow book (succeed)
PASS: duplicate borrow prevented
PASS: borrow copies limit
PASS: return book
PASS: returning non-borrowed book prevented
PASS: cannot remove borrowed book
PASS: removed book after all returned
PASS: adding copies to existing ISBN

Final library state:
Library Summary:
Books (2):
  ID 2: "Effective Modern C++" by Scott Meyers ISBN:ISBN-002 [1/1 available]
  ID 3: "The Pragmatic Programmer" by Hunt & Thomas ISBN:ISBN-003 [5/5 available]
Users (2):
  ID 1: Alice (borrowed 0)
  ID 2: Bob (borrowed 0)
Tests completed.
```

---

## Files in This Project

* `LibraryManagement.cpp` → Main program file with all classes and tests.
* `README.md` → Project description, build instructions, and usage.

---

## Possible Extensions

* Add file persistence (save/load library data).
* Add interactive CLI for real user input.
* Track due dates, fines, and user roles (Admin vs Member).
* Implement a GUI frontend.

---

## Author

**[Your Name Here]**
BSD 122 – Object-Oriented Programming 1 (Assignment 1)

```
```
