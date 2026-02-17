📚 Library Management System (Java JSP/Servlet)

A simple Library Management System built using Java, JSP, Servlets, and MySQL. This web-based application helps manage books, customers, staff, and book issuing/return operations in a library.

🚀 Features

🔐 User Login & Logout

📖 Book Management

Add book

Update book

Delete book

Search & View books

👥 Customer Management

Add customer

View customers

🧑‍💼 Staff Management

Add staff

View staff

Delete staff

🔄 Issue & Return Books

📊 Manager Dashboard

🛠️ Tech Stack

Backend: Java Servlets

Frontend: JSP, HTML, CSS

Database: MySQL

Server: Apache Tomcat

JDBC Driver: MySQL Connector/J

IDE (recommended): Eclipse / IntelliJ IDEA

📂 Project Structure
LibraryManagement/
│
├── src/main/java/com/library/
│   ├── db/
│   │   └── DBConnection.java
│   └── servlet/
│       ├── BookServlet.java
│       ├── CustomerServlet.java
│       ├── IssueServlet.java
│       ├── LoginServlet.java
│       └── StaffServlet.java
│
├── src/main/webapp/
│   ├── *.jsp (UI pages)
│   ├── WEB-INF/
│   │   ├── web.xml
│   │   └── lib/
│
└── build/

⚙️ Setup Instructions
1️⃣ Clone / Import Project

Download or extract the project

Import into Eclipse/IntelliJ as a Dynamic Web Project

2️⃣ Configure Database

Create a MySQL database:

CREATE DATABASE library;


Create required tables (example):

CREATE TABLE books (
    id INT PRIMARY KEY AUTO_INCREMENT,
    title VARCHAR(100),
    author VARCHAR(100),
    price DOUBLE,
    quantity INT
);

CREATE TABLE customers (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    email VARCHAR(100)
);

CREATE TABLE staff (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    role VARCHAR(50)
);

3️⃣ Update DB Credentials

Edit:

DBConnection.java

return DriverManager.getConnection(
    "jdbc:mysql://localhost:3306/library",
    "root",
    "YOUR_PASSWORD"
);


Replace:

YOUR_PASSWORD


with your MySQL password.

4️⃣ Add Server

Configure Apache Tomcat in your IDE

Deploy the project to Tomcat

5️⃣ Run Application

Open browser:

http://localhost:8080/LibraryManagement/login.jsp

🔑 Default Usage Flow

Login

Go to Manager Dashboard

Add Books/Customers/Staff

Issue & Return books

View records

✅ Requirements

Java JDK 8+

MySQL Server

Apache Tomcat 9+

MySQL Connector/J


👨‍💻 Author

Developed as a Java Web Application project for learning and academic purposes.
