# Source Data Dictionary

| Table | Grain / record count | Main fields used | Role |
|---|---|---|---|
| Patients | One patient row / 500 | PatientID, Age, Gender, PrimaryPayerType, RiskCategory | Demographic and risk context |
| Providers | One provider row / 40 | ProviderID, Department, ProviderType, ProviderLocation | Staffing and utilization context |
| Encounters | One encounter row / 1,200 | EncounterID, PatientID, ProviderID, Department, EncounterDate, AppointmentStatus, EncounterType, WaitTimeMinutes, VisitDurationMinutes, SatisfactionScore, FollowUpRequired, DiagnosisCategory, FacilityLocation | Visits and patient experience |
| Claims | One claim row / 1,200 | ClaimID, EncounterID, PayerType, ClaimStatus, DenialReason, BilledAmount, ApprovedAmount, DeniedAmount, PendingAmount | Claims exposure |
| Payments | One payment row / 1,200 | PaymentID, ClaimID, EncounterID, PaymentStatus, CollectedAmount, PendingAmount, PaymentDate | Collections |

**Sensitive fields:** `PatientName`, `PatientID` and encounter/claim linkage keys appear in the raw source. The original workbook should not be released without an appropriate privacy assessment and legal authorization. The public department CSV contains only aggregation-level information.

**Relationship keys to inspect in Power BI:** Patients.PatientID ↔ Encounters.PatientID; Providers.ProviderID ↔ Encounters.ProviderID; Encounters.EncounterID ↔ Claims.EncounterID; Claims.ClaimID ↔ Payments.ClaimID. These are *logical key candidates*, not a verified claim about cardinality or active filter direction in PBIX.
