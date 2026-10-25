DentalFlow V7.9.47 — Visits Card Design

Base:
- Built directly on the user-provided DentalFlow_V7.9.46_Visits_Search.zip.
- V7.9.45 remains available as the earlier stable rollback point; V7.9.46 is retained unchanged as the immediate previous version.

Changes:
- Restyled Clinical Visits cards to match the compact Treatment Plans list: matching compact height, border radius, spacing, typography, and right-aligned icon actions.
- Added a View (eye) icon and Edit (pencil) icon to every Visit card, including filtered search results.
- View opens the existing Clinical Visit Details sheet; Edit opens the existing central Patient Workflow editor for that visit.
- Preserved the Visits search field, matching count, clear button, date grouping, and searchable clinical fields.
- Tightened Advanced Search result card spacing and typography to align with the compact Treatment Plans visual style.
- Added View (eye) and Edit (pencil) icon buttons to every Advanced Search result card, routing through existing record detail and central edit actions.
- No LocalStorage keys, record structures, or clinical data migrations.
- Updated the document version and Service Worker cache name.

Checks performed:
- ZIP integrity checked after packaging.
- HTML parser check.
- Inline JavaScript syntax check with Node.js.
- Service Worker syntax check with Node.js.
- Manifest JSON validation.
- Targeted source checks for Visit search filtering, result count/clear control, View/Edit actions, and Treatment Plans-aligned card CSS.
- Browser/Android interaction testing was not performed.

Rollback:
- Redeploy the unchanged DentalFlow_V7.9.46_Visits_Search.zip.
