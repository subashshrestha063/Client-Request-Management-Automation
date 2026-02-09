# Scenario 3 – Team Reminder for Pending Requests

## Purpose
This scenario prevents **missed or forgotten client requests** by sending reminders
for requests that remain unattended beyond a defined time window.

It improves response time and operational discipline.

---

## Trigger
- Scheduled execution (time-based check)

---

## Logic Overview
The scenario scans the request sheet at scheduled intervals.

1. **Pending Request Identification**
   - Requests with status `New` or `In Review`
   - No update within the defined reminder threshold

2. **Time-Based Logic**
   - Calculates time since last status update
   - Identifies overdue requests

3. **Notification Control**
   - Sends reminder only once per cycle
   - Prevents notification spam

4. **Internal Escalation**
   - Reminder sent to team via Discord
   - Optional tagging of responsible team

---

## Output
- Timely reminders for unattended requests
- Reduced risk of lost leads
- Improved internal accountability

---

## Platform & Components
- Google Sheets (timestamp tracking)
- Make.com (scheduled checks & filters)
- Discord (team reminders)

---
## Blueprint

The Make.com blueprint for this scenario is available here:
- [blueprints/scenario-3.json](/blueprints/scenario-3.json)

Import this file into Make.com to explore or replicate the automation logic.

---

## Screenshots
See the [screenshots/scenario-3](/screenshots/scenario-3) folder for:
- Scheduled scenario configuration
- Reminder logic filters
- Discord reminder messages
