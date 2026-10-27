DentalFlow V7.11.5 — Balanced Patient Dashboard

Base: DentalFlow_V7.11.1_Patient_Workflow_Followup_Billing_Order.zip

Change log:
- Added direct Patient Details quick actions for Clinical Visit, Appointment, Bill, Follow-up and Call (when a phone number exists).
- Added a patient-history search that filters matching entries across the profile's existing sections.
- Added a Medical & Dental History section that surfaces the existing patient medical alert and relevant saved history/allergy records, with quick add/edit actions.
- Added a compact permanent-dentition FDI tooth-history chart (11–18, 21–28, 31–38, 41–48). Markers are derived only from existing tooth-linked visit, treatment-plan and bill records; selecting a tooth shows those linked records.
- Added an Add Clinical Visit action in the Clinical Visits section.
- Kept the existing Treatment Plans, Bills & Payments, Clinical Visits, Appointments & Follow-ups, Reminders & Tasks, and Records & Documents sections and their existing data/workflows.
- No new LocalStorage keys or required data migration. Existing patient/visit/plan/bill/payment/appointment/follow-up/reminder/record data structures are retained.
- Updated app title and service-worker cache identifier to V7.11.5.

Clinical/data notes:
- The tooth chart is a history-link navigator, not an editable diagnostic odontogram. A marker means a linked saved record exists; it does not assert the current clinical condition of the tooth.
- Records & Documents continues to use the app's existing patient-record workflow. Binary file attachment storage and communication-provider integrations were not added in this release.
- Patient data remains local to the device as in the base version. Keep regular backups and protect device access.

Validation performed:
- ZIP integrity check.
- Node.js syntax check of all 15 inline JavaScript blocks.
- JavaScript syntax check of the service worker.
- HTML parser checks for balanced script/style/details tags and basic HTML structure.
- Static checks of version/cache labels and the new Patient Details hooks.
- Attempted headless Chromium UI smoke test, but the browser process did not complete in this environment; browser/Android runtime interaction testing is therefore not claimed.

Deployment checklist:
1. Back up the current clinic data before replacing the app files.
2. Deploy the full ZIP contents together; do not mix files from different versions.
3. Open a known patient and check the quick actions, search, Medical & Dental History, tooth chart, and all existing profile sections.
4. Test creating a visit, appointment, bill, and follow-up on a test patient before routine use.
5. Confirm existing patient records and payment history remain available.

Rollback:
- Restore DentalFlow_V7.11.1_Patient_Workflow_Followup_Billing_Order.zip if required.
- Do not clear LocalStorage as part of rollback; preserve/export clinic data first.
