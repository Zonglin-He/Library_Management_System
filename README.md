# Library Management System

A simple desktop Library Management System written in Java using Swing for the GUI and MySQL for persistence.  
Implements a four-layer architecture (Model → DAO → GUI → Util) and includes unit tests with JUnit 5.

---

## 📖 Table of Contents

1. [Features](#-features)  
2. [Tech Stack](#-tech-stack)  
3. [Prerequisites](#-prerequisites)  
4. [Installation & Setup](#-installation--setup)  
5. [Usage](#-usage)  
6. [Project Structure](#-project-structure)  
7. [Architecture Overview](#-architecture-overview)  
8. [Running Tests](#-running-tests)  
9. [Packaging](#-packaging)  
10. [Contributing](#-contributing)  
11. [License](#-license)

---

## 🌟 Features

- **Add Book**: Insert new books with title & author.  
- **View All Books**: Display list of books (ID, title, author, borrowed‐status).  
- **Delete Book**: Remove a book record by ID.  
- **Borrow/Return**: Mark books as borrowed/returned, track borrow records.  
- **Check Records**: View full history of borrow/return events.

---

## 🛠 Tech Stack

- **Language**: Java 17  
- **GUI**: Swing (`JFrame`, `JDialog`, `JTable`, `JOptionPane`)  
- **Database**: MySQL  
- **Build Tool**: Maven  
- **Testing**: JUnit 5  

---

## ⚙️ Prerequisites

- Java 17 JDK  
- Maven 3.x  
- MySQL server (or any JDBC‐compatible database)  

---

## 📥 Installation & Setup

1. **Clone the repo**  
   ```bash
   git clone https://github.com/yourusername/library-management-system.git
   cd library-management-system
.
├── pom.xml
├── src
│   ├── main
│   │   ├── java
│   │   │   ├── app
│   │   │   │   └── Main.java
│   │   │   ├── dao
│   │   │   │   ├── BookDAO.java
│   │   │   │   └── BorrowDAO.java
│   │   │   ├── model
│   │   │   │   ├── Book.java
│   │   │   │   └── BorrowRecord.java
│   │   │   ├── gui
│   │   │   │   ├── AddBookDialog.java
│   │   │   │   ├── ViewBooksDialog.java
│   │   │   │   └── … 
│   │   │   └── util
│   │   │       └── DBUtil.java
│   │   └── resources
│   │       └── db.properties
│   └── test
│       ├── java
│       │   ├── dao
│       │   │   └── BookDAOTest.java
│       │   └── dao
│       │       └── BorrowDAOTest.java
│       └── resources
│           └── test-data.sql
└── README.md
