# Object-Oriented Programming Projects (01076106)

This repository contains programming exercises and system design projects completed as part of the **01076106 Object-Oriented Programming** course.

The projects progressively introduce core programming concepts including algorithm design, data structures, and object-oriented system architecture using **Python**. Each week focuses on a different topic, gradually increasing in complexity from basic logic problems to multi-class system simulations.

---

# Repository Structure

```
.
├── Week1
│   ├── Week1_1.py
│   ├── Week1_2.py
│   ├── Week1_3.py
│   ├── Week1_5.py
│   └── Week1_6.py
│
├── Week2
│   ├── week2_1.py
│   ├── week2_2.py
│   ├── week2_3.py
│   ├── week2_4.py
│   └── week2_5.py
│
├── Week3
│   └── week3.py
│
├── Week4
│   └── week4.py
│
└── Week5
    └── Lab5_skeleton.py
```

---

# Technologies

* Python 3
* Object-Oriented Programming (OOP)
* Python Standard Library
* `unittest` testing framework

---

# Week 1 – Python Logic and Algorithms

Week 1 focuses on fundamental programming and algorithmic thinking using Python.

## Topics Covered

* Mathematical computation
* String and numeric manipulation
* Sorting and list processing
* Basic algorithm design

## Exercises

| File         | Description                                             |
| ------------ | ------------------------------------------------------- |
| `Week1_1.py` | Computes the series: `a + aa + aaa + aaaa`              |
| `Week1_2.py` | Finds the largest palindrome from two *n-digit* numbers |
| `Week1_3.py` | Calculates parking fees based on time duration          |
| `Week1_5.py` | Rearranges digits to produce the smallest valid number  |
| `Week1_6.py` | Determines the maximum product pair in a list           |

Example:

```
Input:
3

Output:
3702
```

Computation:

```
3 + 33 + 333 + 3333
```

---

# Week 2 – Data Structures and Date Logic

Week 2 introduces **Python dictionaries, nested data structures, and date calculations**.

## Topics Covered

* Dictionary operations
* Nested data structures
* Leap year detection
* Date validation
* Data parsing and transformation

## Exercises

| File         | Description                                             |
| ------------ | ------------------------------------------------------- |
| `week2_1.py` | Calculates the ordinal day of the year for a given date |
| `week2_2.py` | Computes the number of days between two dates           |
| `week2_3.py` | Updates subject scores and calculates averages          |
| `week2_4.py` | Implements a nested gradebook system                    |
| `week2_5.py` | Manages a music collection database                     |

Example:

```
Input:
1-3-2020

Output:
day of year: 61
is_leap: True
```

---

# Week 3 – University Enrollment System

Week 3 introduces **Object-Oriented Programming** through a university enrollment system.

## System Overview

The system manages relationships between students, subjects, and instructors while tracking course enrollments and grades.

## Core Classes

| Class        | Responsibility                                      |
| ------------ | --------------------------------------------------- |
| `Student`    | Represents a university student                     |
| `Subject`    | Represents a course offered by the university       |
| `Teacher`    | Represents an instructor                            |
| `Enrollment` | Associates students with subjects and stores grades |

## Key Features

### Enrollment Management

Students can enroll in and drop courses while preventing duplicate registrations.

### Grade Assignment

Grades are stored within enrollment records.

### GPA Calculation

The system computes GPA using a weighted average based on course credits.

```
GPA = Σ(grade_point × credit) / Σ(credit)
```

### Data Queries

The system can:

* retrieve student records
* count enrolled students in a course
* retrieve the instructor of a subject

## Testing

The script includes **14 built-in test cases** to verify system functionality.

---

# Week 4 – ATM Banking System Simulation

Week 4 builds a **banking system simulation** that models ATM operations.

## System Components

| Class        | Description                             |
| ------------ | --------------------------------------- |
| `Bank`       | Stores users and ATM machines           |
| `User`       | Represents a bank customer              |
| `Account`    | Stores account balance and transactions |
| `ATMCard`    | Represents a physical ATM card          |
| `ATMMachine` | Performs ATM operations                 |

## Features

### Authentication

Users must insert a card and enter the correct PIN before accessing the system.

### Withdrawals

Withdrawal requests validate:

* account balance
* ATM machine cash availability
* card withdrawal limit

### Deposits and Transfers

The system supports:

* cash deposits
* account-to-account transfers
* transaction recording

## Testing

The system contains **10 predefined test cases** verifying common scenarios such as invalid deposits, withdrawal limits, and insufficient ATM cash.

---

# Week 5 – Advanced Banking System

Week 5 expands the banking simulation using **inheritance and automated testing**.

## System Design

The system uses multiple inheritance hierarchies.

### Account Types

| Class            | Description                              |
| ---------------- | ---------------------------------------- |
| `SavingAccount`  | Standard account with interest           |
| `FixedAccount`   | Time-locked account with higher interest |
| `CurrentAccount` | Transactional account for merchants      |

### Card Types

| Class               | Description                     |
| ------------------- | ------------------------------- |
| `ATMCard`           | ATM-only card                   |
| `DebitCard`         | Base debit card class           |
| `ShoppingDebitCard` | Provides cashback for purchases |
| `TravelDebitCard`   | Standard debit card variant     |

### Transaction Channels

| Channel      | Description                                    |
| ------------ | ---------------------------------------------- |
| `ATMMachine` | Handles ATM transactions                       |
| `Counter`    | Bank branch service with identity verification |
| `EDCMachine` | Merchant payment terminal                      |

## Advanced Features

### Fixed Account Maturity

Interest depends on whether the withdrawal occurs before or after the maturity date.

### Electronic Payments

Debit cards can be used on EDC machines for merchant payments.
Shopping debit cards provide cashback for eligible transactions.

### Identity Verification

Branch transactions require verification of the customer's citizen ID.

---

# Unit Testing

The project uses Python's **unittest framework** with approximately **19 automated test cases** validating:

* interest calculations
* early withdrawals
* ATM withdrawal limits
* card authentication
* EDC payment validation
* identity verification

Run tests with:

```
python -m unittest Lab5_skeleton.py -v
```

---

# Learning Outcomes

This repository demonstrates practical experience with:

* Python programming fundamentals
* Data structures and algorithms
* Object-oriented design principles
* Class relationships and system modeling
* Automated testing with `unittest`
