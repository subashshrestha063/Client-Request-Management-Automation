# Automation Scenarios Overview

This folder contains detailed documentation for each automation scenario
implemented in the **Prime Flow Solutions – Client Request Management Automation System**.

Each scenario is designed as an **independent, modular workflow** with a
clear business responsibility. Together, they form a complete operational system
for managing client intake, project lifecycle, reminders, and analytics.

---

## 🧩 Scenario Map

| ID | Scenario Name | Description | Documentation |
|----|--------------|------------|----------------|
| **Scenario 1** | Client Intake & Auto-Rejection | Validates incoming client requests and automatically rejects non-viable leads | [scenario-1.md](scenario-1/README.md) |
| **Scenario 2** | Client Status & Project Lifecycle Automation | Tracks project status changes and sends notifications | [scenario-2.md](scenario-2/README.md) |
| **Scenario 3** | Team Reminder for Pending Requests | Sends reminders for unattended client requests | [scenario-3.md](scenario-3/README.md) |
| **Scenario 4** | Daily Service Demand Analytics | Aggregates daily service demand insights | [scenario-4.md](scenario-4/README.md) |

---

## 🔗 How to Navigate

Each scenario folder contains:
- A **dedicated README** describing its purpose, logic, and outputs
- A matching **Make.com blueprint JSON** (in the `/blueprints` folder)
- Relevant **screenshots** (in the `/screenshots` folder)

To understand a scenario fully:
1. Read its README
2. Review the screenshots
3. Import the corresponding blueprint into Make.com

---

## 🏗️ Design Philosophy

- Scenarios are **loosely coupled**
- Each scenario can run independently
- Failures in one scenario do not block others
- Logic is separated by business responsibility

This structure makes the system:
- Easier to debug
- Easier to extend
- Easier to explain to non-technical stakeholders

---

## 📌 Notes

- Scenario numbering reflects logical flow, not execution dependency.
- Scheduling-based scenarios (like analytics and reminders) run independently.
- All scenarios use Google Sheets as the shared data layer.

---

For system-wide architecture and setup instructions,
refer to the **root README.md**.
