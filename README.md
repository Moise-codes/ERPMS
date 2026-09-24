# ERPM — Enterprise Resource & Project Management System

ERPM is a large-scale Java learning project designed to simulate the development of a real-world Enterprise Resource & Project Management System.

The project is being developed progressively from a simple Java application into a structured, database-backed enterprise application.

The primary goal is not only to build the system, but to use the system as a practical environment for learning Java from fundamentals through advanced Java concepts and professional software development practices.

---

## Project Goals

This project has two main goals:

### 1. Build a complete enterprise-style application

ERPM will eventually provide functionality for managing:

* Employees
* Departments
* Projects
* Tasks
* Customers
* Invoices
* Authentication and roles
* Reports
* Application data
* Database persistence

### 2. Learn Java through practical implementation

Java concepts will be introduced when they become useful to the application.

The project will cover Java fundamentals, object-oriented programming, collections, generics, exception handling, file handling, functional programming, streams, concurrency, JDBC, PostgreSQL, testing, and other important Java concepts.

The goal is to understand **why and when** a Java feature is used rather than simply memorizing its syntax.

---

# Technology Stack

The project will initially use:

* **Java 25**
* **Maven**
* **IntelliJ IDEA**
* **Git**
* **GitHub**

Later stages will introduce:

* PostgreSQL
* JDBC
* JUnit
* Additional Maven dependencies where required

---

# Development Philosophy

ERPM is being developed incrementally.

We will not create the entire application at once.

Each feature will be introduced only when it is needed.

The development process follows:

```text
Learn
  ↓
Understand
  ↓
Practice
  ↓
Implement
  ↓
Test
  ↓
Commit
  ↓
Continue
```

Java concepts will therefore be learned through actual application development.

For example, inheritance will not be introduced simply because inheritance is part of Java.

Instead, when the employee domain requires different employee types such as `Developer` and `Manager`, inheritance will provide a meaningful reason to learn and use the concept.

---

# Architecture

The project will follow a feature-oriented structure.

Instead of placing every model, service, and repository into global folders, related components will stay together inside their respective business domains.

For example:

```text
employee/
├── Employee.java
├── EmployeeRepository.java
├── EmployeeService.java
└── EmployeeController.java
```

This approach keeps each business feature organized and allows the application to grow naturally.

The application will gradually evolve toward:

```text
Main
 ↓
Controller
 ↓
Service
 ↓
Repository
 ↓
Data Source
```

Initially, repositories may use in-memory Java collections.

Later, the persistence layer will be replaced or extended with PostgreSQL through JDBC.

---

# Planned Project Structure

The final structure is expected to evolve toward something similar to:

```text
erp-management-system/
│
├── .gitignore
├── README.md
├── pom.xml
│
├── src/
│   │
│   ├── main/
│   │   └── java/
│   │       └── com/
│   │           └── moise/
│   │               └── erp/
│   │                   │
│   │                   ├── Main.java
│   │                   │
│   │                   ├── employee/
│   │                   │   ├── Employee.java
│   │                   │   ├── Developer.java
│   │                   │   ├── Manager.java
│   │                   │   ├── EmployeeRepository.java
│   │                   │   ├── EmployeeService.java
│   │                   │   └── EmployeeController.java
│   │                   │
│   │                   ├── department/
│   │                   ├── project/
│   │                   ├── task/
│   │                   ├── customer/
│   │                   ├── invoice/
│   │                   ├── authentication/
│   │                   ├── report/
│   │                   └── shared/
│   │
│   └── test/
│       └── java/
│           └── com/
│               └── moise/
│                   └── erp/
│
└── data/
```

This is the **planned destination**, not the initial implementation.

Directories and classes will be created as their functionality becomes necessary.

---

# Implementation Roadmap

## Phase 0 — Project Foundation

### Goals

Set up the project correctly before implementing business functionality.

### Tasks

* [ ] Create Maven project
* [ ] Configure Java 25
* [ ] Configure project metadata in `pom.xml`
* [ ] Create Maven source structure
* [ ] Create test structure
* [ ] Create `.gitignore`
* [ ] Create initial README
* [ ] Initialize Git repository
* [ ] Connect repository to GitHub
* [ ] Create initial commit

### Java Concepts

* Java project structure
* Packages
* Maven basics
* `pom.xml`
* Build lifecycle

---

# Phase 1 — Java Fundamentals

Before making the application complex, the fundamentals will be learned and applied.

### Topics

* Variables
* Primitive data types
* Reference types
* Strings
* Operators
* Type casting
* Input and output
* Conditional statements
* `if`
* `else`
* `else if`
* `switch`
* Loops
* `for`
* `while`
* `do-while`
* Arrays
* Multidimensional arrays
* Methods
* Parameters
* Return values
* Method overloading
* Variable scope
* `static`
* `final`

### Application

Begin the Employee domain.

---

# Phase 2 — Classes and Objects

### Topics

* Classes
* Objects
* Fields
* Methods
* Constructors
* Constructor overloading
* `this`
* Access modifiers
* Encapsulation
* Getters
* Setters
* Static members
* Final members

### Application

Create the first real `Employee` model.

