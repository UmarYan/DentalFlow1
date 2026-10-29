DentalFlow V7.11.26 — Compact Detail Rows

Base: DentalFlow_V7.11.25_Smart_Draft_Recovery.zip

Change log:
- Updated Clinical Visit, Follow-up/Reminder, Bill/Payment and other context-detail popup fields to a compact horizontal label/value row layout with consistent alignment and subtle dividers.
- Long values and multiline items wrap naturally; responsive sizing is applied on narrow mobile screens. Detail popup actions and underlying data/edit behavior are unchanged.
- Routed section Add/Edit entry points (Patient, Clinical Visit, Treatment Plan, Appointment/Arrival, Follow-up, Reminder/Task, Patient Record/Document and Billing) through Patient Visit Entry central workspace.
- Reworked central workspace record-edit binding to load the selected record synchronously after opening Patient Visit Entry, instead of relying on a zero-delay timer and additional delayed hydration patches.
- Clinical Visit Edit now maps existing visit field-name variants into the central editor, opens the Clinical Visit section and expands More clinical details so populated fields are visible.
- Add and Edit continue to use Patient Visit Entry central workspace; the existing central save path and record IDs/data schema are retained.
- Replaced the repeated global “Resume draft?” popup with a non-blocking Unfinished Work dashboard card.
- Added support for multiple saved Patient Workflow drafts, each with Resume and Discard actions.
- Draft cards identify the patient (when known), task/edit type and last-saved time.
- Drafts are kept separate so starting work for another patient does not overwrite an earlier unfinished workflow.
- Legacy single-draft storage is imported into the new draft list when encountered; core patient/clinical/billing data schema is unchanged.
- Updated the service-worker cache identifier for V7.11.26.

Validation performed:
- ZIP integrity check.
- JavaScript syntax check for every inline script and service worker.
- Static checks for compact detail-row styles and V7.11.26 version/cache labels.

Validation performed (inherited from base):
- ZIP integrity check.
- JavaScript syntax check for every inline script and service worker.
- Static checks for draft recovery routes, dashboard card IDs, legacy migration, central edit routing, save routing and version/cache labels.
- Browser/Android runtime test was not available in this environment; actual local data edit/save behavior still requires post-deployment verification.

Post-deployment checklist:
1. Back up existing DentalFlow data before deploying.
2. Start a workflow, enter a few fields, then leave it unfinished; confirm an Unfinished Work card appears on Home.
3. Start a different patient workflow; confirm no resume popup appears and the first draft remains available.
4. Resume each draft and confirm the correct patient and entered fields are restored.
5. Discard one draft and confirm other drafts and saved patient records remain intact.
6. Test editing and saving an existing Clinical Visit; confirm it updates the same record without creating a duplicate.

Rollback: redeploy DentalFlow_V7.11.25_Smart_Draft_Recovery.zip.
