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


DentalFlow V7.11.15 — Patient Details Section Layout Match
Base: DentalFlow_V7.11.14_Visit_Summary_Toggle_Sections.zip.

Change log:
- Reordered Patient Details subsections to: Clinical Visits, Treatment Plans, Bills & Payments, Follow-ups, Appointments, Reminders, Documents & Records.
- Split the previous combined Appointments & Follow-ups subsection into two independent sections.
- Copied the Visit Summary subsection layout, spacing, heading typography, count badges, and triangular disclosure-toggle behavior to Patient Details.
- All subsections remain independently collapsible and collapsed by default.
- Preserved existing record rendering and actions, including the Add record action.
- No data schema or LocalStorage migration was introduced.

Validation performed for V7.11.15:
- JavaScript syntax check of all inline JavaScript blocks (Node.js).
- HTML script/style tag balance checks.
- ZIP integrity test.
- Browser/mobile runtime testing was not performed.

Post-deployment checklist:
1. Open a patient profile and confirm the seven subsection names and order.
2. Confirm the headings, count badges, spacing, and triangular toggle match Visit Summary.
3. Toggle each subsection independently and confirm its contents show/hide correctly.
4. Confirm visits, plans, bills/payments, follow-ups, appointments, reminders, and documents still open/edit as before.
5. Confirm existing patient data remains present.

Rollback: redeploy DentalFlow_V7.11.14_Visit_Summary_Toggle_Sections.zip. Keep an exported app-data backup before deployment; do not clear LocalStorage.


DentalFlow V7.11.16 — Android Back Navigation
Base: DentalFlow_V7.11.15_Patient_Details_Visit_Summary_Layout.zip.

Change log:
- Removed the in-page “← Patients” button from Patient Details.
- Removed the in-page “← Back to Visits” button from Visit Summary.
- Added browser-history-backed SPA navigation so Android system Back/browser Back returns to the previous DentalFlow view.
- Added fallback destinations (Patients for Patient Details, Visits for Visit Summary) if a Back event has no DentalFlow view state.
- Kept the Visit Summary Patient Profile action and all other page actions intact.
- Updated the service-worker cache version so deployed clients can fetch the new app shell.
- No patient data schema or LocalStorage migration was introduced.

Validation performed for V7.11.16:
- JavaScript syntax check of all inline JavaScript blocks and service worker (Node.js).
- HTML script/style tag balance checks.
- ZIP integrity test.
- Browser/mobile runtime testing was not performed.

Post-deployment checklist:
1. Open Patients, open a patient profile, and press Android Back; confirm it returns to Patients.
2. Open Visits, open a Visit Summary, and press Android Back; confirm it returns to Visits.
3. Open a profile/summary directly after a refresh and verify fallback behavior.
4. Confirm no top-left in-page back buttons remain on these two pages.
5. Confirm other view navigation and patient records still work.

Rollback: redeploy DentalFlow_V7.11.15_Patient_Details_Visit_Summary_Layout.zip. Do not clear LocalStorage; the update does not change stored data structures.


V7.11.17 hotfix: repaired printBill() inline-script boundary that caused JavaScript source text to appear at the bottom of the app. Retained V7.11.16 Android Back navigation changes.
