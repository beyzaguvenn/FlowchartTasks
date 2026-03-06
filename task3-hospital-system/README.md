# Hospital Appointment and Test Results System

## System Description

This project models a simple **hospital information system** that allows patients to make medical appointments and access laboratory test results. The system verifies the patient's identity using an ID number and provides a main menu where the user can choose between two main actions:

1. Making an appointment
2. Viewing laboratory test results

The system is designed using a **modular approach**, where each functionality is implemented as a separate module. This structure improves readability, maintainability, and scalability.

The workflow of the system includes:

* Patient identity verification
* Main menu action selection
* Appointment creation process
* Viewing laboratory test results
* Option to repeat actions within a loop

The system is represented in three formats:

* **Pseudocode** written in plain English
* **Graphviz DOT flowchart**
* **Mermaid flowchart**

Each format describes the same logic using different representations.

---

## Module 1: Appointment System

The appointment module allows the patient to create a hospital appointment. The process includes the following steps:

* Selecting a clinic
* Displaying the list of available doctors
* Showing available time slots
* Allowing the patient to confirm the appointment
* Sending an SMS notification after confirmation

A loop structure allows the user to select another time slot if the appointment is not confirmed.

---

## Module 2: Test Results System

The test results module allows the patient to check laboratory results.

The algorithm performs the following checks:

* Verify whether the patient has any test records
* Check whether the results are ready
* Display the results if they are available
* Show a waiting message if results are not ready yet
* Provide an option to download the results as a PDF file

---

## System Flow

Both modules are connected through a **main menu system**. After completing any action, the user is asked whether they want to perform another operation. This is implemented using a loop structure that returns the user to the main menu.

---

## Technologies Used

The system design was represented using the following formats and tools:

* **Pseudocode** – algorithm description in plain English
* **Graphviz DOT** – flowchart generation
* **Mermaid Flowcharts** – alternative diagram representation

---

## Personal Notes

While developing this system, the modular design approach helped separate the responsibilities of each component. Creating independent modules for appointments and test results made the algorithm easier to design and understand.

Converting the pseudocode into **Graphviz DOT** and **Mermaid flowcharts** helped visualize the system logic more clearly. The use of subgraphs allowed each module to be represented as an independent block inside the overall system structure.

This exercise also demonstrated how large systems can be broken down into smaller manageable components before combining them into a final integrated system.
