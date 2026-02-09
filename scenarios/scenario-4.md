# Scenario 4 – Daily Service Demand Analytics

## Purpose
This scenario generates **daily analytics** showing which services are most in demand.
It helps the business understand trends and make data-driven decisions.

Unlike order-based quantities, this scenario focuses on **request count** per service.

---

## Trigger
- Scheduled execution (once per day)

---

## Logic Overview
The scenario aggregates request data for the current day.

1. **Daily Filtering**
   - Filters rows by current date
   - Ensures only today’s data is processed

2. **Aggregation Logic**
   - Groups requests by service type
   - Counts number of requests per service

3. **Metric Structuring**
   - Uses a structured format:
     - Date
     - Metric
     - Label (Service Name)
     - Value (Count)

4. **Storage**
   - Aggregated results stored in Google Sheets
   - Enables historical trend analysis

---

## Output
- Daily service demand summary
- Service-wise request counts
- Clean dataset for reporting or dashboards

---

## Platform & Components
- Google Sheets (data source & analytics storage)
- Make.com (aggregation & scheduling)
- Make Data Stores (temporary aggregation handling)

---
## Blueprint

The Make.com blueprint for this scenario is available here:
- [blueprints/scenario-4.json](/blueprints/scenario-4.json)

Import this file into Make.com to explore or replicate the automation logic.

---

## Screenshots
See the [screenshots/scenario-4](/screenshots/scenario-4) folder for:
- Aggregation logic
- Daily analytics output
- Google Sheets summary view
