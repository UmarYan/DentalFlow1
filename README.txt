DentalFlow V7.11.24 — Clinical Visit Editor Rebuild

Base: DentalFlow_V7.11.19_Patient_Visit_Entry_Section_Alignment.zip

Change log:
- Routed section Add/Edit entry points (Patient, Clinical Visit, Treatment Plan, Appointment/Arrival, Follow-up, Reminder/Task, Patient Record/Document and Billing) through Patient Visit Entry central workspace.
- Reworked central workspace record-edit binding to load the selected record synchronously after opening Patient Visit Entry, instead of relying on a zero-delay timer and additional delayed hydration patches.
- Clinical Visit Edit now maps existing visit field-name variants into the central editor, opens the Clinical Visit section and expands More clinical details so populated fields are visible.
- Add and Edit continue to use Patient Visit Entry central workspace; the existing central save path and record IDs/data schema are retained.
- Updated the service-worker cache identifier for V7.11.24.
- No intentional changes to unrelated features or stored data structures.

Validation performed:
- ZIP integrity check.
- JavaScript syntax check for every inline script and service worker.
- Static checks for section IDs, central edit routing, save routing and version/cache labels.
- Browser/Android runtime test was not available in this environment; actual local data edit/save behavior still requires post-deployment verification.

Post-deployment checklist:
1. Back up existing DentalFlow data before deploying.
2. Open an existing Clinical Visit from Visit Summary and from Patient Details; confirm fields are prefilled.
3. Change one field, save, reopen the same visit, and confirm the change persists without a duplicate visit.
4. Confirm patient identity and other clinical, appointment, treatment-plan and billing data remain unchanged.
5. Test Add Clinical Visit and one Add/Edit action in another section.

Rollback: redeploy DentalFlow_V7.11.19_Patient_Visit_Entry_Section_Alignment.zip.
