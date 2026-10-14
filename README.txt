DentalFlow V7.8.9 — Blank Screen & Raw-Code Fix

Purpose:
- Fixes a malformed script/HTML boundary in V7.8.8 that caused JavaScript source to appear as visible text on the screen and could interfere with home-screen interaction.
- Retains the V7.8.8 Smart Multi-Entry changes: type an item and press Enter to add it, with no per-item Add button; separate item suggestions; edit/remove individual entries; paste multiple lines as separate entries.
- Updates service-worker cache version so the corrected app assets can be fetched.

Before deployment:
- Export a JSON backup first. Do not clear Chrome site data.
- Replace repository files with the ZIP contents. If the old screen remains, verify the deployed files and let the service-worker update take effect; do not delete site data because patient records may be stored there.

Testing status:
- Automated JavaScript syntax and ZIP integrity checks are required/checked during packaging.
- Real Android end-to-end testing, data migration, draft recovery, and backup/restore have not been verified in this environment. Test with a fictional patient before using in clinic.


V7.8.10 — Billing & Payment Layout
- Billing fields arranged in two rows, two fields per row: Treatment/Service + Total Fee; Received Now + Payment Mode.
- Treatment/Service uses the same Enter-to-add multi-entry interface as other Patient Workflow sections; no Add button required.
- Service entries remain newline-separated within the existing bill item format for compatibility with existing records.
- Please back up clinic data before deployment and test with a dummy patient.
