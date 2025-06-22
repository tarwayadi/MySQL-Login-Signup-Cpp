# C++ MySQL User Authentication System

This project demonstrates a basic user authentication system (Signup and Login) written in C++ and connected to a MySQL database using the MySQL C API. It also includes a simple password encryption mechanism for educational purposes.

---

## 🌟 Features

- **User Registration (Signup):** New users can register using a unique ID and password.
- **Password Encryption:** Uses a basic XOR cipher to encrypt passwords before storing them in the database.
- **User Login:** Verifies login credentials by comparing the entered data with stored encrypted data.
- **MySQL Database Integration:** Uses the MySQL C Connector to communicate with a MySQL Server.
- **Command-Line Interface:** Console-based interactive menu for Signup and Login operations.

---

## ⚠️ Security Warning

> The encryption method used (XOR cipher) is highly insecure and only suitable for demonstration purposes. For real-world applications, use strong hashing algorithms like **bcrypt**, **scrypt**, or **Argon2** along with salting.

---

## 🚀 Setup Instructions

### 1. Prerequisites

- MySQL Server 8.0+ (Running)
- MySQL Workbench or MySQL Shell
- Dev-C++ IDE
- MySQL Connector/C (C API)

### 2. MySQL Database Setup

Run the  SQL code written in sql_code in MySQL Workbench or Shell:


 ### 3: Configure Dev-C++ Project

- Open Dev-C++.
- Go to Project > Project Options (or press Alt + P).
- Select the "Directories" tab.

3.1 Configure Include Directories (Header Files)
- Choose "C Include Directories".
- Click the "New" button.
- Browse to: C:\MySQL_C_Connector\mysql-connector-c-8.x.x-winx64\include

3.2 Configure Library Directories (Library Files)
- Choose "Library Directories".
- Click the "New" button.
- Browse to: C:\MySQL_C_Connector\mysql-connector-c-8.x.x-winx64\lib

3.3 Configure Linker Settings
- Go to the "Parameters" tab.
- Under "Linker", add: -lmysql or -lmysqlclient
- Click OK to save changes.

 ### 4: Place the Runtime DLL

- Locate libmysql.dll in either the 'lib' or 'bin' folder inside your extracted MySQL Connector/C directory.
- Example: C:\MySQL_C_Connector\mysql-connector-c-8.x.x-winx64\lib\libmysql.dll
- Copy this file.
- Paste it in your Dev-C++ project folder (where your .exe will be generated).

### 5: Update MySQL Credentials in Code

- Open your main.cpp file.
- Find the line:
  const char* PW = "your password";
- Replace with your actual MySQL root password.
  For example:
  const char* PW = "MyRootPass123";

### 7: Compile and Run

- In Dev-C++, go to Execute > Compile & Run (or press F11).
- If everything is set up correctly, the program will compile and display a console menu for login/signup.


