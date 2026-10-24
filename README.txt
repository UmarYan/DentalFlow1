DentalFlow V7.10.0 — Unified Patient Workflow

Base: DentalFlow V7.9.1 — Clinic Management Tabs (the explicitly selected stable base).

Changes in V7.10.0:
- Reorganized the unified Patient Workflow into a compact ordered journey: Patient → Appointment & Arrival → Clinical Visit → Treatment Plan → Follow-up → Billing & Payment → Visit Completion.
- Added an optional planned-treatment entry linked to the patient and, when present, the clinical visit; planned treatment remains separate from treatment performed and billing.
- Added Existing Appointment and Follow-up Visit entry types alongside Walk-in and Schedule a New Appointment. Existing appointments can be selected for the chosen patient.
- Added a compact step indicator, clearer section labels, mobile-first spacing, and Continue Later / Save & Finish actions. Existing local draft autosave remains in place.
- Main menu order: Home, Patients, Visits, Advanced Search, Clinical Workflow, Billing & Payments, Clinic Management, Reports, Settings.
- Grouped Data Safety, Backup Data, and Restore Data under Data & Security; Data Safety remains outside Settings.
- More contains only Clinical Workflow, Clinic Management, Treatment Plans, Reports, Backup Data, and Restore Data.
- Renamed the footer Finance label to Billing.
- Preserved the existing LocalStorage key and record collections; no data reset or migration is performed.

Deployment:
1. Export a DentalFlow JSON backup before deployment.
2. Extract the ZIP and publish the contents of the DentalFlow folder to the existing GitHub Pages deployment.
3. Reload the PWA and check navigation, patient workflow, and existing records.

Rollback:
- Redeploy DentalFlow_V7.9.1_Clinic_Management_Tabs.zip.
- Export a backup first; do not clear LocalStorage.
