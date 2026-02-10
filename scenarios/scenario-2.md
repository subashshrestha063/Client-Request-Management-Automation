# Scenario 2 – Client Status & Project Lifecycle Automation

## Purpose
This scenario manages the **entire project lifecycle** after a client request is accepted.
It ensures that every status change is tracked, recorded, and communicated automatically.

This creates transparency for both the internal team and the client.

---

## Trigger
- Order / client request status update in Google Sheets

---

## Logic Overview
The scenario continuously monitors the request sheet for status changes.

1. **Status Change Detection**
   - Compares current status with the last notified status
   - Prevents duplicate notifications

2. **Lifecycle Flow**
   - New → In Review → Approved → In Progress → Completed → Rejected

3. **Notification Handling**
   - Client email sent for relevant status changes
   - Internal Discord alerts for operational awareness

4. **Metadata Updates**
   - Last Status Update timestamp is recorded
   - Assigned team or owner is updated if applicable

---

### Scenario Design
<img src="/screenshots/scenario-2/Flow_scenario-2.png" width="850">

## Output
- Automated client email notifications
- Internal Discord notifications
- Accurate lifecycle tracking without manual follow-ups

---
## Discord Notifcations

## Approved
<img src="/screenshots/scenario-2/approved_discord_alert.png" width="600">

## In-Process
<img src="/screenshots/scenario-2/in_process_discord_alert.png" width="600">

## Completed
<img src="/screenshots/scenario-2/completed_discord_alert.png" width="600">

## Email Notifcations

## Approved
<img src="/screenshots/scenario-2/approved_email_alert.png" width="600">

## In-Process
<img src="/screenshots/scenario-2/in_process_email_alert.png" width="600">

## Completed
<img src="/screenshots/scenario-2/completed_email_alert.png" width="600">


## Platform & Components
- Google Sheets (status tracking)
- Make.com (routing & condition logic)
- Gmail (client notifications)
- Discord (internal alerts)

---
## Blueprint

The Make.com blueprint for this scenario is available here:
- [View Blueprints](/blueprints/scenario-2.json)

Import this file into Make.com to explore or replicate the automation logic.

---

## Screenshots
See the [screenshots](/screenshots/scenario-2) folder for:
- Scenario routing logic
- Client status email samples
- Discord lifecycle notifications
  
