DentalFlow V7.9.0 — Unified Clinical Workflow Tabs

Base: DentalFlow V7.8.69 Materials Purchase Account Sync.

Changes in V7.9.0:
- Replaced the two separate More menu entries for “Appointments & Queue” and “Follow-ups & Reminders” with one “Clinical Workflow” entry.
- Combined Appointments, Queue, Follow Up, and Reminders into four consecutive horizontal tabs under one Clinical Workflow heading.
- Reused the existing panes, record lists, forms, counts, actions, and rendering logic; no clinical data structure or LocalStorage key was changed.
- Legacy calls to switchView('reminders') now open Clinical Workflow directly on the Follow Up tab. Calls to switchView('appointments') open it on Appointments.
- Updated service-worker cache version so deployed clients can load the new UI.

Deployment:
1. Export a DentalFlow backup before deployment.
2. Extract the ZIP and publish the contents of the DentalFlow folder to the existing GitHub Pages deployment.
3. Reload the app. If an older cached version remains, close/reopen the PWA or refresh after the service worker updates.

Rollback:
- Redeploy the prior DentalFlow V7.8.69 ZIP.
- Export a backup first and do not clear LocalStorage.

Automated checks performed for this build:
- JavaScript syntax checks for all inline scripts.
- Service-worker syntax check.
- HTML parsing and duplicate-ID scan.
- Manifest JSON parsing.
- ZIP integrity and required-file checks.
- Static navigation checks for all four tabs and legacy reminder navigation alias.

Limitations:
- Browser end-to-end testing was not performed.
