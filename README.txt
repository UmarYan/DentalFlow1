DentalFlow V7.8.4 — Save Verification & Data Safety

Base: DentalFlow V7.8.3 Workflow Draft Recovery.

Changes in this build:
- Verifies localStorage writes by reading back the exact saved payload.
- Shows a persistent warning if clinic data cannot be saved to this device.
- Exports a versioned JSON backup envelope with export time and record counts; import supports this format and older raw JSON backups.
- Import preview shows patient/visit/bill counts and warns about duplicate IDs, missing patient references, or invalid bill/payment amounts before replacement.
- Data check now includes invalid bill/payment amounts.
- Keeps existing workflow draft recovery, internal record associations, and clinic sections.
- Updates app labels and service-worker cache version.

Important limits:
- This is local-device storage; JSON export is an external backup, not cloud sync.
- If a save warning appears, do not reload/close the app until you have exported what you can and resolved the storage issue.
- JavaScript syntax and ZIP integrity checks are performed for this package. Physical Android end-to-end testing, real patient data migration, and backup/restore acceptance testing remain to be done.
- Test with a fictional patient first. Do not clear Chrome site data. Export a JSON backup before replacing deployed files.
