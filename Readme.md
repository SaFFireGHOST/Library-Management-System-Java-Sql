
# Library Management System

This project is a console-based Library Management System implemented in Java, using a MySQL database for data storage and management. The system allows librarians and students to perform various actions such as adding, deleting, borrowing, and returning books, as well as viewing book and student records.

---

## Features

### For Librarians:
- View all books or only available books.
- Add new books to the database.
- Delete books from the library.
- Issue books to students.
- Accept returned books.
- View all students.
- View the list of books borrowed by a student.

### For Students:
- View the list of all available books.
- View the list of books they have borrowed.

---

## Prerequisites

1. **MySQL** installed and configured on your system.
2. **Java Development Kit (JDK)** installed (version 8 or higher recommended).

---

## Setup Instructions

### Database Setup

1. Open the MySQL terminal:
   ```bash
   mysql -u <your_username> -p
   ```
2. Execute the following SQL scripts in the provided order:
   ```sql
   SOURCE Library_create.sql;
   SOURCE Library_alter.sql;
   SOURCE Library_data.sql;
   ```

### Application Setup

1. Navigate to the `src` directory where the project files are located:
   ```bash
   cd src
   ```
2. Set the `CLASSPATH` environment variable to include the included MySQL Connector/J library:
   ```bash
   export CLASSPATH='/path/to/src/mysql-connector-j-8.3.0.jar:.'
   ```
   Replace `/path/to/` with the actual path to the `src` directory where the `.jar` file is located.

3. Compile the Java application:
   ```bash
   javac imt2022570_librarydb.java
   ```
4. Run the application:
   ```bash
   java imt2022570_librarydb
   ```

---

## Configuration

- Update the `DB_URL`, `USER`, and `PASS` variables in `imt2022570_librarydb.java` with your MySQL credentials:
  ```java
  static final String DB_URL = "jdbc:mysql://localhost:3306/librarydb";
  static final String USER = "<your_mysql_username>";
  static final String PASS = "<your_mysql_password>";
  ```

---

## Project Structure

- `sql/`: Contains SQL scripts to create, alter, and populate the database.
- `src/`: Contains the Java source code files and dependencies (e.g., `mysql-connector-j-8.3.0.jar`).

---

## Dependencies

- MySQL Connector/J: The required `.jar` file (`mysql-connector-j-8.3.0.jar`) is already included in the `src` directory.

---
