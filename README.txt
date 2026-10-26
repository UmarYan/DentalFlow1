DentalFlow V7.9.52 — Startup Recovery Fix

Base:
- Built from the current provided V7.9.51 artifact.
- Keep V7.9.47 as the declared stable base/rollback reference unless the user explicitly changes it.

Changes:
- Removed the write-to-LocalStorage call from the Billing list render path; rendering/searching the list should not save or mutate data.
- Retained the date-wise collapsible grouping in Visits and Billing.
- Retained Patient Name card titles and existing View/Edit/Payment/Receipt actions.
- Updated Service Worker cache name to force the new app shell to load.

Validation:
- ZIP integrity and HTML script syntax checks performed.
- Browser testing was not performed; confirm startup and stored-data access after deployment.

Rollback:
- Redeploy the previously working ZIP if any regression occurs. Do not clear browser storage.
