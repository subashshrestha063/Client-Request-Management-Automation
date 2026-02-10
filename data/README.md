# Data Templates (Google Sheets)

This folder documents the **Google Sheets data structure** used by the
Prime Flow Solutions automation system.

The automation scenarios rely on a shared Google Sheets template that
acts as the system’s database for client intake, project tracking,
reminders, and analytics.

---

## 📊 Google Sheets Template

👉 **Access the Google Sheets template:**  

🔗 [Click here to open the template](https://docs.google.com/spreadsheets/d/1MzJxkOjZNQ-KHV__wnJhCYHxIjk4EevQDfKTaETV6uo/edit?usp=sharing)**


> ⚠️ Important:  
> Do **NOT** request edit access.  
> Always click **File → Make a copy** and use your own version.


### How to Use
1. Open the Google Sheets link
2. Click **File → Make a copy**
3. Save it to your own Google Drive
4. Connect the copied sheet to the Make.com scenarios

⚠️ **Important:**  
Sheet names and column headers **must not be changed** unless you also
update the Make.com modules.

---

## 📑 Sheets Overview

### 1️⃣ Client Requests Sheet
Primary data source for all incoming client requests.

Used by:
- Scenario 1 – Client Intake & Auto-Rejection
- Scenario 2 – Client Status & Project Lifecycle
- Scenario 3 – Team Reminder Automation
- Scenario 4 – Daily Service Demand Analytics

Key columns include:
- Date
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

---

### 2️⃣ Service Analytics Sheet
Stores aggregated service demand metrics generated daily.

Used by:
- Scenario 4 – Daily Service Demand Analytics

Key columns include:
- Date
- Service Type
- Number of Requests

This sheet enables:
- Service popularity tracking
- Demand trend analysis
- Business decision insights

---

## 🔄 Scenario Dependency Map

| Scenario | Data Usage |
|--------|-----------|
| Scenario 1 | Reads & writes client request records |
| Scenario 2 | Updates status, assignment, timestamps |
| Scenario 3 | Checks pending requests & reminder flags |
| Scenario 4 | Aggregates daily service demand data |

---

## 📌 Notes

- This data model is **automation-first**
- Google Sheets acts as a lightweight operational database
- Designed for learning, demonstration, and portfolio presentation
- Easily extendable for weekly/monthly analytics

For automation logic and flows, refer to:
- [scenarios](/scenarios/) — scenario documentation
- [blueprints](/blueprints/) — Make.com scenario JSON exports
