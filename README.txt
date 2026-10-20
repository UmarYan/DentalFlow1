DentalFlow V7.8.50 — Vertical Workflow Inline Expansion

Changes in this version (based on the current V7.8.49 build):
- Today's Workflow cards are stacked vertically in this order: Appointments, Queue, Follow-ups, Reminders.
- Tapping a card header expands/collapses its list inline on the Home screen; it no longer navigates away.
- Preserves the existing card title, count, summary, list rendering, search/header controls, and underlying data structures.
- Updated service-worker cache name for the new release.

Deployment: Extract this ZIP and publish the DentalFlow folder contents to the existing GitHub Pages deployment.
Rollback: Redeploy the previous ZIP. Do not clear LocalStorage; this update does not intentionally change stored data.

Validation performed: JavaScript syntax, HTML parsing/IDs, service-worker syntax, ZIP integrity, and required-file checks. Browser end-to-end testing was not performed.


V7.8.57 — Unified Navigation Revamp (2026-10-20)
- Added consistent context-aware More actions beside section headings.
- Refined mobile navigation, footer tabs, menu spacing, focus states and menu surfaces.
- Preserved the existing hamburger drawer, footer More utility page, bottom navigation, FAB, data model and PWA files.
- Contextual actions reuse existing application functions; no data migration or storage-key changes.
