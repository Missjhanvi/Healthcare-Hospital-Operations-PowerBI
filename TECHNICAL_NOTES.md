# Technical Review & Report Architecture

## Confirmed report pages (read from PBIX report layout)
1. **Hospital Operation Overview** — appointment-status KPI cards, department workload, wait time, cancellation and filtering.
2. **Hospital Operation** — satisfaction, follow-up workload, provider utilization, patient risk and supporting metrics.
3. **Hospital Operation** — encounter-type comparison, facility/payer context and supporting KPIs.
4. **Revenue Overview** — billed/approved/collected/pending/denied amounts, payer/claim categories, denial reasons and prioritization.
5. **Revenue** — department revenue comparisons, pending amount/follow-up and date/facility/department slicers.
6. **Operational Vs Financial Connection** — comparisons of completion/no-show, billed amount, department pending balance and follow-up.

## Technical QA to perform in Power BI Desktop
- Rename the two similarly titled *Hospital Operation* pages to descriptive names.
- Verify all relationship direction/cardinality, especially Claims ↔ Payments and departmental filter propagation.
- For each measure, record its exact DAX expression and denominator; check blanks and drill-down filter behavior.
- Check collection/denial/pending *amount rates* for expected definitions and consistent numerator/denominator.
- Confirm missing date values in Payments do not distort time trends.
- Correct chart titles and typo **Revenue Risk In Deapermnt**.
- Use currency for dollar measures, percentages for rates and counts for visit KPIs.
- Test department, facility and date slicers against matrix/detail output.

## Limitations
A PBIX report layout was inspectable and a source-data audit was conducted; this package does not claim execution or exhaustive validation of every DAX measure inside Power BI Desktop.
