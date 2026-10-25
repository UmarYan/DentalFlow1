DentalFlow V7.9.35 — Patient Record Cards: Essential Info

Change log:
- Treatment Plan cards show only plan title, status, completion count and estimate; full details remain under View.
- Billing cards show bill title, status, date, total, paid and due; payment details remain under View.
- Visit History cards show date/time and diagnosis/reason; full clinical details remain under View.
- View and Edit actions remain visible on each record card.
- Existing data keys and record structures are unchanged.

Previous rollback version: V7.9.34.
DentalFlow V7.9.28 — Compact Workflow Forms

Changes:
- Compactened the Treatment Plan editor: reduced field spacing, smaller quick-pick buttons, tighter item rows, and a more compact estimated-total area.
- Quick-pick procedures wrap neatly instead of forcing a horizontally clipped row.
- Compactened Patient Workflow section headers, fields, bill items and billing summaries.
- Advanced existing-bill collection and extra billing options start collapsed in a fresh workflow; open them when needed. Existing functionality remains available.
- Kept the existing plan, visit, billing and payment logic and LocalStorage structures unchanged.
- No intentionally removed features or data migrations.

Checks performed:
- ZIP integrity tested after packaging.
- HTML parser check performed.
- Inline JavaScript syntax checked with Node.js.
- Service Worker syntax checked with Node.js.
- Manifest JSON validated.
- Targeted checks verified compact CSS, quick-pick controls, plan item renderer and workflow billing controls remain present.
- Real browser/Android interaction testing was not performed.

Rollback:
- Redeploy DentalFlow_V7.9.27_Compact_Treatment_Plan_Cards.zip.


V7.9.29 — One-Line Treatment Entry
- Procedure, estimate, priority and status share one compact row on mobile.
- Planned-treatment rows use less height and a shorter bill action.
- No LocalStorage keys or existing record structures changed.


V7.9.30 — Compact UI Across Sections
- Applied consistent compact spacing to Patient, Visits, Billing, settings, summaries, forms, cards and expandable workflow sections.
- Reduced excess padding, gaps, field heights and card whitespace while preserving readable text and usable touch targets.
- Kept existing features, event handlers, LocalStorage keys and record structures unchanged; no data migration.

Checks performed for V7.9.30:
- ZIP integrity verified after packaging.
- HTML parser check performed.
- Inline JavaScript syntax checked with Node.js.
- Service Worker syntax checked with Node.js.
- Manifest JSON validated.
- Confirmed compact CSS override is present and version title updated.
- Real browser/Android interaction testing was not performed.

Rollback: redeploy DentalFlow_V7.9.29_OneLine_Treatment_Entry.zip.


Version 7.9.32 — Central Patient Workflow Editing
- Patient Details edit actions route into the central Patient Workflow.
- The selected record type is prefilled and its matching workflow section is opened while other sections remain collapsed.
- Central save updates the existing patient, visit, treatment plan, appointment, follow-up, reminder, record, bill, or payment record rather than creating a duplicate.
- Static validation: inline JavaScript syntax, service-worker syntax, manifest JSON, HTML parser, and ZIP integrity checked. Browser interaction testing was not performed.


Version 7.9.33 — Patient Workflow
- Restored the app/version label to the familiar name: Patient Workflow (no separate editing-oriented product name).
- Routed all legacy Edit Visit entry points to the central Patient Workflow editor, avoiding the standalone visit form.
- The selected visit's complaint, history, examination, diagnosis, treatment, prescription, advice and next-visit fields are loaded into the matching workflow fields; other workflow sections stay collapsed.
- Saving continues to update the selected visit by its existing ID, not create a new visit.
- Static validation performed after packaging: JavaScript syntax, HTML parsing, manifest JSON and ZIP integrity.
- Browser/Android interaction testing was not performed.

Rollback: redeploy DentalFlow_V7.9.32_Central_Patient_Workflow_Editing.zip.

V7.9.34 — Patient Workflow Compact Record Cards
- Made individual Treatment Plan, Bill/Payment, and Clinical Visit records inside Patient Details more compact, matching the existing compact appointment/follow-up/reminder/document row style.
- Added visible, consistently sized View and Edit icon actions to patient-detail clinical visits and bills; treatment-plan cards retain visible details/edit icons.
- Added visible View/Edit actions for individual payments in bill payment history.
- Edit actions continue routing to Central Patient Workflow for the selected existing record.
- No intentional changes to LocalStorage keys or record schemas.

Checks performed for V7.9.34:
- HTML parser check passed.
- All 13 inline JavaScript blocks passed Node.js syntax checks.
- Service Worker JavaScript syntax check passed.
- manifest.json parsed successfully.
- ZIP integrity checked after packaging.
- Existing duplicate IDs were detected in the source (appointments, clinicManagement, dfF_); not introduced intentionally by this update.
- Real browser/Android interaction testing was not performed.

Rollback:
- Redeploy DentalFlow_V7.9.33_Patient_Workflow_Visit_Edit_Fix.zip.
