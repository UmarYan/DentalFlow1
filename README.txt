DentalFlow V7.9.46 — Explicit Info Opt-In

Development starting point: V7.9.44 — Clinical Visits Search.
Change log:
- Changed global Info button auto-insertion to require explicit data-df-global-info="true" opt-in.
- Explicitly opted in appointment, follow-up, and reminder cards that previously relied on global insertion.
- Kept inline-details pane setup and existing manually rendered Info actions intact.
- No LocalStorage keys, patient records, clinical data structures, or unrelated workflows intentionally changed.

Verification: ZIP integrity, HTML parsing, JavaScript syntax, Service Worker syntax, manifest JSON, and base comparison checked. Browser interaction testing not performed.

DentalFlow V7.9.44 — Clinical Visits Search

Stable base: DentalFlow_V7.9.39_Treatment_Plan_Cards.zip (user-designated stable base).
Changes:
- Added a compact search field to More/Clinical Visits, matching the search pattern used in other list sections.
- Search filters visit cards by patient name/phone/ID, visit ID/date/time, chief complaint/reason, examination, treatment performed, diagnosis, notes, follow-up, and procedure text where available.
- Date grouping, visit ordering, card actions, records, LocalStorage keys, and existing data structures are preserved.

Checks performed: ZIP integrity, required files, HTML parse, inline JavaScript syntax, Service Worker syntax, manifest JSON, and source-level search-hook checks. Browser interaction testing was not performed.

Rollback: redeploy the unchanged user-designated DentalFlow_V7.9.39_Treatment_Plan_Cards.zip.

--- Previous release notes ---

DentalFlow V7.9.39 — Treatment Plan List Cards

Stable base: DentalFlow_V7.9.38_Global_Action_Icons_Fix.zip (user-designated stable base).
Changes:
- Restored/implemented the More → Treatment Plans destination as a working all-patient treatment-plan list (the base linked to a `plans` view but had no matching section).
- Treatment plan cards reuse the compact Visits card geometry and typography, with Patient Details-style Details, Edit, and Schedule icons where applicable.
- Added search across plan title/status/notes, patient identity, and treatment-item details.
- Existing treatment-plan records, handlers, LocalStorage keys, and data structures are preserved; no migration or data reset added.
- Updated the document version label and Service Worker cache name.

Checks planned/performed are reported in the delivery note; browser interaction testing was not performed.

Rollback: redeploy the unchanged DentalFlow_V7.9.38_Global_Action_Icons_Fix.zip.

--- Previous release notes ---

DentalFlow V7.9.38 — Global Action Icons Fix

Stable base: V7.9.33 — Patient Workflow Visit Edit Fix ZIP supplied for this task.
Changes:
- Fixed the global .df-action-icon CSS rule that set font-size:0!important, hiding text-glyph Details/Edit/action icons throughout the app.
- Global action buttons now allow visible text glyphs while retaining their existing icon SVG styling.
- Kept patient profile compact card styling and the agreed section names: Treatment Plans, Bills & Payments, Clinical Visits.
- No data schema or LocalStorage keys intentionally changed.
- Updated Service Worker cache name.

Previous release notes retained below:

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
