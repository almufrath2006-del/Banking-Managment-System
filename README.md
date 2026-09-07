# Banking Management System

## Overview
A console-based Banking Management System developed using Core Java 
with JDBC and MySQL database integration. This is an advanced version 
of the banking system where customer details including name, phone 
number, and email are stored along with account data. All records are 
persistently managed in MySQL and loaded automatically on every startup 
ensuring zero data loss between sessions.

## Features
- Dual account types — Savings and Current with different business rules
- Secure 4-digit PIN-based authentication for all transactions
- Customer registration with name, phone number, and email
- View account details (name, PIN, phone, email) with PIN verification 
- PIN Change features
- Deposit with real-time MySQL database update
- Withdrawal with minimum balance validation
  (Savings: ₹500 minimum, Current: ₹1000 minimum)
- Fund transfer between accounts with real-time DB sync
- Loan request with salary and balance eligibility check
- Savings account loan capped at ₹5,00,000
- Multiple loan tracking and repayment management
- Complete transaction history stored in database
- Account deletion with full data cleanup from all tables
- All account data loaded from MySQL on startup

## Technologies Used
- Core Java
- JDBC — Java Database Connectivity
- MySQL Database
- OOP Concepts — Abstract class, Inheritance, Method Overriding
- Java Collections — HashMap, ArrayList

## OOP Concepts Used
- Abstract class (Bank) with abstract methods
- Inheritance — saveBank and currentBank extend Bank
- Method Overriding — withdrawal and loan logic per account type
- Encapsulation — balance and pin managed via access modifiers

## Database Tables
- saving — stores pin, name, phone, email, balance
- current — stores pin, name, phone, email, balance
- loan — stores pin and loan amount
- transaction_details — logs every transaction

## How to Run
1. Clone the repository
2. Create MySQL database named 'bank'
3. Create saving, current, loan, transaction_details tables
4. Add MySQL connector JAR to lib folder
5. Update DB password in code if needed
6. Compile and run Main.java