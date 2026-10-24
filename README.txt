DentalFlow V7.9.5 — Collapsible Patient Workflow

Stable base: DentalFlow_V7.9.2_Navigation_Data_Security.zip

Change log — V7.9.5
Inherited from V7.9.3 Unified Patient Workflow:
- Patient Workflow remains the central creation entry point for patients, clinical visits, follow-ups, appointments, treatment plans, bills, payments, patient records and reminders.
- Existing Tooth Chart / individual tooth-area UI cleanup and legacy-data preservation are retained from the supplied base.
- The `dentalflow_v2` LocalStorage key and existing patient, clinical, appointment, billing, payment and finance schemas are preserved.

V7.9.4 — Central Edit Workspace:
- Added an expandable Existing Records & Payments directory inside Patient Workflow.
- Added record-type filtering and text search across patients, clinical visits, treatment plans, appointments, follow-ups, reminders, patient records, bills and nested payment records.
- Added central Edit actions that open the matching ID-based editor while leaving Patient Workflow available underneath.
- Added a dedicated “Save patient details only” action so patient-only edits/registration do not accidentally create a visit, bill or other record.
- Added the missing `openPaymentEditForm` entry point and populated the payment correction form from the selected historical payment.
- Historical payment corrections continue to use the existing correction-history mechanism and bill balance validation.
- Bumped the service-worker cache name so the deployed PWA can fetch the new version.
- No LocalStorage migration, reset, or destructive record cleanup was performed.

Automated checks performed for V7.9.4:
- HTML parsing: PASS.
- Actual HTML element duplicate-ID check: PASS (none found).
- JavaScript syntax: PASS for all 13 script blocks.
- Manifest JSON validation: PASS.
- Static presence checks for the central edit directory, patient-only save action, payment edit handler, and existing LocalStorage key: PASS.
- ZIP integrity: checked before delivery.

Not performed:
- Browser end-to-end testing, live UI interaction testing, and real LocalStorage data regression testing. The deployment checklist below must be run before treating this version as stable.

Deployment checklist
1. Export a DentalFlow backup before deployment.
2. Extract the ZIP and publish the contents of the DentalFlow folder to the existing GitHub Pages deployment.
3. Refresh/reopen the PWA so the updated service worker installs the new cache.
4. Test: open Patient Workflow → Existing records & payments; search/filter a saved record; edit patient, visit, plan, appointment, follow-up, reminder, patient record, bill and historical payment; confirm payment correction history and balance calculations. Then create a patient; edit an existing patient; save a clinical visit; add a treatment plan; schedule an appointment; create a follow-up/reminder/record; create a bill with partial and full initial payment; collect a partial and full payment against an existing bill.
5. Confirm previous patient records, clinical history, appointments, bills, payment history and finance data remain intact.

Rollback
- Redeploy `DentalFlow_V7.9.2_Navigation_Data_Security.zip`.
- Export a backup first. Do not clear LocalStorage.


V7.9.5 — Collapsible Patient Workflow:
- Added consistent compact accordion sections for Patient, Appointment/Arrival, Clinical Visit, Follow-up, Billing & Payment, and existing record management.
- Kept Patient and Clinical Visit sections expanded by default; optional/longer sections start collapsed to reduce visual clutter and scrolling.
- Standardized compact section spacing, keyboard focus indication, chevron state, and reduced-motion behavior.
- Preserved existing record/payment edit flows, field IDs, LocalStorage keys and data schemas.
- Updated the service-worker cache name to dentalflow-v795-collapsible-patient-workflow.

Automated checks performed for V7.9.5:
- Python HTML parser integrity check: PASS; no duplicate HTML IDs found.
- JavaScript syntax checks: PASS for all 13 inline script blocks and the Service Worker.
- ZIP integrity: PASS after packaging.
- Browser end-to-end tests: not performed.
