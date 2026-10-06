DentalFlow V5 — Prescription & Clinical Templates

Based on the stable DentalFlow V4 Treatment Planning foundation.
Updates:
- Reusable templates for Examination, Diagnosis, Treatment, Advice and Prescription.
- One-tap template insertion directly inside the Clinical Visit form.
- Custom template creation, editing and deletion from Settings.
- Default templates provide documentation structure; prescription text remains editable by the dentist.
- Existing patient, clinical visit, tooth chart and treatment-plan data retained.
- Existing dentalflow_v2 localStorage key retained for data continuity.
- Data schema upgraded defensively to version 5.
- No external libraries.
- Service worker cache updated to V5.

Recommended test:
Existing patient → Profile → Clinical visit → template buttons → edit text → Save → Profile.
Then Settings → Clinical & Prescription Templates → New/Edit/Delete → reload.
Also test old Treatment Plans and Backup/Restore.
