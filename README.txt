DentalFlow V7.9.10 — Patient Autocomplete Workflow

Changes:
- Replaced visible patient dropdown with type-to-search autocomplete in Patient Workflow.
- Search by patient name, phone, or patient ID.
- Select an existing patient from live suggestions.
- If no exact name match exists, offer Add New Patient with the typed name prefilled.
- Retained the underlying patient select value, existing IDs, LocalStorage keys, and data schema for compatibility.
- No patient records are deleted or migrated.

Checks: HTML structure and JavaScript syntax checked; ZIP integrity checked after packaging. Real browser testing not performed.

DentalFlow V7.9.7 — Reference-Matched Workflow Section Layout

Stable base: DentalFlow_V7.9.2_Navigation_Data_Security.zip
Immediate source: DentalFlow_V7.9.6_Notion_Style_Workflow_Toggles.zip

Change log — V7.9.7
- Standardized Patient Workflow section cards to match the supplied screenshot: rounded bordered cards, compact spacing, left-side disclosure triangle, bold section title, and right-aligned muted helper text.
- Triangle points right when collapsed and down when expanded.
- Applied the same layout to nested workflow sections while preserving their existing details/summary behavior.
- Kept existing form fields, handlers, data structures, and LocalStorage key unchanged.
- Bumped the Service Worker cache name so deployed clients can fetch the updated UI.

Quality checks performed:
- HTML parser check
- Inline JavaScript syntax checks where Node.js is available
- Service Worker syntax check
- Manifest JSON parse
- ZIP integrity check

Not performed:
- Real browser/PWA interaction test
- Existing LocalStorage data regression test

Rollback:
- Redeploy DentalFlow_V7.9.2_Navigation_Data_Security.zip if a regression occurs.
- Export a backup before deployment; do not clear LocalStorage.


V7.9.12 — Inline Patient Matching
- Removed floating/shadowed patient suggestion popup styling. Matching patients and “Add new patient” render as a normal white list directly beneath the search field.
- Hid the separate always-visible New Patient button; the add-new action remains in the inline match list.
- Kept existing patient selection logic, storage keys, and record structures unchanged.
