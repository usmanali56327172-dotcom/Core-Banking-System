# Core Banking System (CBS)
### Simplified Database Project with SQL Transaction Control (TCL)

A simplified **Core Banking System (CBS)** developed as a final semester database project. This project demonstrates how customer records, account management, and banking transactions are handled using a centralized relational database with strong emphasis on **Transaction Control Language (TCL)** commands such as `COMMIT`, `ROLLBACK`, and `SAVEPOINT`.

---

## Project Objective

The objective of this project is to simulate the core functionality of a banking system while ensuring:

- Data consistency
- Transaction integrity
- Atomic operations
- Audit logging
- Secure handling of banking activities

---

## Modules Implemented

### 1. Customer Management
Manage customer profiles and personal information.

**Features**
- Add new customer
- Update customer details
- View customer records
- Delete customer

**Attributes**
- CustomerID
- Name
- CNIC
- Contact

---

### 2. Account Management
Manage bank accounts linked to customers.

**Features**
- Create account
- View account details
- Update account status
- Check balance

**Attributes**
- AccountNo
- CustomerID
- AccountType
- Balance
- Status

---

### 3. Transaction Management
Perform financial transactions.

**Features**
- Deposit
- Withdrawal
- Transfer funds

**Attributes**
- TransactionID
- FromAccount
- ToAccount
- Amount
- Type
- DateTime

---

### 4. Audit and Security Control
Maintain logs of all critical database operations.

**Features**
- Record COMMIT and ROLLBACK actions
- Track user activities
- Maintain timestamps

**Attributes**
- LogID
- Operation
- TableAffected
- Username
- DateTime

---

## Database Schema

### Entities
- Customer
- Account
- Transaction
- AuditLog

---

## Entity Relationship Overview

```text
Customer 1 ──────< Account
Account 1 ──────< Transaction
AuditLog stores all critical operations
