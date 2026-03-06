# Task 5 — Smart Home Security System (Real-Time Monitoring)

## System Description

This task models the behavior of an IoT-based smart home security system that continuously monitors a house for potential security threats. The system runs in real time and operates 24/7 using an infinite monitoring loop.

The system checks several types of sensors during each iteration of the loop:

* Motion sensors
* Door sensors
* Window sensors

If any suspicious activity is detected, the system analyzes the situation and determines the level of threat. Based on the threat level, different security actions are triggered, such as activating cameras and sending notifications to the homeowner.

The system also checks whether the homeowner is currently at home in order to reduce false alarms.

Notifications are sent through multiple communication channels:

* SMS
* Mobile application notifications
* Email alerts

After handling a potential security event, the system waits briefly and continues monitoring the sensors. The monitoring process only resets the alarm state when a reset command is received, but the system itself continues running indefinitely.

This design reflects how real IoT security systems operate in practice: continuous monitoring, automated threat detection, and multi-channel alerting.

---

## System Workflow Overview

The overall workflow of the system is:

1. The system starts and verifies whether the security system is active.
2. Sensors are continuously monitored in an infinite loop.
3. Motion sensors and door/window sensors are checked.
4. If a potential threat is detected, the system evaluates whether the homeowner is at home.
5. The system determines the alarm level:

   * **Low:** Possible false alarm.
   * **Medium:** Suspicious activity detected.
   * **High:** Multiple threats detected.
6. If the alarm level is medium or high, the security camera is activated.
7. Notifications are sent to the homeowner via SMS, mobile app, and email.
8. The system waits for a short period.
9. The system checks whether a reset command has been received.
10. Monitoring continues.

This loop continues indefinitely in order to provide real-time protection.

---

## Files in This Task

This folder contains the following files:

* **pseudocode.md**
  Plain English pseudocode describing the system logic.

* **flowchart.dot**
  Graphviz DOT code representing the flowchart of the system.

* **flowchart-dot.png**
  Flowchart diagram exported from Graphviz.

* **flowchart.mmd**
  Mermaid flowchart code.

* **flowchart-mermaid.png**
  Flowchart diagram exported from Mermaid Live Editor.

* **llm-conversations.txt**
  Notes and prompts used while generating the system logic with an LLM.

---

## Personal Notes

While completing this task, I focused on modeling the behavior of a **real-time system** that runs continuously rather than stopping after one execution. This required designing the algorithm around an **infinite monitoring loop**.

One of the key challenges was representing a continuously running system using flowcharts. Instead of ending the diagram, the flow returns to the sensor monitoring step to represent ongoing surveillance.

Another important design decision was the use of **different alarm levels**. This helps reduce false alarms while still allowing the system to react appropriately to more serious threats.

This task helped reinforce several concepts:

* Algorithmic thinking for real-time systems
* Using loops and conditions in system design
* Converting logical system behavior into flowcharts
* Representing infinite loops in diagram tools like Graphviz and Mermaid

Overall, this exercise demonstrated how software logic can be used to model practical IoT systems such as smart home security platforms.
