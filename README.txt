DentalFlow V7.7.0 — Simplified Workflow

This build is based on DentalFlow V7.6.5 Clinical Visit Open/Add Fix.

Simplification changes:
- Home dashboard visual clutter reduced while retaining underlying metrics/data.
- Diagnosis-to-treatment and visit-to-plan links are now inside a collapsed Advanced links (optional) section in Clinical Visit.
- Treatment Plan to Clinical Visit linking is collapsed under an optional section.
- Billing clinical-context links are collapsed under an optional section.
- Quick-add FAB shows fewer primary actions; advanced actions remain available in their dedicated screens/menu.
- Existing localStorage key dentalflow_v2 is unchanged. No intentional data reset or schema deletion.

Deployment: replace the existing 7 GitHub Pages files with these 7 files. Back up data externally first. After deploy, test Patient, General Clinical Visit, Patient-specific Clinical Visit, Save/Reload, Billing and Backup/Restore.

This package has static code/ZIP validation only; test on the target phone before relying on it clinically.