Example direction:

```text
employee/
└── Employee.java
```

Employees will eventually contain information such as:

* ID
* First name
* Last name
* Email
* Salary
* Department
* Employment information

---

# Phase 3 — Employee Feature

Build the first complete application feature.

### Components

```text
employee/
├── Employee.java
├── EmployeeRepository.java
├── EmployeeService.java
└── EmployeeController.java
```

### Topics

* Separation of responsibilities
* Repository pattern
* Service layer
* Basic application flow
* Collections
* `ArrayList`
* Iterators
* Searching
* Updating
* Deleting

Application flow:

```text
Main
 ↓
EmployeeController
 ↓
EmployeeService
 ↓
EmployeeRepository
 ↓
Employee
```

---

# Phase 4 — Inheritance and Polymorphism

Introduce different employee types.

Example:

```text
Employee
├── Developer
├── Manager
└── Accountant
```

### Topics

* Inheritance
* `extends`
* `super`
* Constructors in inheritance
* Method overriding
* Method overloading
* Polymorphism
* Upcasting
* Downcasting
* `instanceof`
* `protected`

The concepts will be implemented through the employee domain.

---

# Phase 5 — Abstraction and Interfaces

### Topics

* Abstract classes
* Abstract methods
* Interfaces
* Implementing interfaces
* Multiple interfaces
* Interface inheritance
* Default methods
* Static interface methods
* Polymorphism through interfaces

### Application

Interfaces will be introduced where they solve an actual design problem.

---

# Phase 6 — Departments

Create the Department domain.

```text
department/
├── Department.java
├── DepartmentRepository.java
├── DepartmentService.java
└── DepartmentController.java
```

### Topics

* Object relationships
* Composition
* Aggregation
* Collections of objects
* Object references
* Encapsulation across domains

---

# Phase 7 — Projects

Create project management functionality.

```text
project/
├── Project.java
├── ProjectRepository.java
├── ProjectService.java
└── ProjectController.java
```

Projects will connect employees, departments, and tasks.

### Topics

* Object relationships
* Composition
* Collections
* Enums
* Date and time API

---

# Phase 8 — Tasks

Build the Task domain.

```text
task/
├── Task.java
├── TaskStatus.java
├── Priority.java
├── TaskRepository.java
├── TaskService.java
└── TaskController.java
```

### Topics

* Enums
* `LocalDate`
* `LocalDateTime`
* Collections
* Searching
* Filtering
* Sorting

---

# Phase 9 — Collections Framework

Deep dive into Java collections.

### Topics

#### Lists

* `ArrayList`
* `LinkedList`

#### Sets

* `HashSet`
* `LinkedHashSet`
* `TreeSet`

#### Maps

* `HashMap`
* `LinkedHashMap`
* `TreeMap`

#### Queues

* `Queue`
* `PriorityQueue`
* `Deque`

#### Iteration

* `Iterator`
* Enhanced `for`
* `forEach`

We will learn when and why to use each structure.

---

# Phase 10 — Generics

### Topics

* Generic classes
* Generic methods
* Generic interfaces
* Type parameters
* Bounded type parameters
* Wildcards
* Upper bounds
* Lower bounds

The repository architecture will eventually be generalized where appropriate.

Example direction:

```java
Repository<T, ID>
```

---

# Phase 11 — Exception Handling

### Topics

* Exceptions
* `try`
* `catch`
* `finally`
* `throw`
* `throws`
* Checked exceptions
* Unchecked exceptions
* Custom exceptions
* Exception propagation
* Try-with-resources

Exceptions will be introduced according to actual application requirements.

---

# Phase 12 — File Handling

The application will learn to work with files.

### Topics

* `File`
* `Path`
* `Files`
* Reading files
* Writing files
* `BufferedReader`
* `BufferedWriter`
* File streams
* Try-with-resources

Potential application features:

* Data export
* Import
* Logs
* Reports

---

# Phase 13 — Validation and Regular Expressions

### Topics

* Input validation
* String validation
* Regular expressions
* `Pattern`
* `Matcher`

Potential validation:

* Email
* Phone number
* Employee ID
* Project code
* User input

---

# Phase 14 — Lambda Expressions

### Topics

* Lambda syntax
* Functional interfaces
* Lambda parameters
* Lambda return values
* Method references

Example direction:

```java
task -> task.isCompleted()
```

---

# Phase 15 — Functional Interfaces

### Topics

* `Predicate`
* `Consumer`
* `Function`
* `Supplier`
* Custom functional interfaces

---

# Phase 16 — Stream API

### Topics

* `stream()`
* `filter()`
* `map()`
* `sorted()`
* `distinct()`
* `limit()`
* `count()`
* `findFirst()`
* `anyMatch()`
* `allMatch()`
* `collect()`
* `toList()`

Streams will be applied to real ERPM data.

---

# Phase 17 — Sorting

### Topics

* `Comparable`
* `Comparator`
* Natural ordering
* Custom ordering
* Multiple sorting conditions
* Method references

Examples:

```text
Employees by name
Employees by salary
Tasks by priority
Tasks by deadline
Projects by status
```

---

