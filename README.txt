DentalFlow V7.8.1 — Link-Free Simplified Build

Base archive: DentalFlow_V7.7.11_FAB_Search_Payment_Fixes.zip (designated V7.8.0 base).

Only link-related features were removed in this update:
- Diagnosis ↔ Treatment advanced linking.
- Clinical Visit ↔ Treatment Plan linking.
- Bill ↔ Visit / Treatment Plan linking.
- Reminder links to Visits, Treatment Plans and Bills.
- Linked-record summaries and navigation actions.

Existing standalone features retained: patients, clinical visits, examination, diagnosis, treatment, treatment plans, billing, payments, appointments, reminders, patient records, search, FAB, reports, backup and restore.

Legacy link fields are discarded during data normalization. The underlying patient, visit, plan, bill and reminder records remain independent. This ZIP contains app files only, not patient records.

Validation performed: inline JavaScript syntax check and ZIP integrity check. Interactive browser/device testing was not available in this environment. Before deploying, export a Safety Snapshot / JSON backup. Do not clear browser data during deployment.
