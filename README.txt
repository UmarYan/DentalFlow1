DentalFlow V7.10.1 — Patient Workflow Central Workspace

Base: DentalFlow_V7.10.0_Billing_TreatmentPlans_RightRail.zip (the exact stable base specified by the user).

Change log:
- Patient-related record edits continue through the central Patient Workflow overlay for patient, visit, treatment plan, billing, appointment, follow-up, reminder, record/document, and payment edit routes already supported by the base.
- Before opening the central editor, any other open form/detail overlay is dismissed to prevent stacked dialogs and keep the Patient Workflow editor as the single foreground workspace.
- Added dialog accessibility semantics (role=dialog, aria-modal=true, labelled title) to Patient Workflow overlay.
- Saving a central edit returns to the patient profile/workspace for the same patient; closing without saving leaves the underlying view in place.
- Preserved V7.10.0 visual design, including Billing/Treatment Plan right-rail status and horizontal action icons.
- No data schema, LocalStorage keys, patient records, or clinical records were intentionally changed.
- Updated service-worker cache identifier for V7.10.1.

Validation performed:
- JavaScript syntax check for all 14 inline scripts using Node.js: passed (0 syntax errors).
- HTML script/style tag balance: passed (14/14 script tags; 44/44 style tags).
- ZIP integrity: passed (all archive members tested).
- Browser/UI testing: not performed in this environment.

Post-deployment checklist:
1. From Patients, Visits, Billing, Treatment Plans, and Clinical Workflow, open a patient-related edit action and confirm Patient Workflow appears as the single foreground overlay.
2. Confirm another detail/form overlay is not left stacked behind or in front.
3. Close without saving and confirm the original underlying view remains.
4. Save an edit and confirm the same patient's profile/workspace is shown with updated data.
5. Test visit, plan, bill, payment, appointment, follow-up, reminder, and patient-record editing.
6. Verify search, date-wise grouping, and existing patient data.

Rollback:
Redeploy DentalFlow_V7.10.0_Billing_TreatmentPlans_RightRail.zip. Do not clear LocalStorage.