# Phase 18 — Authentication and Users

Create:

```text
authentication/
├── User.java
├── Role.java
├── AuthenticationService.java
└── AuthenticationController.java
```

### Topics

* Enums
* Password handling concepts
* Roles
* Authentication flow
* Authorization concepts
* Object relationships

---

# Phase 19 — Customers and Invoices

Introduce:

```text
customer/
invoice/
```

### Topics

* More complex object relationships
* Collections
* Composition
* Business rules
* Calculations
* Validation

---

# Phase 20 — Multithreading and Concurrency

### Topics

* Threads
* `Runnable`
* Thread lifecycle
* `ExecutorService`
* Tasks
* Synchronization
* Race conditions
* Concurrent collections
* Basic concurrency concepts

Potential application uses:

* Background report generation
* Notifications
* Periodic operations

---

# Phase 21 — Database and JDBC

Move from in-memory data to PostgreSQL.

### Topics

* JDBC
* Database connections
* SQL
* `Connection`
* `PreparedStatement`
* `ResultSet`
* CRUD operations
* Transactions
* SQL exceptions
* Resource management

Architecture:

```text
Controller
    ↓
Service
    ↓
Repository
    ↓
JDBC
    ↓
PostgreSQL
```

---

# Phase 22 — Testing

Introduce automated testing.

### Topics

* JUnit
* Unit tests
* Assertions
* Test lifecycle
* Test organization
* Testing services
* Testing repositories
* Edge cases

---

# Phase 23 — Reporting

Build the reporting domain.

Possible reports:

* Employee report
* Project report
* Task completion report
* Department report
* Financial report

This phase will combine many previously learned Java concepts.

---

# Phase 24 — Refactoring and Professionalization

Once the application is large enough, we will review it.

### Topics

* Clean code
* Separation of concerns
* DRY
* SOLID principles
* Composition vs inheritance
* Dependency management
* Code organization
* Refactoring
* Error handling
* Testing strategy

We will refactor code based on problems we actually encounter rather than learning these principles only theoretically.

---

# Git Commit Strategy

Every meaningful milestone will be committed.

Examples:

```text
Initial Maven project setup

Add project README and implementation roadmap

Implement Employee model

Add Employee constructors

Implement Employee encapsulation

Add employee repository

Add employee service

Add employee controller

Implement employee inheritance

Implement employee polymorphism

Add department feature

Add project feature

Add task management

Implement generic repository

Add exception handling

Add file persistence

Add stream-based reporting

Add JDBC persistence

Add PostgreSQL integration

Add unit tests
```

Commit messages will describe **what changed**, not simply:

```text
update
fix
stuff
changes
```

---

# Learning Rules

This project follows several rules.

### Rule 1 — Understand before implementing

A Java concept will be explained before it is used.

### Rule 2 — No blind copying

Code should be typed and understood rather than copied without explanation.

### Rule 3 — Build incrementally

We will not implement the entire application at once.

### Rule 4 — Use real application requirements

Java concepts should have a meaningful reason for being used.

### Rule 5 — Ask why

For every important design decision, we should understand why it was chosen.

### Rule 6 — Test what we build

Features should be verified before moving forward.

### Rule 7 — Commit meaningful milestones

The Git history should show the evolution of the application.

---

# Current Status

```text
Phase 0 — Project Foundation       🔄 In Progress
Phase 1 — Java Fundamentals        ⏳ Not Started
Phase 2 — Classes and Objects      ⏳ Not Started
Phase 3 — Employee Feature         ⏳ Not Started
Phase 4 — Inheritance              ⏳ Not Started
Phase 5 — Abstraction/Interfaces   ⏳ Not Started
Phase 6 — Departments              ⏳ Not Started
Phase 7 — Projects                 ⏳ Not Started
Phase 8 — Tasks                    ⏳ Not Started
Phase 9 — Collections              ⏳ Not Started
Phase 10 — Generics                ⏳ Not Started
Phase 11 — Exceptions              ⏳ Not Started
Phase 12 — File Handling           ⏳ Not Started
Phase 13 — Validation/Regex        ⏳ Not Started
Phase 14 — Lambdas                 ⏳ Not Started
Phase 15 — Functional Interfaces   ⏳ Not Started
Phase 16 — Streams                 ⏳ Not Started
Phase 17 — Sorting                 ⏳ Not Started
Phase 18 — Authentication          ⏳ Not Started
Phase 19 — Customers/Invoices      ⏳ Not Started
Phase 20 — Concurrency             ⏳ Not Started
Phase 21 — JDBC/PostgreSQL         ⏳ Not Started
Phase 22 — Testing                 ⏳ Not Started
Phase 23 — Reporting               ⏳ Not Started
Phase 24 — Refactoring             ⏳ Not Started
```

---

# Project Status

**Status:** Learning / Development

**Build System:** Maven

**Java Version:** 25

**IDE:** IntelliJ IDEA

**Database:** PostgreSQL — planned

**Testing:** JUnit — planned

**Repository:** Git / GitHub

---

# Author

**YEHOVAYIRE Moise**

GitHub: [Moise-codes](https://github.com/Moise-codes)
