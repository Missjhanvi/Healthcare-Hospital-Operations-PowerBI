# Healthcare Hospital Operations and Revenue Dashboard

A multi-page Power BI portfolio project that connects **hospital operations, service quality, follow-up workload, and revenue performance**.

## Project at a Glance

- **Tool:** Microsoft Power BI
- **Report pages:** 6
- **Visuals:** 59
- **Model tables:** 5
- **Named measures used:** 25
- **Primary analysis areas:** encounters, wait time, completion, cancellations, no-shows, satisfaction, follow-ups, billed revenue, approved revenue, collections, pending amounts, and denied amounts

## Dashboard Pages

| Page | Purpose |
|---|---|
| Hospital Operation Overview | Executive operational KPIs, departmental volume, wait time, cancellations, no-shows, and approved amount. |
| Hospital Operation - Quality and Follow-Up | Satisfaction risk, diagnosis follow-up workload, provider performance, visit duration, and patient risk. |
| Hospital Operation - Performance | Completion and no-show performance by encounter type, facility-level volume, and billed/pending revenue. |
| Revenue Overview | Billed, approved, collected, pending, and denied amounts with payer and denial analysis. |
| Revenue | Revenue risk by department, appointment status, facility, and follow-up workload. |
| Operational vs Financial Connection | Connects operational outcomes such as completion and no-shows with billed, approved, pending, and denied revenue. |

## Business Questions Answered

1. How many encounters were completed, cancelled, missed, or rescheduled?
2. Which departments and encounter types have the highest operational volume?
3. Where are wait times, cancellations, or no-shows creating operational risk?
4. Which diagnosis categories and patient risk groups generate the most follow-up workload?
5. How do provider activity, visit duration, and satisfaction relate to service delivery?
6. How much revenue is billed, approved, collected, pending, or denied?
7. Which payer types, denial reasons, facilities, and departments carry the highest financial risk?
8. How are operational outcomes connected to financial performance?

## Data Model

The report references the following model tables:

- `ClaimsTable`
- `EncountersTable`
- `PatientsTable`
- `PaymentsTable`
- `ProvidersTable`

The fields used in report visuals are documented in [`docs/Data_Dictionary.xlsx`](docs/Data_Dictionary.xlsx) and [`docs/DATA_DICTIONARY.md`](docs/DATA_DICTIONARY.md).

## Key KPI Groups

### Operational KPIs

- Total and completed encounters
- Cancellations, no-shows, and rescheduled visits
- Completion, cancellation, and no-show rates
- Average wait time and average visit duration
- Provider count
- Follow-up count and follow-up rate
- Average satisfaction score and satisfaction risk classification

### Financial KPIs

- Total billed amount
- Total approved amount
- Total collected amount
- Total pending amount
- Total denied amount
- Collected, pending, and denied amount rates
- Pending payment priority

## Tools and Techniques Demonstrated

- Power BI report design
- Data modeling across healthcare operational and financial tables
- DAX measures and KPI calculations
- Interactive slicers and filter context
- Combo charts, column charts, cards, and analytical tables
- Department, provider, payer, facility, diagnosis, encounter, and patient-risk segmentation
- Operational and financial performance storytelling

## Repository Structure

```text
Healthcare_Hospital_Operations_PowerBI_GitHub/
|-- Healthcare_Hospital_Operations_Dashboard.pbix
|-- README.md
|-- LICENSE
|-- .gitignore
|-- GITHUB_UPLOAD_GUIDE.md
|-- docs/
|   |-- PROJECT_DOCUMENTATION.pdf
|   |-- PROJECT_DOCUMENTATION.md
|   |-- DATA_DICTIONARY.md
|   |-- Data_Dictionary.xlsx
|   |-- DAX_MEASURE_CATALOG.md
|   |-- VISUAL_INVENTORY.csv
|   `-- RECOMMENDED_IMPROVEMENTS.md
|-- screenshots/
|   `-- README.md
`-- data/
    `-- README.md
```

## How to View the Dashboard

1. Download `Healthcare_Hospital_Operations_Dashboard.pbix`.
2. Open it in Power BI Desktop.
3. Review each report page and use the slicers to filter by department, encounter date, facility, or other available dimensions.

## Dashboard Preview

Add exported dashboard images to the `screenshots` folder before publishing. Recommended filenames are listed in [`screenshots/README.md`](screenshots/README.md).

## Privacy and Data Safety

**Do not make this repository public until you verify that the PBIX contains no protected health information, patient identifiers, employer-confidential data, credentials, or private connection details.**

This repository intentionally does not include a raw healthcare dataset. Only add synthetic, public, or properly de-identified sample data.

## Documentation

- [Full project documentation](docs/PROJECT_DOCUMENTATION.md)
- [PDF project summary](docs/PROJECT_DOCUMENTATION.pdf)
- [Data dictionary](docs/DATA_DICTIONARY.md)
- [DAX measure catalog](docs/DAX_MEASURE_CATALOG.md)
- [Visual inventory](docs/VISUAL_INVENTORY.csv)
- [Recommended dashboard improvements](docs/RECOMMENDED_IMPROVEMENTS.md)

## Author

**Jhanvi Patel**  
Data Analyst | Healthcare Analytics | Power BI | SQL | Python
