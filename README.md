# Ei-Study Coding Assignment

This repository contains the tasks completed as part of the *Ei-Study Company Internship Assignment*. The assignment consisted of two main exercises:

* *Exercise 1* – Implementing six software design patterns in *TypeScript*
* *Exercise 2* – Building a Virtual Classroom Manager mini-project in *TypeScript*

---

## 📂 Repository Structure

```
Ei-Study-Coding-Assignment/
│
├── Exercise-1/              # Implementation of six design patterns (TypeScript)
│   ├── Observer Pattern
│   ├── Strategy Pattern
│   ├── Singleton Pattern
│   ├── Abstract Factory Pattern
│   ├── Adapter Pattern
│   └── Decorator Pattern
│
└── Exercise-2/              # Virtual Classroom Manager (TypeScript)
    ├── src/
    │   ├── controllers/         # Handle user input/output
    │   ├── models/             # Domain entities
    │   ├── services/           # Business logic
    │   ├── repositories/       # Data access layer
    │   ├── interfaces/         # Type definitions
    │   ├── utils/              # Utility functions
    │   ├── main.ts             # Application entry point
    │   └── VirtualClassroomManager.ts  # Main application class
    ├── package.json
    ├── tsconfig.json
    └── README.md
```

---

## 🚀 Exercise 1 – Design Patterns (TypeScript)

As part of Exercise-1, six different design patterns were implemented in *TypeScript* to demonstrate their real-world applications.

### ✅ Implemented Patterns

1. *Observer Pattern* – Notifies dependent objects when the state changes.
2. *Strategy Pattern* – Dynamically selects and applies an algorithm at runtime.
3. *Singleton Pattern* – Ensures only a single instance of a class exists.
4. *Abstract Factory Pattern* – Creates related objects without specifying their concrete classes.
5. *Adapter Pattern* – Allows incompatible interfaces to work together.
6. *Decorator Pattern* – Adds new functionality to objects without changing their structure.

### ▶ How to Run

1. Make sure *Node.js* is installed on your system.
2. Navigate to the *Exercise-1* folder.
3. Install dependencies (if required):

```bash
npm install
```

4. Run the project:

```bash
npm run dev
```

> 💡 This command will compile and execute all TypeScript files automatically.

---

## 🌍 Exercise 2 – Virtual Classroom Manager (TypeScript)

### Project: *Virtual Classroom Manager*

The *Virtual Classroom Manager* is a *TypeScript-based terminal application* that models the backend for an EdTech platform. It provides a command-line interface for:

* Creating and managing virtual classrooms
* Enrolling students in classrooms
* Scheduling assignments for classes
* Submitting assignments by students
* Demonstrating *SOLID principles* and design patterns
* Implementing *repository pattern*, *service layer*, and error handling

### ▶ How to Run (TypeScript)

1. Navigate to the *Exercise-2* folder.
2. Install dependencies:

```bash
npm install
```

3. Run the project:

```bash
npm run dev
```

---

## 🖥 Sample Output

### Exercise 1 – Design Patterns (TypeScript)

*Observer Pattern*
```
[Satellite Status Updated] - Notifying all observers...
Observer1: Received update: Satellite orientation changed
Observer2: Received update: Satellite orientation changed
```

*Strategy Pattern*
```
Selected Travel Strategy: Fastest Route
Traveling from Point A to Point B using Fastest Route
```

(Add similar outputs for Singleton, Abstract Factory, Adapter, and Decorator patterns)

### Exercise 2 – Virtual Classroom Manager (TypeScript)

*Virtual Classroom Manager*
```
> add_classroom Math 101
Classroom Math 101 has been created.

> add_student S12345 Math 101
Student S12345 has been enrolled in Math 101.

> schedule_assignment Math 101 Complete exercises 1-10 from page 25
Assignment for Math 101 has been scheduled.

> submit_assignment S12345 Math 101 Complete exercises 1-10 from page 25
Assignment submitted by Student S12345 in Math 101.

> list_classrooms
Available Classrooms:
- Math 101 (Students: 1, Assignments: 1)

> list_students
Available Students:
- S12345 (Enrolled in: Math 101)

> list_assignments
Available Assignments:
- assignment_1: Complete exercises 1-10 from page 25 (Class: Math 101, Submissions: 1)
```

---

## 🛠 Technologies Used

* *Languages*: TypeScript
* *Concepts*: OOP, Software Design Patterns, SOLID Principles, System Simulation
* *Tools*: Node.js, npm, TypeScript Compiler, VS Code

---

## 📖 Learning Outcomes

* Implemented six major *software design patterns* using *TypeScript*.
* Learned the role of design patterns in building reusable and maintainable code.
* Applied OOP concepts and SOLID principles to create a *Virtual Classroom Manager* in TypeScript.
* Improved modular design, problem-solving, and full-stack TypeScript development skills.
* Gained experience with repository pattern, service layer architecture, and error handling.
