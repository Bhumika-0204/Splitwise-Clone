<div align="center">

# 💸 Splitwise Clone  
### C++ Low-Level System Design | Expense Sharing Engine  

![C++](https://img.shields.io/badge/Language-C++-blue?style=for-the-badge&logo=cplusplus)
![OOP](https://img.shields.io/badge/Design-OOP-green?style=for-the-badge)
![LLD](https://img.shields.io/badge/System%20Design-LLD-orange?style=for-the-badge)

*A scalable expense-sharing system built with strong focus on business logic, object-oriented design, and low-level system architecture.*

</div>

---

## ⚡ Overview

This project is a console-based Splitwise Clone built in C++, designed to simulate real-world expense-sharing systems.

It focuses on:
- Core financial business logic  
- Low-Level System Design (LLD)  
- Clean and modular architecture  

---

## 🚀 Features

### 👥 User Management
- Add and manage multiple users  

### 💰 Expense Splitting
- Equal split  
- Exact split  
- Percentage-based split  

### 📊 Balance Tracking
- Tracks who owes whom  
- Maintains individual balance sheets  

### 🔄 Debt Simplification
- Minimizes number of transactions  

### 📁 Transaction Handling
- Efficient expense recording and updates  

---

## 🧠 System Design (LLD)

### 🔹 Core Components
- User → Represents a participant  
- Expense → Handles expense details  
- Balance → Maintains debt relationships  
- SpendManager → Core business logic controller  

### 🔹 Design Principles
- Encapsulation  
- Abstraction  
- Modularity  
- Separation of Concerns  

---

## 🏗️ System Architecture

```mermaid
classDiagram
    class User {
        +string userId
        +string name
    }

    class Expense {
        +string expenseId
        +double amount
        +User paidBy
    }

    class Balance {
        +map balances
        +updateBalance()
    }

    class SpendManager {
        +addExpense()
        +splitExpense()
    }

    User --> Expense
    Expense --> Balance
    SpendManager --> Expense
    SpendManager --> Balance
```

---

## 🔄 Expense Flow

```mermaid
sequenceDiagram
    participant U as User
    participant SM as SpendManager
    participant E as Expense
    participant B as Balance

    U->>SM: Add Expense
    SM->>E: Create Expense
    SM->>B: Update Balances
    B-->>U: Show Updated Balances
```

---

## 📂 Project Structure

```
SplitWise/
│
├── models/
│   ├── Expense.cpp
│   ├── Expense.h
│   ├── User.cpp
│   ├── User.h
│
├── services/
│   ├── Balance.cpp
│   ├── Balance.h
│   ├── SpendManager.cpp
│   ├── SpendManager.h
│
├── main.cpp
```

---

## 💻 Tech Stack

- Language: C++  
- Paradigm: Object-Oriented Programming (OOP)  
- Focus: Low-Level System Design + Business Logic  

---

## 🚀 Quickstart

```bash
# Clone the repository
git clone https://github.com/your-username/splitwise-clone.git

# Navigate into project
cd splitwise-clone

# Compile
g++ main.cpp models/*.cpp services/*.cpp -o splitwise

# Run
./splitwise
```

---

## 🧪 Example

```
User1 paid ₹1000 for 4 users

Each owes: ₹250

Balances:
User2 owes User1 ₹250
User3 owes User1 ₹250
User4 owes User1 ₹250
```

---

## 🎯 Key Highlights

- Built using Low-Level System Design principles  
- Clean separation of models and services layers  
- Strong OOP implementation in C++  
- Simulates real-world financial transaction systems  
- Scalable and maintainable architecture  

---

## 🏁 Future Enhancements

- Database integration (MySQL / MongoDB)  
- REST API backend  
- Web-based UI  
- Authentication system  
- Group-based expense tracking  
- Advanced debt minimization algorithms  

---

## 📄 License

This project is licensed under the MIT License.
