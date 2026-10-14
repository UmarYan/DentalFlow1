DentalFlow V7.8.6 — Workflow Error Recovery

Base: DentalFlow V7.8.5 Workflow Reliability Check.

Changes in this build:
- Adds a safer startup failure path: if stored clinic data cannot be parsed or normalized, DentalFlow shows a recovery screen instead of continuing with an empty dataset.
- Prevents the failed-load path from immediately writing a blank replacement over the existing primary local-storage record.
- Adds an Export stored data action on the recovery screen. It exports the original raw stored value as JSON when parseable, or TXT if the stored value is malformed.
- Keeps the existing patient workflow, draft recovery, data check, backup tools, and clinic features.
- Updates app title, backup version label, and service-worker cache version.

Important limits:
- This recovery export is a raw copy of the primary local-storage value, not a guarantee that damaged data can be imported without review.
- Data remains local to this browser/device unless separately exported. This is not cloud sync.
- JavaScript syntax and ZIP integrity checks are performed for this package. Physical Android end-to-end testing, real patient data migration, and backup/restore acceptance testing remain to be done.
- Test with a fictional patient first and export a normal JSON backup before replacing deployed files. Do not clear Chrome site data.
