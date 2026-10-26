DentalFlow V7.10.9 — Individual Visit Central Workspace Completion

Base: DentalFlow_V7.10.7_Visit_Workspace_Render_Fix.zip (user-provided current version).

Change log:
- Added a “+ Investigation / Record” action to the Individual Visit Summary workspace.
- The action opens the existing unified workflow record section, preselects Investigation, and prefills the selected visit date and a visit-related title.
- Reuses the existing record workflow and data structure; no parallel record store or new LocalStorage schema was introduced.
- Updated the service-worker cache identifier to V7.10.9 so deployed clients can fetch the new app assets.
- Preserved existing visit, treatment-plan, billing, payment, follow-up, appointment, reminder, and linked-record rendering.

Validation performed:
- ZIP integrity test: passed.
- HTML script/style boundary counts: checked for balance.
- JavaScript syntax: checked for every inline script block with Node.js.
- Duplicate V7.10.7 source ZIPs were byte-size and content-layout equivalent; one was used as the base.
- Browser/Android runtime testing: not performed.

Manual QA still recommended:
1. Open Clinical Visits > View for a visit and confirm Visit Summary loads.
2. Click “+ Investigation / Record”; verify the unified workflow opens with Investigation selected and the visit date prefilled.
3. Save a record and confirm it appears only when linked to the selected visit.
4. Test existing Treatment Plan, Bill, Payment, Follow-up, Appointment, Reminder, and Edit actions.
5. Confirm the dashboard does not display JavaScript source as visible text.

Rollback: redeploy the original V7.10.7 ZIP. Do not clear browser storage or LocalStorage.


V7.10.10: Appointment and Follow-up create/edit forms now use their native standalone forms rather than Patient Workflow. Existing data structures and linked reminder updates are preserved.


V7.10.19 update: Appointment-to-Clinical-Visit and Treatment-Plan-item-to-Appointment actions now open their standalone forms rather than Patient Workflow. Runtime testing in Android/browser remains required. Patient Workflow has NOT yet been fully removed; other legacy entry/edit and draft-recovery paths may remain.


V7.10.22 — Direct Patient Profile Actions
- Routed Treatment Plan creation from the Patient Profile action dispatcher directly to the standalone Treatment Plan form.
- Added action aliases for record/investigation/document, clinical visit, treatment plan, follow-up, and billing.
- Unknown actions now show a clear message instead of silently opening Patient Workflow.
- Patient Workflow itself is not yet removed; remaining references require separate dependency audit and runtime testing.


V7.10.29 note: Patient Workflow UI remains retired. See LEGACY_WORKFLOW_AUDIT_V7.10.29.txt for the dependency audit and testing limitations.

V7.10.31: Added visible section-level Add buttons for Clinical Visits, Treatment Plans, Patient Records, Billing, Appointments, Follow-ups, and Reminders. Buttons route to existing standalone forms; no data schema or stored records were changed.
