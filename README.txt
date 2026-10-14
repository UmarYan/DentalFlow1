DentalFlow V7.8.5 — Workflow Reliability Check

Base: DentalFlow V7.8.4 Save Verification & Data Safety.

Changes in this build:
- Expands the non-destructive Data Check to report records missing IDs and duplicate IDs.
- Checks patient references only when a record contains a patient ID, avoiding false alarms for intentionally unassigned records.
- Checks existing internal references between visits, appointments, bills, reminders, and treatment plans.
- Checks bill item and payment amounts for invalid or negative values.
- The check reports issues but does not automatically edit, delete, or repair clinic records.
- Keeps the existing continuous workflow, draft recovery, save verification, backup import/export, safety snapshots, and clinic sections.
- Updates the app title and service-worker cache version.

Important limits:
- This app stores data locally on this device; JSON export is an external backup, not cloud sync.
- A clean data check is not a guarantee that all clinical/financial data is correct. Review any warnings before making changes.
- JavaScript syntax and ZIP integrity checks are performed for this package. Physical Android end-to-end testing, real patient data migration, and backup/restore acceptance testing remain to be done.
- Test with a fictional patient first. Export a JSON backup before replacing deployed files. Do not clear Chrome site data.
- If a save warning appears, do not reload/close the app until you have exported what you can and resolved the storage issue.
