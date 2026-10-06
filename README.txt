DentalFlow V13 — Advanced Backup & Data Safety

Based on the stable DentalFlow V12 Follow-up & Reminder foundation.

Updates:
- Backup & Data Safety center.
- Manual safety snapshots (metadata/count snapshots) before risky operations.
- Export full clinic data as validated JSON backup.
- Import JSON backup with structure validation and confirmation.
- Data health check.
- Clear safety/reset flow with double confirmation.
- Existing V1–V12 patient, clinical, treatment, billing, appointment, record and reminder data retained.
- Existing dentalflow_v2 localStorage key retained for data continuity.
- Schema version upgraded defensively to version 13.
- Service worker cache updated to V13.
- No external libraries.

Recommended test:
1. Open Backup & Data Safety.
2. Run data check.
3. Create Snapshot.
4. Export JSON and verify the file downloads.
5. Import the exported JSON only after confirming; the app creates a safety snapshot first.
6. Reload and verify all patient/visit/billing/appointment/reminder data.

Note: Safety snapshots store metadata/counts, while Export JSON contains the full restorable dataset.
