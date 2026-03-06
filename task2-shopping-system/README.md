# E-Commerce Cart Management and Checkout System

## Overview

This task demonstrates the logic of an **e-commerce cart management and checkout system**.
The system models a typical online shopping process including user authentication, adding products to a cart, checking product availability, applying discount codes, calculating shipping fees, and completing payment.

The goal of this task is to represent the system logic in three different ways:

1. **Pseudocode** – Human-readable algorithm description
2. **Graphviz DOT diagram** – Flowchart generated using Graphviz
3. **Mermaid flowchart** – Flowchart generated using Mermaid syntax

The diagrams visualize the control flow of the system while avoiding low-level commands such as `READ`, `SET`, or `PRINT`.

---

## System Workflow

The system follows these main steps:

1. **User Login**

   * The user attempts to log in.
   * If the credentials are invalid, the system requests another attempt.

2. **Shopping / Cart Management**

   * The user selects a product.
   * The system checks whether the product is in stock.
   * If available, the product is added to the cart.
   * The user can continue shopping or proceed to checkout.

3. **Discount Code**

   * The user may enter a discount code.
   * The system verifies whether the code is valid.
   * If valid, the discount is applied to the cart total.

4. **Shipping Fee Calculation**

   * The system checks whether the order qualifies for free shipping.
   * If not, a shipping fee is added.

5. **Payment**

   * The user attempts payment.
   * If the payment fails, the user may try again.
   * If successful, the order is confirmed.

---

## Control Points (Decision Nodes)

The system contains several decision points that control the workflow:

* Are the login credentials valid?
* Is the selected product in stock?
* Does the user want to continue shopping?
* Does the user have a discount code?
* Is the discount code valid?
* Is the order eligible for free shipping?
* Was the payment successful?

These decisions are represented as **diamond nodes in the diagrams** with **YES / NO branches**.

---

## Files in This Folder

| File                    | Description                                         |
| ----------------------- | --------------------------------------------------- |
| `pseudocode.md`         | Step-by-step pseudocode describing the system logic |
| `flowchart.dot`         | Graphviz DOT code used to generate the flowchart    |
| `flowchart_dot.png`     | Flowchart exported from Graphviz                    |
| `flowchart.mmd`         | Mermaid flowchart syntax                            |
| `flowchart_mermaid.png` | Flowchart exported from Mermaid Live                |
| `llm-conversations.txt` | Record of AI-assisted development discussions       |

---

## Tools Used

* **Graphviz** – Used to generate the DOT flowchart diagram
* **Mermaid Live Editor** – Used to generate the Mermaid flowchart
* **Markdown** – Used for documentation and pseudocode formatting

---

## Notes

* Decision points in the diagrams include **YES / NO labels**.
* The diagrams focus on **system logic**, not implementation details.
* Commands like `READ`, `SET`, and `PRINT` were intentionally omitted from diagrams to keep them visually clean and focused on workflow.

---

## Author

Prepared as part of a programming assignment demonstrating algorithm design and flowchart representation.
