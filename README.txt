DentalFlow V10 — Patient Records & Clinical Records
Built directly on the stable DentalFlow V8 foundation.

V8 fixes/refinements:
- Fixed + Appointment so the appointment form opens correctly.
- Removed Search from bottom navigation.
- Bottom navigation now includes Appointments and Billing for faster chairside access.

V10 — Patient Records:
- Patient Records module for Medical history, Allergy, Investigation, Referral, Consent, Document note and Other.
- Add, edit and delete patient records.
- Search records by patient, title, type, phone or Patient ID.
- Record date, title and detailed notes.
- Patient shortcut from each record.
- Existing V1–V8 patient, clinical, treatment-plan, prescription-template, billing, reports and appointment data retained.
- Existing dentalflow_v2 localStorage key retained.
- Defensive data normalization upgraded to schema version 10.
- Service worker cache updated to V10.
- No external libraries.

Recommended test:
1. Existing patient → Appointments → + Appointment → form opens → Save → Waiting → Start → Complete.
2. Footer → Appointments and Billing; confirm Search is no longer in footer.
3. Menu → Patient Records → + record → Save → Edit → Delete → Reload.
4. Test old Clinical Visit, Treatment Plan, Templates, Billing, Reports and Backup/Restore.
