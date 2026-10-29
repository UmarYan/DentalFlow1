DentalFlow V7.11.20 — Central Workspace Add/Edit

Base: DentalFlow_V7.11.19_Patient_Visit_Entry_Section_Alignment.zip.

Change log:
- Routed Clinical Visit, Treatment Plan, Billing & Payment, Appointment/Arrival, Follow-up, Reminder/Task, Patient Record/Document, and Patient add/edit entry points through the central Patient Visit Entry workspace.
- Section-specific add actions open the relevant section; edit actions use the existing central section editor and existing save routines.
- Removed legacy standalone-form fallback behavior from these entry points by routing them directly to the central workspace.
- Preserved existing record IDs, data fields, LocalStorage keys, save logic, and unrelated workflows.
- Updated service-worker cache identifier to V7.11.20.

Validation performed:
- ZIP integrity test after packaging.
- JavaScript syntax checks for inline scripts and service worker.
- HTML tag balance checks for script/style and central section IDs.
- Static route checks for all requested add/edit entry points.
- Browser/mobile runtime testing was not performed.

Post-deployment checklist:
1. Open Patient Visit Entry and verify all eight sections appear in the expected order.
2. Add a clinical visit and confirm it saves once for the selected patient.
3. Edit an existing clinical visit and confirm the same visit is updated without creating a duplicate.
4. Try Add/Edit for Treatment Plan, Appointment, Follow-up, Billing, Reminder, and Patient Record; confirm each opens the corresponding central section/editor.
5. Confirm existing patient, clinical, appointment, payment, and billing data remain available after reload.
6. On Android, test Back navigation and reopening Patient Visit Entry.

Rollback:
- Redeploy the preserved base ZIP: DentalFlow_V7.11.19_Patient_Visit_Entry_Section_Alignment.zip.
- Because this update does not intentionally change data schemas or LocalStorage keys, rollback should not require a data migration. Keep a backup of clinic data before deployment as usual.
