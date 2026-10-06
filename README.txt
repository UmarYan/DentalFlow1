DentalFlow V7 — Clinic Dashboard & Reports
Based on the stable DentalFlow V6 Billing & Payment foundation.

Updates:
- Expanded Home dashboard with monthly billed, collected, overall due and active treatment-plan metrics.
- Added compact Outstanding Dues panel with quick Billing access.
- Added dedicated Clinic Reports screen.
- Monthly report filter for visits, new patients, billing and collections.
- Billing status breakdown: Open, Partially paid, Paid.
- Treatment plan status breakdown.
- Payment-mode collection summary.
- Recent monthly clinical/billing activity.
- Existing patients, clinical visits, tooth chart, treatment plans, templates and billing data retained.
- Existing dentalflow_v2 localStorage key retained for data continuity.
- Data schema upgraded defensively to version 7.
- No external libraries.
- Service worker cache updated to V7.

Recommended test:
Home dashboard → Billing → patient bill/payment → Reports → change report month → check metrics/statuses/activity → reload.
Then test existing Clinical Visit, Treatment Plan, Templates and Backup/Restore.
