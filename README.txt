DentalFlow V7.8.50 — Vertical Workflow Inline Expansion

Changes in this version (based on the current V7.8.49 build):
- Today's Workflow cards are stacked vertically in this order: Appointments, Queue, Follow-ups, Reminders.
- Tapping a card header expands/collapses its list inline on the Home screen; it no longer navigates away.
- Preserves the existing card title, count, summary, list rendering, search/header controls, and underlying data structures.
- Updated service-worker cache name for the new release.

Deployment: Extract this ZIP and publish the DentalFlow folder contents to the existing GitHub Pages deployment.
Rollback: Redeploy the previous ZIP. Do not clear LocalStorage; this update does not intentionally change stored data.

Validation performed: JavaScript syntax, HTML parsing/IDs, service-worker syntax, ZIP integrity, and required-file checks. Browser end-to-end testing was not performed.
