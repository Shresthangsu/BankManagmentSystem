Bank Management System

Overview

The Bank Management System is a desktop-based Java application that simulates the functionality of an Automated Teller Machine (ATM) and a banking system. Users can sign up for accounts, log in, and manage their banking details securely. The project also integrates a MySQL database for backend data management.

Features

1. Login Page

Sign In: Users can log in using their card number and PIN.

Sign Up: New users can create accounts by providing personal details.

Clear: Reset the input fields for card number and PIN.

2. Signup Page

Personal Details Form: Users are required to fill out personal details such as name, father's name, date of birth, gender, email, marital status, address, city, state, and pincode.

Validation: Ensures all fields are filled before proceeding.

Database Integration: Data is stored in a MySQL database upon submission.

3. Backend Integration

MySQL Database: Stores user details.

JDBC Connectivity: Provides seamless communication between the Java application and MySQL database.

Database Schema

Database Name: bankmanagementsystem

Table: signup

Column Name

Data Type

Description

formno

VARCHAR(20)

Unique application form number

name

VARCHAR(30)

Name of the user

father_name

VARCHAR(30)

Name of the user's father

dob

VARCHAR(20)

Date of birth of the user

gender

VARCHAR(20)

Gender of the user

email

VARCHAR(30)

Email address of the user

marital_status

VARCHAR(20)

Marital status of the user

address

VARCHAR(40)

Address of the user

city

VARCHAR(25)

City or village of the user

pincode

VARCHAR(20)

Pincode of the user's address

state

VARCHAR(25)

State of the user's address


Setup MySQL Database:

Import the bankmanagementsystem schema using the SQL script:

DROP DATABASE IF EXISTS bankmanagementsystem;
CREATE DATABASE bankmanagementsystem;
USE bankmanagementsystem;

CREATE TABLE signup (
    formno VARCHAR(20) PRIMARY KEY,
    name VARCHAR(30),
    father_name VARCHAR(30),
    dob VARCHAR(20),
    gender VARCHAR(20),
    email VARCHAR(30),
    marital_status VARCHAR(20),
    address VARCHAR(40),
    city VARCHAR(25),
    pincode VARCHAR(20),
    state VARCHAR(25)
);

SELECT * FROM signup;

Configure Database Connection:

Update the database credentials in the con class:

c = DriverManager.getConnection("jdbc:mysql:///bankmanagementsystem", "root", "yourpassword");

Run the Application:

Compile and run the Java application using an IDE (e.g., IntelliJ IDEA, Eclipse) or the command line.

Technologies Used

Programming Language: Java (Swing for GUI development)

Database: MySQL

Build Tool: None (standard Java compilation)

External Libraries: toedter.calendar for date selection

Usage

Launch the application.

Sign up for an account by filling out the personal details form.

Log in using your card number and PIN.

Proceed to additional banking functionalities (to be implemented in future updates).

Future Enhancements

Add more banking features such as account management, fund transfers, and transaction history.

Improve UI design for better user experience.

Enhance security by encrypting sensitive data such as PINs.

Contributing

Contributions are welcome! If you'd like to contribute, please follow these steps:

Fork the repository.

Create a new branch (git checkout -b feature/YourFeature).

Commit your changes (git commit -m 'Add some feature').

Push to the branch (git push origin feature/YourFeature).

Open a Pull Request.

