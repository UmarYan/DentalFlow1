DentalFlow V7.9.43 — Treatment Plan Date Groups

Stable base: DentalFlow_V7.9.39_Treatment_Plan_Cards.zip (explicitly designated by the user).

Changes in V7.9.43:
- Categorized More → Treatment Plans cards by plan creation date, following the existing Visits date-group pattern: Today, Future-dated Plans, Recent Plans (last 7 days), and Older Plans.
- Kept the patient-name-first card presentation, plan title/status/item summary, and right-side Details, Edit, and Schedule actions.
- Search results are grouped by the same date categories; date grouping is presentation-only and does not modify stored records.
- Updated the document version label and Service Worker cache name.

Data safety: No LocalStorage keys, data structures, patient records, or treatment-plan records were migrated, reset, or deleted.

Verification: ZIP integrity, HTML parsing, inline JavaScript syntax, Service Worker syntax, manifest JSON, required files, and base-file comparison checked before delivery. Browser interaction testing was not performed.

Rollback: Redeploy the unchanged DentalFlow_V7.9.39_Treatment_Plan_Cards.zip.
