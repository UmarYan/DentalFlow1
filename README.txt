DentalFlow V7.8.66 — Simple Laboratory Tracking

Base: DentalFlow V7.8.65 Finance & Inventory Usability.

Changes in V7.8.66:
- Added a simple Laboratory Tracking workspace for crown, bridge, denture, inlay/onlay, night guard and other lab cases.
- Each case links to an existing patient and records work type, tooth/area, laboratory, sent date, expected return date, lab cost, status and optional note.
- Added compact status summaries for In progress, Ready to fit and Overdue, plus search and status filters.
- Added quick status actions: Mark sent, Received and Mark fitted. Cases can be edited; Cancelled status is available instead of deleting history.
- Overdue is shown when a case is marked Sent to lab and its expected return date has passed.
- Laboratory data is stored in the existing DentalFlow data object, included in normal backup/restore, and normalized without changing existing patient, clinical, appointment, billing, finance or inventory records.
- No external dependencies added.

Deployment: Extract the ZIP and publish the contents of the DentalFlow folder to the existing GitHub Pages deployment.
Rollback: Redeploy the previous V7.8.65 ZIP (or the designated V7.8.63 stable base if required). Export a backup first and do not clear LocalStorage. Lab records created in this version may not appear in older versions.

Validation performed: JavaScript syntax checks, HTML parsing, duplicate-ID scan, manifest JSON parsing, service-worker syntax, ZIP integrity, required-file checks and static laboratory-handler checks. Browser end-to-end testing was not performed.
