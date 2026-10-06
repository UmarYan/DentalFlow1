DentalFlow V12 — Follow-up & Reminder Center
Based directly on the stable DentalFlow V11 Advanced Search & Clinical Timeline foundation.

Updates:
- Patient-linked follow-up/reminder center.
- Due date, reminder type and note.
- Types: Follow-up, Call, Review, Payment, Treatment, Other.
- Statuses: Pending, Done, Snoozed.
- Dashboard reminder summary with overdue and due-today counts.
- Dedicated Follow-up & Reminders screen with search.
- Quick Done, Snooze, Edit, Delete and Patient actions.
- Reminder activity appears in the Patient Timeline.
- Existing V1–V11 data and dentalflow_v2 storage key retained.
- Defensive schema upgraded to V12.
- Service worker cache updated to V12.
- No external libraries.

Recommended test:
Create reminder → dashboard → Done/Snooze → Edit/Delete → reload.
Then verify Clinical Visit, Treatment Plan, Billing, Appointments, Advanced Search, Patient Timeline and Backup/Restore.
