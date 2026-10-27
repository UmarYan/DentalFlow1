DentalFlow V7.11.4 — Patient Details Save & Collapse

Base: DentalFlow_V7.11.2_Patient_Visit_Entry_Focused_Editing.zip.

Change log:
- The Patient section header now shows the selected patient name on the right in both expanded and collapsed states.
- Removed the extra selected-patient row beneath the patient search field from the visible UI.
- Phone and Address now share one horizontal row.
- Medical alert and Important note are separate, side-by-side fields.
- Important note is saved and loaded as a backward-compatible patient property (`importantNote`); existing `medical` data remains intact.
- Added the new field to local workflow draft persistence and updated the service-worker cache identifier.
- No unrelated workflow sections or actions were intentionally changed.

Validation performed:
- JavaScript syntax check of all inline JavaScript blocks (Node.js).
- HTML script/style tag balance checks.
- ZIP integrity test.
- Browser/mobile runtime testing was not performed.

Post-deployment checklist:
1. Select an existing patient and confirm their name appears in the Patient section header while open and closed.
2. Confirm the extra selected-patient row is no longer visible.
3. Confirm Phone/Address and Medical alert/Important note appear side-by-side on mobile.
4. Save a patient with an Important note, reopen the workflow, and confirm it persists.
5. Confirm existing Medical alert values remain present and other workflow actions still work.


V7.11.4 changes: The Save patient details button retains its label without “only” and collapses Patient details / edit after a successful save. Medical alert and Important note are displayed on separate full-width rows.
