DentalFlow V7.11.6 — Clinical Visit Treatment Plan Link

Base: DentalFlow_V7.11.4_Workflow_Links_Final.zip.

Change log:
- Moved the existing Follow-up section to immediately after Treatment plan and before Billing & payment.
- All section contents and other UI areas remain unchanged.
- No data schema or LocalStorage changes.
- Updated the app version and service-worker cache identifier to V7.11.1.

Validation performed:
- JavaScript syntax check of all inline JavaScript blocks (Node.js).
- HTML script/style/details tag balance checks.
- Confirmed requested Patient Workflow section order.
- ZIP integrity test.
- Browser/UI runtime testing was not performed.

Post-deployment checklist:
1. Open Patient Workflow and confirm Follow-up appears directly after Treatment plan and before Billing & payment.
2. Expand Follow-up and Billing & payment and verify their fields and interactions.
3. Confirm Patient record / document and Reminder / task remain after Billing & payment.
4. Confirm the history button, draft note, Discard draft, and Save & Finish remain unchanged.
5. Test with an existing patient; confirm existing records remain intact.

Rollback:
Redeploy DentalFlow_V7.11.0_Patient_Workflow_Section_Order.zip. Do not clear LocalStorage.

Version 7.11.2 change log
- Link clinical visits to their selected treatment-plan item even when no appointment record is used; preserve existing status and data behavior.

Version 7.11.3 change log
- Carry treatment-plan item identity into bill items and prevent duplicate plan-to-bill additions while retaining legacy name/fee fallback.

Version 7.11.4 change log
- Final cumulative workflow update: visit-plan item linkage, identity-based plan-to-billing deduplication, and follow-up-linked reminder/task creation.


V7.11.6 change log
- Added optional link from a Clinical Visit to one existing Treatment Plan item for the selected patient.
- Added explicit status choice (no change / In progress / Completed); status is never inferred from free-text treatment notes.
- Visit and plan keep reciprocal linked IDs. Existing unrelated sections and stored record structures are preserved.


V7.11.7 change log
- Follow-up saves/status changes now reuse existing workflow-created reminders by followupId instead of creating a second linked reminder.
- Linked reminder dates, times, patient details, and source references stay synchronized when a follow-up is edited.
- Completed/cancelled follow-ups update the linked task state without deleting historical reminder records.
- Preserved independent additional reminders/tasks and unrelated sections.
- Updated service-worker cache identifier to V7.11.7.

Validation for V7.11.7
- ZIP integrity, inline JavaScript syntax, service-worker syntax, JSON manifest, and HTML tag balance checked.
- Browser runtime/UI freezing tests were not performed.


V7.11.8 change log
- Extended the read-only Data Check report to include lab patient references, duplicate lab-expense links, inventory quantity/ID consistency, and Finance expense ID/amount consistency.
Validation: ZIP integrity, JavaScript syntax, HTML tag balance, manifest JSON and targeted static/smoke checks performed for this version. Browser/Android runtime testing was not performed.


V7.11.9 change log
- Lab-to-Finance synchronization now consolidates duplicate expense records linked to the same lab case before updating the canonical expense, reducing duplicate expense totals.
Validation: ZIP integrity, JavaScript syntax, HTML tag balance, manifest JSON and targeted static/smoke checks performed for this version. Browser/Android runtime testing was not performed.


V7.11.10 change log
- Stock-out movements now record an estimated consumption value using quantity × stored unit cost when no explicit loss/consumption value is entered; this is a cost estimate only and does not create a cash expense.
Validation: ZIP integrity, JavaScript syntax, HTML tag balance, manifest JSON and targeted static/smoke checks performed for this version. Browser/Android runtime testing was not performed.


V7.11.11 change log
- Safety Snapshot now checks the storage save result, rolls back the in-memory snapshot list on failure, and never reports success when persistence failed.
Validation: ZIP integrity, JavaScript syntax, HTML tag balance, manifest JSON and targeted static/smoke checks performed for this version. Browser/Android runtime testing was not performed.


V7.11.12 change log
- Final cumulative release: JSON backup metadata reflects the current app version; includes prior workflow data checks, lab-finance duplicate consolidation, material consumption costing, and safer snapshot persistence.
Validation: ZIP integrity, JavaScript syntax, HTML tag balance, manifest JSON and targeted static/smoke checks performed for this version. Browser/Android runtime testing was not performed.

V7.11.12 final release checklist
1. Run Backup & Data Safety > Run data check and review all reported counters.
2. Create a safety snapshot and export an external JSON backup before importing or restoring data.
3. Create/edit a lab case with cost and account; confirm one linked Laboratory expense and correct account balance.
4. Stock out a material without entering a cost; confirm the movement records quantity × unit cost as estimated consumption cost, without creating a cash expense.
5. Import/restore only a trusted backup after reviewing the confirmation and keep an external copy of the current data.
6. Test patient, appointment, clinical visit, treatment plan, follow-up, reminder, billing and payments on a test patient.
7. Deploy to a test GitHub Pages URL and verify install/offline behavior before replacing the live version.

Rollback: redeploy DentalFlow_V7.11.7_Followup_Reminder_Task_Link.zip (or the immediately previous known-good version). Do not clear LocalStorage.
Runtime limitation: Android/browser runtime tests were not available during this build; deploy to a test URL and complete the checklist before live use.
