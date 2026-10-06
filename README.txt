DentalFlow V14 — Settings & Customization
Based on the stable DentalFlow V13 Backup & Data Safety foundation.

Updates:
- Expanded clinic profile: clinic name, doctor, phone, address and registration/licence number.
- Workflow defaults for new payments, appointments and reminders.
- Receipt customization: show/hide doctor name and clinic contact details.
- Compact interface option for faster chairside scanning.
- Preference reset does not delete patient or clinical data.
- Existing V1–V13 data retained; existing dentalflow_v2 localStorage key retained.
- Data schema upgraded defensively to version 14.
- Backup & Data Safety remains available as a dedicated center.
- No external libraries.
- Service worker cache updated to V14.

Recommended test:
1. Deploy and open DentalFlow.
2. Settings → edit clinic profile → Save settings → reload.
3. Set default payment/appointment/reminder values and create new entries to verify defaults.
4. Enable receipt options and print a receipt to verify clinic details.
5. Toggle Compact interface and confirm spacing changes.
6. Reset preferences and confirm patient/clinical data remains untouched.
7. Open Backup Center and verify V13 safety tools still work.
