DentalFlow V7.9.48 — Patient Card Parity & Date-wise Billing

Stable base:
- Built directly on DentalFlow_V7.9.46_Visits_Search.zip.
- V7.9.46 remains unchanged and available for rollback.

Changes in V7.9.48:
- Visits cards now use the Patient Details mini-card structure, with Patient Name as the card title and Details/Edit actions.
- Billing cards now use the Patient Details mini-card structure, with Patient Name as the card title and relevant Details/Edit/Payment/Receipt actions.
- Billing records are grouped by date in collapsible groups; existing visit date grouping is preserved.
- Visit search, billing search, billing summary metrics, existing records, and data structures are preserved.
- Updated document version and Service Worker cache name.

Checks performed:
- HTML parser check.
- Inline JavaScript syntax check with Node.js.
- Service Worker syntax check with Node.js.
- Manifest JSON validation.
- ZIP integrity check.
- Browser/Android visual and interaction testing was not performed.

Rollback:
- Redeploy the unchanged DentalFlow_V7.9.46_Visits_Search.zip.
