# ATM Cash Withdrawal System

## Overview

This project demonstrates the design of an **ATM cash withdrawal system** using pseudocode and flowcharts.
The goal is to model the logical steps of withdrawing money from an ATM while applying programming logic and algorithm design principles.

The system includes important ATM features such as:

* PIN verification with a maximum of **3 attempts**
* **Balance checking**
* **Withdrawal amount validation** (must be multiples of 20 TL)
* **Daily withdrawal limit control**
* Option to **repeat another transaction**

The project also converts the algorithm into two flowchart representations:

* **Graphviz DOT**
* **Mermaid Flowchart**

Both diagrams follow standard flowchart symbols.

---

## Flowchart Symbol Conventions

The following shapes are used in the diagrams:

| Symbol         | Meaning        |
| -------------- | -------------- |
| Oval / Stadium | Start or End   |
| Parallelogram  | Input / Output |
| Rectangle      | Process        |
| Diamond        | Decision       |

To keep the diagrams clean, **programming commands such as READ, PRINT, and SET are not displayed in the flowcharts.**
Instead, the diagrams show the **logical actions and decisions of the ATM system.**

---

## System Logic

The ATM withdrawal process follows these steps:

1. The user enters their **PIN**.
2. The system checks whether the PIN is correct.
3. The user has **up to three attempts** to enter the correct PIN.
4. If the PIN is correct, the user enters a **withdrawal amount**.
5. The system verifies:

   * The amount is a **multiple of 20 TL**
   * The account has **sufficient balance**
   * The **daily withdrawal limit** is not exceeded
6. If all checks pass, the ATM **dispenses the cash** and updates the balance.
7. The user can choose to **perform another transaction** or end the session.

If the PIN is entered incorrectly three times, the **card is blocked** and the process ends.

---

## Project Structure

```
task1-atm-system/
│
├── pseudocode.md
├── flowchart.dot
├── flowchart-dot.png
├── flowchart.mmd
├── flowchart-mermaid.png
└── README.md
```

---

## Tools Used

* **Graphviz** – used to generate flowcharts from DOT language
* **Mermaid Live Editor** – used to create flowcharts from Mermaid syntax
* **Markdown** – used for documentation

---

## Purpose of the Project

This project demonstrates how an algorithm can be represented in multiple formats:

* **Pseudocode** → Human-readable algorithm description
* **Graphviz DOT** → Programmatically generated diagrams
* **Mermaid Flowchart** → Markdown-friendly visual diagrams

It helps illustrate how logical program design can be translated into clear visual representations.
