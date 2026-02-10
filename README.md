# 🚀 Prime Flow Solutions – Client Request Management Automation

![Make.com](https://img.shields.io/badge/Platform-Make.com-purple?style=flat&logo=make)
![Google Forms](https://img.shields.io/badge/Input-Google%20Forms-blue?style=flat&logo=google-forms)
![Google Sheets](https://img.shields.io/badge/Database-Google%20Sheets-green?style=flat&logo=google-sheets)
![Discord](https://img.shields.io/badge/Notifications-Discord-5865F2?style=flat&logo=discord)
![Gmail](https://img.shields.io/badge/Email-Gmail-red?style=flat&logo=gmail)
![Status](https://img.shields.io/badge/Project-Completed-success)

> A production-style automation system simulating a **freelancing / automation agency workflow**, built using **Make.com** to manage client intake, project lifecycle, reminders, and service-demand analytics.

This project focuses on **workflow automation, operational logic, and real business constraints**, not frontend or UI design.

---

## 📖 Overview

**Prime Flow Solutions** is a fictional automation agency that receives multiple service requests daily—web design, automation, branding, and more.

Common challenges:
- Low-quality or unrealistic client requests
- Manual status tracking
- Missed follow-ups by the team
- No visibility into which services are most in demand

This automation system solves those problems using **modular, no-code workflows** built in Make.com.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|-----|-------|
| **Make.com** | Core automation platform |
| **Google Forms** | Client request intake |
| **Google Sheets** | Data backend and analytics |
| **Discord** | Internal alerts and reminders |
| **Gmail** | Client communication |
| **Make Data Stores** | Temporary state & aggregation |

---

## ⚙️ System Architecture

The system is divided into **4 independent automation scenarios**, each responsible for a specific business function.

| ID | Scenario | Description |
|----|--------|-------------|
| **Scenario 1** | Client Intake & Auto-Rejection | Validates new client requests and auto-rejects invalid leads |
| **Scenario 2** | Client Status & Project Lifecycle Automation | Tracks project stages and sends notifications |
| **Scenario 3** | Team Reminder for Pending Requests | Sends reminders for unattended or stalled requests |
| **Scenario 4** | Daily Service Demand Analytics | Aggregates daily service requests for insights |

Each scenario is documented individually in the [`/scenarios`](scenarios/) folder.

---

## 🔁 Scenario Breakdown

### Scenario 1 – Client Intake & Auto-Rejection
- Triggered by Google Form submissions
- Validates budget, deadline, and service type
- Automatically rejects low-quality or unrealistic requests
- Stores valid leads in Google Sheets

---

### Scenario 2 – Client Status & Project Lifecycle Automation
- Tracks project status changes:
  - New → In Review → Approved → In Progress → Completed → Rejected
- Sends automated email updates to clients
- Posts internal Discord notifications
- Updates timestamps and assignments

---

### Scenario 3 – Team Reminder for Pending Requests
- Runs on a scheduled basis
- Identifies requests stuck in **New** or **Approved**
- Sends reminders to internal Discord channels
- Prevents missed leads and delays

---

### Scenario 4 – Daily Service Demand Analytics
- Executes once per day
- Counts number of requests per service type
- Uses date–metric–label–value aggregation structure
- Generates insights such as:
  - Total applications received today
  - Service-wise demand (Web Design, Automation, Branding, etc.)

---
## 🖼️ Screenshots
See visual references of each scenario in:  

- [`Screenshots`](/screenshots)

---

## 📊 Data Design (Google Sheets)

### Core Column ( Client_Requests)
- Contact Date
- Client Name
- Email
- Service Required
- Project Description
- Budget
- Deadline
- Status
- Last Notified Status
- Last Status Update
- Reminder Sent
- Comments

Each row represents a single client request, enabling reliable aggregation and reporting.

### Core Column (Service Analytics)
- Date
- Service Required
- Number of Requests

---

## 📊 Data Templates
The Google Sheets structure used by this automation is documented here:
- [Data Templates](data/)
  
---

## 🚀 How to Run

1. Open the Google Sheets template from the [`/data`](data/) folder.
2. Click **File → Make a copy** and save it to your Google Drive.
3. Create scenarios in **Make.com**
4. Import JSON blueprints from the [`/blueprints`](blueprints/) folder
5. Create Google Sheets using the documented structure
6. Reconnect your Google, Gmail, and Discord accounts

> ⚠️ **Note:**  
> Blueprints are provided for learning and reference.  
> Minor adjustments may be required depending on your setup.

---

## ✨ Key Features

- Automated client intake and validation
- Auto-rejection of low budget requests
- Project lifecycle tracking
- Internal team reminders
- Prevention of duplicate reminders
- Daily service demand analytics


---

## 🧠 Learnings & Highlights

- Designing automations as independent services
- Preventing duplicate notifications
- Using **COUNT-based aggregation** for analytics
- Handling time-based reminders
- Structuring data for future scalability
- Coordinating multiple scenarios around one data source
---

## 📁 Repository Structure

```text
├── README.md
├── scenarios/
│   ├── scenario-1.md
│   ├── scenario-2.md
│   ├── scenario-3.md
│   └── scenario-4.md
├── screenshots/
│   ├── scenario-1/
│   ├── scenario-2/
│   ├── scenario-3/
│   └── scenario-4/
├── blueprints/
│   ├── scenario-1.json
│   ├── scenario-2.json
│   ├── scenario-3.json
│   └── scenario-4.json
└── data/
    └── README.md
```
## 📝 Notes

This project simulates a real freelancing or automation agency workflow.  
It focuses on **process reliability, response time, and operational clarity** rather
than frontend or UI design.

---

## 👤 Author

**Subash Shrestha**  
Automation & Workflow Design (Make)

⭐ If you find this project useful, feel free to explore the  [`scenarios`](scenarios/) and [`screenshots`](screenshots/) for deeper insights.
