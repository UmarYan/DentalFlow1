DentalFlow V7.9.46 — Visits Search

Base:
- Built directly on the user-provided DentalFlow_V7.9.45_Treatment_Plan_Inline_Info_Fix.zip.
- V7.9.45 remains unchanged for rollback.

Changes:
- Added a compact search field to the Clinical Visits section.
- Searches visit patient name, linked patient name, visit date/time, visit IDs, complaint/reason, history, examination, diagnosis, treatment, prescription, advice, notes, and follow-up values.
- Shows the number of matching visits and a clear-search button.
- Search results retain the existing date groups, visit cards, inline details, patient profile action, and edit action.
- Added an accessible label and live result count.
- Updated the document version and Service Worker cache name.

Data safety:
- No LocalStorage keys, data structures, patient records, visit records, or clinical data were reset, migrated, or renamed.

Checks:
- ZIP integrity checked after packaging.
- HTML parser check.
- Inline JavaScript syntax check with Node.js.
- Service Worker syntax check with Node.js.
- Manifest JSON validation.
- Targeted source checks for search input, filtering, result count, clear action, and existing visit card actions.
- Browser/Android interaction testing was not performed.

Rollback:
- Redeploy the unchanged DentalFlow_V7.9.45_Treatment_Plan_Inline_Info_Fix.zip.


Version: V7.9.48
Change log:
- Visits list cards reuse the Patient Details Clinical Visits mini-card layout and Details/Edit actions.
- Billing list cards reuse the Patient Details Bills & Payments mini-card layout and Details/Edit/Payment/Receipt actions.
- Preserved visit search, billing search, billing summary metrics, and existing data structures.


V7.9.48 — Visits & Billing Card Parity
- Visits cards use Patient Details compact-card geometry, Patient Name as the title, visit details as content, and visible View/Edit icons. Existing date grouping and search are retained.
- Billing cards use compact card sizing and typography; Patient Name is the title and bill/date/paid/due amounts remain in the content. Existing billing/payment actions are retained.
- No older-version features were reintroduced; no data schema or LocalStorage keys were changed.
