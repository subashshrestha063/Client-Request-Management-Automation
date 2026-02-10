# Scenario 1 – Client Intake & Auto-Rejection Automation

## Purpose
This scenario automates the **initial client intake process** for Prime Flow Solutions.
Its goal is to filter incoming requests, reject unrealistic leads automatically, and
store only valid requests for further processing.

This ensures the team does not waste time reviewing low-quality or non-viable requests.

---

## Trigger
- Google Form submission (new client request)
- Check Out Google form -> <a href ="https://docs.google.com/forms/d/e/1FAIpQLSfLnTBoo9y-MudFf1r0ImeoAzTGrTDl0ogmbiWmIVKH2doDlA/viewform?usp=header">Prime Flow Solutions</a>

---

## Logic Overview
When a client submits a request, the scenario performs a series of validations:

1. **Data Capture**
   - Captures client name, email, service required, budget, deadline, and project description.

2. **Validation Rules**
   - Budget below minimum threshold → Auto-reject
   - Deadline too short → Auto-reject
   - Invalid or unsupported service → Auto-reject

3. **Conditional Routing**
   - Valid requests are stored in Google Sheets.
   - Invalid requests trigger an automated rejection email.

4. **State Tracking**
   - Initial status is set to `New`
   - Timestamp is recorded for lifecycle tracking

   ---

### Scenario Design
<img src="/screenshots/scenario-1/Flow_scenario-1.png" width="850">



## Output
- Accepted requests stored in Google Sheets
- Automatic rejection emails sent to invalid leads
- Clean, filtered client intake pipeline

---
## Discord Notifcations

## New Request
<img src="/screenshots/scenario-1/new_request_discord_alert.png" width="600">

## Auto-Rejected (Low Budget )
<img src="/screenshots/scenario-1/autorejected_discord_alert.png" width="600">

## Email Notifcations

## New Request
<img src="/screenshots/scenario-1/new_request_email_alert.png" width="600">

## Auto-Rejected (Low Budget )
<img src="/screenshots/scenario-1/auto_rejected_email_alert.png" width="600">

## Duplicate Email (Already Registerd)
<img src="/screenshots/scenario-1/duplicate_email_alert.png" width="600">

## Platform & Components
- Google Forms (client submission)
- Make.com (validation & routing)
- Google Sheets (request storage)
- Gmail (auto-rejection emails)

---
## Blueprint

The Make.com blueprint for this scenario is available here:
- [View Blueprint ](/blueprints/scenario-1.json)

Import this file into Make.com to explore or replicate the automation logic.

---

## Screenshots
See the [Screenshots](/screenshots/scenario-1) for:
- Scenario flow design
- Auto-rejection email sample
- Google Sheets data entry
