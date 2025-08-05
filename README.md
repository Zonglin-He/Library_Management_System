# Library Management System

A simple Java desktop application for managing books: add, view, delete, borrow, return, and track borrowing records.

---

## Features

- **Add Book**: Insert new books (title + author).  
- **View All Books**: Display a table of all books with their status.  
- **Delete Book**: Remove a book record by its ID.  
- **Borrow Book**: Mark a book as borrowed and record the transaction.  
- **Return Book**: Mark a book as returned and update the record.  
- **Check Borrowing Records**: View history of all borrow/return events.

---

## Tech Stack

- **Java 17**  
- **Swing** for GUI (`JFrame`, `JDialog`, `JTable`, `JOptionPane`)  
- **MySQL** (via JDBC)  
- **Maven** for build & dependency management  
- **JUnit 5** for automated unit tests  

---

## Prerequisites

- JDK 17  
- Maven 3.x  
- MySQL Server (or any JDBC-compatible database)

---

## Installation & Setup

1. **Clone the repository**  
   ```bash
   git clone https://github.com/yourusername/library-management-system.git
   cd library-management-system

## Project Structure

library-management-system/
├── pom.xml
├── src
│ ├── main
│ │ ├── java
│ │ │ ├── app
│ │ │ │ └── Main.java
│ │ │ ├── dao
│ │ │ │ ├── BookDAO.java
│ │ │ │ └── BorrowDAO.java
│ │ │ ├── model
│ │ │ │ ├── Book.java
│ │ │ │ └── BorrowRecord.java
│ │ │ ├── gui
│ │ │ │ ├── AddBookDialog.java
│ │ │ │ ├── ViewBooksDialog.java
│ │ │ │ ├── DeleteBookDialog.java
│ │ │ │ ├── BorrowBookDialog.java
│ │ │ │ ├── ReturnBookDialog.java
│ │ │ │ └── BorrowRecordDialog.java
│ │ │ └── util
│ │ │ └── DBUtil.java
│ │ └── resources
│ │ └── db.properties
│ └── test
│ ├── java
│ │ ├── dao
│ │ │ ├── BookDAOTest.java
│ │ │ └── BorrowDAOTest.java
│ └── resources
│ └── test-data.sql
└── README.md


---

## Architecture Overview

We follow a **four-layer** design:

1. **Model Layer**  
   Plain Java objects (`Book`, `BorrowRecord`) that map to database tables.

2. **DAO Layer**  
   - `BookDAO`: handles `addBook()`, `getAllBooks()`, `deleteBookById()`.  
   - `BorrowDAO`: handles `borrowBook()`, `returnBook()`, `showAllBorrowRecords()`.

3. **GUI Layer**  
   Swing dialogs (`JDialog`) for each feature and a main window (`LibraryGUI`).

4. **Utility Layer**  
   `DBUtil.getConnection()`: centralizes JDBC configuration and resource management.

---

## Running Tests

Execute all JUnit tests against the `test_library` schema:

```bash
mvn test

Build an executable JAR:mvn package
The resulting JAR is located at:target/library-system-1.0-SNAPSHOT.jar

Contributing
Fork the repository

Create your feature branch (git checkout -b feature/YourFeature)

Commit your changes (git commit -m 'Add new feature')

Push to the branch (git push origin feature/YourFeature)

Open a Pull Request

License
This project is licensed under the MIT License. See the LICENSE file for details.
