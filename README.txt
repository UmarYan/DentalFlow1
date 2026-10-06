DentalFlow V8 — Appointment & Queue
Based directly on the stable DentalFlow V7 Dashboard & Reports foundation.

Updates:
- Patient appointment records with date, time, reason/treatment, status and note.
- Statuses: Scheduled, Confirmed, Waiting, In treatment, Completed, Cancelled, No-show.
- Dedicated Appointments & Queue screen available from the hamburger menu.
- Compact today queue with quick progression: Waiting → In treatment → Completed.
- Edit/delete appointments and open the linked patient directly.
- Existing V1–V7 features and dentalflow_v2 storage key retained.
- Existing patient data, clinical visits, tooth chart, treatment plans, templates, billing and reports retained.
- Service worker cache updated to V8.
- No external libraries.

Recommended test:
Add appointment → Appointments & Queue → Waiting → Start → Complete → Edit/Delete → Reload.
Then test existing Clinical Visit, Treatment Plan, Billing, Reports and Backup/Restore.
