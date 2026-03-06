# University Course Registration System

## System Description

This project models the workflow of a **University Course Registration System**. The system simulates how students log into a registration portal, select courses, and complete the registration process while the system performs several academic and administrative checks.

The goal of this task is to represent the system using **pseudocode** and **flowcharts** created with **Graphviz DOT** and **Mermaid**.

The system includes the following main stages:

1. **Login**

   * The student logs into the system using their credentials.
   * The system verifies whether the login information is valid.

2. **Course List Display**

   * After successful login, the system shows the list of available courses.

3. **Course Selection**

   * The student selects courses one by one from the list.

4. **Validation Checks**

   * For each selected course, the system performs several checks:

     * Course quota availability
     * Completion of prerequisite courses
     * Schedule conflicts with other selected courses
     * Credit limit validation

5. **Advisor Approval**

   * In some universities, the course selection must be approved by an academic advisor.
   * If approval is required, the selected courses are sent to the advisor for confirmation.

6. **Registration Confirmation**

   * If all checks pass and the advisor approves (if required), the registration is finalized.

---

## Validation Checks Performed

During course registration the system performs the following validations:

* **Quota Check**
  Ensures that the course still has available seats.

* **Prerequisite Check**
  Verifies that the student has completed all required prerequisite courses.

* **Schedule Conflict Check**
  Confirms that the selected course does not overlap with the schedule of other courses.

* **Credit Limit Check**
  Ensures that the student's total course credits do not exceed the allowed maximum.

* **Advisor Approval**
  Some institutions require the student's academic advisor to approve the course selection.

---

## Project Structure

```
task-course-registration-system/

pseudocode.md
flowchart.dot
flowchart-dot.png
flowchart.mmd
flowchart-mermaid.png
README.md
llm-conversations.txt
```

---

## Personal Notes

While working on this task, the main objective was to clearly represent the **decision-making process of a course registration system**. The most important part was modeling the validation logic using **nested IF-THEN structures and loops**.

Some key points considered during the design:

* Each validation step must be performed in sequence before a course is accepted.
* If any check fails, the course is rejected and the student can select another one.
* The system should allow the student to select multiple courses.
* Advisor approval is included as a final decision step when required.

The diagrams were designed so that:

* **All control points are represented with diamond shapes**
* The diagrams focus on **decision flow rather than programming commands**
* Operations such as reading input or printing output are intentionally not shown in the flowchart to keep the diagram clear and focused on logic.

This project helped in understanding how real university registration systems enforce academic policies and manage course selection processes.
