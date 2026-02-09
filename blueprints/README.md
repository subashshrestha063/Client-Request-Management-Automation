# Make.com Scenario Blueprints

This folder contains exported **Make.com scenario blueprints** (`.json`) for the
automation system implemented in this repository.

Each JSON file represents a **complete, self-contained automation scenario**
and can be imported directly into **Make.com** for learning, testing, or
replication purposes.

These blueprints demonstrate real-world automation design patterns such as:

- Conditional routing
- State tracking
- Scheduled analytics
- Notification control

---

## 📦 Blueprint Mapping

| Blueprint File | Scenario |
|---------------|----------|
| [`scenario-1.json`](scenario-1.json) | Client Intake & Auto-Rejection |
| [`scenario-2.json`](scenario-2.json) | Client Status & Project Lifecycle Automation |
| [`scenario-3.json`](scenario-3.json) | Team Reminder for Pending Requests |
| [`scenario-4.json`](scenario-4.json) | Daily Service Demand Analytics |

Each blueprint directly corresponds to the documentation found in the
[`/scenarios`](../scenarios/) folder.

---

## 🚀 How to Import a Blueprint

1. Open **Make.com**
2. Click **Create a new scenario**
3. Select **More (⋮) → Import Blueprint**
4. Upload the desired `.json` file from this folder
5. Reconnect required services:
   - Google Sheets
   - Gmail
   - Discord (Webhooks or Bot)
6. Review module settings and adjust sheet names if needed

Once imported, the scenario can be run immediately after reconnection.

---

## ⚠️ Important Notes

- Blueprint connection IDs are **placeholders**
- You must manually reconnect:
  - Google Sheets
  - Gmail
  - Discord
- Google Sheet structure must match the templates described in:
  - Root `README.md`
  - Scenario-specific documentation

These blueprints are intended for:
- Learning and experimentation
- Portfolio demonstration
- Automation design reference

They are **not production-ready out of the box** without configuration.

---

## 📌 Recommendation

Before running a blueprint:
- Read the corresponding scenario documentation
- Review screenshots for expected outputs
- Verify sheet headers and column names

This ensures the automation behaves exactly as designed.
