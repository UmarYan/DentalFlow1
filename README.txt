DentalFlow V6 — Billing & Payment
Based on the stable DentalFlow V5 Prescription & Clinical Templates foundation.
Updates:
- Patient-specific dental bills with multiple service/tooth line items.
- Quantity, amount and automatic bill total.
- Payment recording with amount and payment mode (Cash / UPI / Card / Bank transfer / Other).
- Automatic Paid / Partially paid / Open status and due balance.
- Billing dashboard with total billed, collected and outstanding due.
- Billing section available from the hamburger menu and directly inside each patient profile.
- Compact receipt view with browser print support.
- Existing patients, clinical visits, tooth chart, treatment plans and templates retained.
- Existing dentalflow_v2 localStorage key retained for data continuity.
- Data schema upgraded defensively to version 6.
- No external libraries.
- Service worker cache updated to V6.
Recommended test:
Existing patient → Profile → + Bill → add services → Save → add partial payment → verify Due/Partially paid → add remaining payment → verify Paid → Receipt/Print → reload.
Also test existing Treatment Plans, Clinical Visits, Templates and Backup/Restore.
