# KPI Definitions & Validation

| KPI | Calculation applied for source validation | Result |
|---|---|---:|
| Encounters | Count of rows in Encounters | 1,200 |
| Completed | Count AppointmentStatus = Completed | 889 |
| Completion rate | Completed / All encounters × 100 | 74.1% |
| No-show rate | AppointmentStatus = No-show / All encounters × 100 | 10.0% |
| Cancelled | Count AppointmentStatus = Cancelled | 108 |
| Rescheduled | Count AppointmentStatus = Rescheduled | 83 |
| Average wait | Arithmetic mean of numeric WaitTimeMinutes | 20.9 min |
| Billed amount | Sum Claims.BilledAmount | $465,896 |
| Approved amount | Sum Claims.ApprovedAmount | $362,401 |
| Denied amount | Sum Claims.DeniedAmount | $30,651 |
| Collected amount | Sum Payments.CollectedAmount | $284,664 |
| Pending amount | Sum Payments.PendingAmount | $77,737 |

**Reconciliation rule:** Avoid summing Claims billed measures alongside Payments billed measures; these tables represent related transactions. These numbers are sums across the source tables, not proof of precise DAX equivalence. Confirm the Power BI measure expressions, relationships and active filters before claiming a perfect match.
