DentalFlow V7.11.27 — Tooth-wise Treatment Tracking

Base: DentalFlow_V7.11.26_Compact_Detail_Rows.zip

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

- Added optional FDI tooth-number fields to Patient Visit Entry for Clinical Visit, each planned treatment item, and each bill line. Supports entries such as 37 and 46 without creating duplicate patient records.
- Tooth numbers are retained in workflow drafts, saved Treatment Plan items, visit records, and bill items; planned treatment can be added to the bill with its tooth number carried over.
- Tooth identifiers are displayed alongside planned treatment and bill lines and included in Treatment Plan search.
- Fixed linked Treatment Item progression so entering any treatment text during a visit no longer automatically marks the entire item Completed. A non-completed linked item moves to In progress; completion remains an explicit status decision.
- Preserved existing Lab Tracking module and existing local data schema; older records without tooth values continue to load with blank tooth identifiers.

- Static checks for tooth-wise fields, visit/item/bill mappings, status progression, and V7.11.27 version/cache labels.

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

Rollback: redeploy DentalFlow_V7.11.26_Compact_Detail_Rows.zip.

7. Add planned items for Tooth 37 and Tooth 46; verify tooth numbers persist after save/edit and appear on the plan card.
8. Add bill lines for Tooth 37 and Tooth 46; verify tooth numbers appear on bill details and survive editing.
9. Record a partial visit against a linked planned item; verify it becomes In progress, not Completed automatically.
