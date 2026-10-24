DentalFlow V7.9.3 — Unified Patient Workflow

Stable base: DentalFlow_V7.9.2_Navigation_Data_Security.zip

Change log — V7.9.3
- Made Patient Workflow the single create/action entry point, with one FAB action.
- Routed new Patient, Clinical Visit, Follow-up, Appointment, Treatment Plan, Bill, Payment, Patient Record, and Reminder actions through Patient Workflow.
- Added editable existing-patient details inside an expandable section; new-patient details expand only when needed.
- Added collapsible treatment-plan entry with procedure, estimate, priority and status.
- Added appointment scheduling and linkage from an existing appointment or planned treatment.
- Added follow-up creation from a clinical visit or as a standalone patient follow-up, plus optional reminders and patient records.
- Added initial payment entry for a new bill and collection against an existing outstanding bill, with patient/bill matching and due-balance validation.
- Preserved existing edit paths for existing visits, plans, bills, appointments, follow-ups, reminders, records and payment corrections.
- Removed Tooth Chart, individual tooth/area selection/status UI, related visible fields, and active chart/context handlers. Legacy tooth-related data already stored in records is preserved for backward compatibility; no existing clinical data is deleted.
- Kept the `dentalflow_v2` LocalStorage key and existing patient, clinical, appointment, billing, payment and finance data structures.
- Bumped the service-worker cache to force the new version to be fetched after deployment.

Automated checks performed
- HTML parsing and duplicate-ID check.
- JavaScript syntax check for all inline script blocks and service worker.
- Manifest JSON validation.
- Static checks for Patient Workflow routing, payment balance validation, draft-control IDs and removal of tooth/area UI references.
- Node-based mocked workflow logic tests: full patient/visit/plan/bill/follow-up/reminder/record flow; patient-only registration; appointment scheduling and appointment-to-visit linkage; initial and existing-bill payments; overpayment rejection.
- ZIP integrity verification.

Browser end-to-end testing was attempted but did not complete in the available browser runtime. Do not treat the app as browser-tested until the deployment checklist has been run.

Deployment checklist
1. Export a DentalFlow backup before deployment.
2. Extract the ZIP and publish the contents of the DentalFlow folder to the existing GitHub Pages deployment.
3. Refresh/reopen the PWA so the updated service worker installs the new cache.
4. Test: create a patient; edit an existing patient; save a clinical visit; add a treatment plan; schedule an appointment; create a follow-up/reminder/record; create a bill with partial and full initial payment; collect a partial and full payment against an existing bill.
5. Confirm previous patient records, clinical history, appointments, bills, payment history and finance data remain intact.

Rollback
- Redeploy `DentalFlow_V7.9.2_Navigation_Data_Security.zip`.
- Export a backup first. Do not clear LocalStorage.
