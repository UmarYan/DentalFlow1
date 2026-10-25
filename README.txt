DentalFlow V7.9.24 - Simplified Patient Workflow

Changes:
- Combined the Patient Workflow existing-records directory label with Visit History so previous visits and other saved records are found in one expandable section.
- The combined section continues to manage visits, patient records, treatment plans, appointments, follow-ups, reminders, bills and payments using their existing record structures.
- Removed the separate Timeline accordion from the patient profile to reduce duplication. Underlying timeline data and records are not deleted; only the separate UI entry was removed.
- Preserved other workflow sections, visit-time alignment, Clinic Management Finance/Inventory/Lab Tracking tabs, and LocalStorage structures.

Base: DentalFlow V7.9.23 - Visit Time & Aligned Management Tabs.

Checks performed: ZIP integrity, HTML parsing, inline JavaScript syntax, service worker syntax, manifest JSON parsing, and targeted UI assertions. Real browser/mobile testing and existing LocalStorage regression testing were not performed.

Rollback: redeploy DentalFlow V7.9.23 if needed. Do not clear LocalStorage.
