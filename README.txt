DentalFlow V7.9.45 — Treatment Plan Inline Info Fix

Development starting point: DentalFlow V7.9.43 — Treatment Plan Date Groups (explicitly authorized by the user for this update).
Official Stable Base remains: DentalFlow V7.9.39 — Treatment Plan Cards.

Changes in V7.9.45:
- Excluded More → Treatment Plans cards from the legacy global inline-info enhancement, preventing an unwanted left-side ⓘ button from being injected.
- Preserved the existing right-side Details (ⓘ), Edit, and Schedule actions and their handlers.
- Preserved patient-name-first cards, date-wise grouping, search, and existing plan rendering.
- Updated document version label and Service Worker cache name.

Data safety: No LocalStorage keys, data structures, patient records, or treatment-plan records were changed or migrated.

Verification performed for this build:
- ZIP integrity and required project files.
- HTML parsing and JavaScript syntax checks.
- Service Worker syntax and manifest JSON validation.
- Source inspection confirming the Treatment Plans exclusion is applied before legacy inline-details injection.
- File-level comparison against V7.9.43; only index.html, sw.js, and README.txt changed.
- Browser interaction testing was not performed.

Rollback: Redeploy the unchanged DentalFlow_V7.9.43_Treatment_Plan_Date_Groups.zip to restore the immediate prior build. The user's officially designated Stable Base remains DentalFlow_V7.9.39_Treatment_Plan_Cards.zip unless explicitly changed by the user.
