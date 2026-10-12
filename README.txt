DentalFlow V7.7.2 — Minimal Home Screen

This build is based on DentalFlow V7.6.5 Clinical Visit Open/Add Fix.

Home simplification changes:
- Removed the Outstanding Dues section from Home; dues remain available in Billing.
- Removed the monthly billing/plans metric row from Home.
- Shortened the Home heading and made appointment rows compact (up to 3).
- Made Home reminders compact (up to 3, details-only); full Done/Snooze/Edit/Delete actions remain on the Reminders screen.
- Shortened clinical next-visit rows (up to 4) and retained context details.
- Kept the four tappable Patients/New this month/Today's visits/Follow-ups metrics.
- Diagnosis-to-treatment and visit-to-plan links are now inside a collapsed Advanced links (optional) section in Clinical Visit.
- Treatment Plan to Clinical Visit linking is collapsed under an optional section.
- Billing clinical-context links are collapsed under an optional section.
- Quick-add FAB shows fewer primary actions; advanced actions remain available in their dedicated screens/menu.
- Existing localStorage key dentalflow_v2 is unchanged. No intentional data reset or schema deletion.

Deployment: replace the existing 7 GitHub Pages files with these 7 files. Back up data externally first. After deploy, test Patient, General Clinical Visit, Patient-specific Clinical Visit, Save/Reload, Billing and Backup/Restore.

This package has static code/ZIP validation only; test on the target phone before relying on it clinically.


V7.7.4 Home UI Refinement update
- Compact, consistent spacing and softer card hierarchy across screens and sheets.
- Common secondary actions (Details, Edit, Delete, Close, Cancel, Done, Snooze, Receipt, etc.) display as accessible icon buttons with title/aria labels.
- Action groups with four or more buttons keep the first two visible and place remaining actions in a tap-open More menu.
- Existing app data key and data model are preserved.
- Please export a JSON backup before deploying; test patient, visit, appointment, billing, reminders, backup/restore after deploy.
