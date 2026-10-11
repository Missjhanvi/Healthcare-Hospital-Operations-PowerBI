# Case Study | Patient Access Meets Revenue Cycle

## Challenge
A healthcare operations and revenue case study was framed around 20 stakeholder business questions, including capacity, patient experience, follow-up workload, claims denials and collections. The practical objective was a decision-ready dashboard that makes operational and financial tradeoffs visible.

## Data scope
Five source tables: 500 patient records, 40 providers, 1,200 encounters, 1,200 claims and 1,200 payments. This is a supplied analytical exercise, not a validated live hospital production system.

## Executive findings
| Observation | Business interpretation | Suggested action |
|---|---|---|
| 889 of 1,200 encounters are completed (74.1%) | A substantial share is not completed within the source status distribution | Segment non-completion by department and appointment type |
| 120 no-shows (10.0%), 108 cancelled, 83 rescheduled | Patient access and schedule utilization warrant attention | Test reminders, confirmation and fast rebooking |
| Primary Care: 187 encounters; Emergency: 151; Cardiology: 142 | Workload is uneven | Review provider capacity together with wait time and completion |
| Cardiology: $12,663 pending; Primary Care: $11,820 | Receivables follow-up could be prioritized here | Drill into payer and claim aging before intervening |
| $30,651 denied versus $77,737 pending | Pending balances are larger than denied balances | Create separate workflows for adjudication backlog vs denials |
| Average wait: 20.9 minutes | A starting patient-experience benchmark | Track distribution and high-wait departments |
| 466 pending claims; 74 denied claims | Claims require status-specific follow-up | Review resolution timelines and denial causes |
| $284,664 collected from $465,896 billed | Collected is not equal to billed | Monitor collections and reconcile measure definitions |

## Analytical workflow
1. Inspect five raw sheets and identify entity-level grain and key identifiers.
2. Review Power BI's six pages and their existing visuals and metric references.
3. Recalculate selected headline indicators directly from source records to make the presentation auditable.
4. Link **observation → plausible business impact → proposed test/action**. Distinguish correlation from causation.
5. Publish only aggregated data and documentation while source privacy is evaluated.

## Caveats
- Full-workbook calculations use no slicers. Dashboard visual values depend on report filter context.
- Rates are operational definitions for this portfolio case study, not independently certified hospital KPIs.
- Revenue balance categories should not be added together indiscriminately or taken to mean realized write-offs.
- Any forecasted improvement, financial savings or real business deployment would require separate evidence.
