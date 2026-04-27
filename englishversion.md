# Object-Oriented Programming (OOP) Exercises Repository  
### Second Semester of 2025

This repository contains exercises developed during the **Object-Oriented Programming (OOP)** course in the second semester of 2025.  
Each activity explores fundamental OOP concepts, including encapsulation, inheritance, polymorphism, business rules, testing, and database integration.

---

# 📂 Exercise Summary
1. [Exercise 1 — Student Class](#exercise-1--student-class)
2. [Exercise 2 — Mini Library System](#exercise-2--mini-library-system)
3. [Exercise 3 — Library Part 2 (Extension)](#exercise-3--library-part-2-extension)
4. [Exercise 4 — OOP Practices in TypeScript](#exercise-4--oop-practices-in-typescript)
5. [Exercise 5 — Task System with OOP + Prisma + SQLite](#exercise-5--task-system-with-oop--prisma--sqlite)
6. [Group Project — OOP (DB + Web)](#group-project--oop-db--web)

---

# Exercise 1 — Student Class

### Objective
Implement a class that represents a student, handling grades and calculating the average.

### Specification
- `name: string`
- `grades: number[]`
- `addGrade(grade: number)`
- `average(): number`

### Activities
- Create an array of students  
- Add grades  
- Print averages  
- Compare with the implementation in C (struct + functions)

---

# Exercise 2 — Mini Library System

### Implemented Classes
- **Book** → title, author, publisher, genre, year  
- **Copy** → id, book, status  
- **User** → id, name  
- **Loan** → user, copy, dates, status  
- **Library** → loan/return management  

---

## System Rules
- A copy can be: **Available**, **Loaned**, or **Damaged**  
- A user can have **up to 3 borrowed books**  
- Loan duration: **14 days**  
- It is not possible to loan an unavailable copy  
- Upon return:
  - the copy becomes **Available**
  - the loan is marked as **Completed**

---

## Implemented Methods
- `Library.loan(user, copy, startDate)`
- `Library.return(user, copy, returnDate)`
- `Loan.lateDays(today)` → returns `0` if within the deadline

---

## Test Cases (Manual)
- Loan and return within the deadline  
- Attempt to loan an already borrowed copy → **error**  
- User attempting to borrow a 4th book → **error**  
- Return after 20 days → delay = **6 days**

---

# Exercise 3 — Library Part 2 (Extension)

### New Rules
- A user with overdue returns is **blocked for X days**, where X = delay days  
- A copy can be returned as **Damaged**, becoming permanently unavailable  
- The library maintains:
  - penalty history  
  - damaged copies history  

---

### New Methods
- `Library.isBlocked(user, currentDate)`
- `Library.registerDamagedReturn(user, copy, returnDate)`

---

### Automated Test Cases
- Return with 5 days delay → 5-day block  
- Blocked user attempts to borrow → should throw error  
- Return damaged copy → state updated and future loans blocked  

---

# Exercise 4 — OOP Practices in TypeScript

### 1) Transportation System  
All objects implement `move()`, but:
- some **fly**  
- some **navigate**  
- some **drive**  

Demonstrates **polymorphism** across different classes.

---

### 2) Document Processing Flow  
Mandatory execution order for all documents:  
```
open → process → save → close
```


Modeled using the **Template Method** pattern.

---

### 3) Payment Service with Multiple Gateways  
Implement a service that uses different gateways:
- Stripe  
- PayPal  
- Pix  

Demonstrates the **Strategy** pattern.

---

# Exercise 5 — Task System with OOP + Prisma + SQLite

### Objective
Create a simple task management system (Todo List) with:
- Classes (`User`, `Task`)
- Real database persistence
- Prisma ORM

---

## Technical Requirements
- **TypeScript**
- **Prisma 5**
- **SQLite**

---

# Group Project — OOP (DB + Web)

During the course, we also developed a group project combining:
- Object-Oriented Programming  
- Database (relational model)  
- Web layer for interaction  
- Real-world business rules  

## Project Idea

Build a complete system applying:
- Classes and relationships  
- Design patterns  
- Full CRUD with database  
- Functional web interface  

## Project Repository
👉 Access the group project here: [Project](https://github.com/KauanQuinzote/Conserta-Felix.git)

---

# 👨‍💻 Author

Ana Luisa Rodrigues  
Object-Oriented Programming Course — 2025.2
