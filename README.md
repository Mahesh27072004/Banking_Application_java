# 🏦 Java Banking Backend System (JDBC-Connected)

A modular Java-based banking backend application that uses **JDBC** for database connectivity and provides a command-line interface to perform various banking operations.

---

## 🚀 Features

- User registration and account creation
- Secure user authentication
- Deposit and withdraw funds
- Check account balances
- Display account details
- Database integration using JDBC

---

## 🧱 Project Structure

- `User.java`  
  Represents a bank customer. Stores user-related information like full_name, ID, credentials, etc.

- `Accounts.java`  
  Models a bank account and includes deposit, withdrawal, and display logic.

- `AccountManager.java`  
  Contains business logic to manage accounts — handles actions like finding, updating, and displaying user accounts.

- `BankingApp.java`  
  **Main class**. Establishes JDBC connection to the database and runs the application's main execution logic via console interaction.

---

## 🖥️ Tech Stack

- Java SE
- JDBC API
- MySQL / Any RDBMS
- Command-Line Interface (CLI)

---

## 🛠️ Setup Instructions

1. **Clone the repository**:
   git clone https://github.com/yourusername/java-banking-backend.git
   cd java-banking-backend
   
2. Configure the database:
Create a MySQL database (e.g., bankdb)
Set up tables (users, accounts, etc.)
Update JDBC URL, username, and password in BankingApp.java

3. Compile the code:
javac *.java

4. Run the application:
java BankingApp

🗃️ Sample Database Table (MySQL)
1. create database banking_system;

2. CREATE TABLE user (
  id INT PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(100),
  email VARCHAR(100),
  password VARCHAR(100)
);

3. CREATE TABLE accounts (
  acc_id INT PRIMARY KEY AUTO_INCREMENT,
  user_id INT,
  balance DOUBLE,
  FOREIGN KEY (user_id) REFERENCES users(id)
);

📌 Notes
All data is stored persistently using JDBC and a relational database.

The app runs via terminal and provides a menu-based interface for operations.

Ensure your JDBC driver is added to the classpath when compiling/running.

📝 License
This project is licensed under the MIT License.

🙌 Contributing
Pull requests and suggestions are welcome! For major changes, please open an issue first to discuss.
