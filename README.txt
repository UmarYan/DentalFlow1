DentalFlow V7.8.2 — Continuous Patient Workflow

Base used: DentalFlow_V7.8.1_Link_Free_Simplified.zip supplied in this conversation.

Changes in this build:
- Adds a single Patient Workflow entry from the Home FAB and the patient profile FAB.
- The workflow can select an existing patient or create a patient without leaving the workflow.
- Captures arrival type, clinical notes, diagnosis, treatment, prescription, advice, follow-up date, and optional billing/payment in one workspace.
- Creates internal associations between a visit and any appointment, bill, or follow-up generated in this workflow. No manual linking UI is required.
- Keeps existing standalone patient, visit, treatment plan, billing, appointment, reminder, records, search, reports, backup, and restore features available.
- Data normalization now preserves existing association fields rather than deliberately deleting them.
- Updates the service-worker cache version to reduce stale-app loading after deployment.

Data and deployment notes:
- Patient records are stored in this browser's local storage; this ZIP does not contain patient records.
- Export a JSON backup before replacing the deployed files. Do not clear browser/site data during deployment.
- JavaScript syntax and ZIP integrity are checked. Full real-device interaction, storage quota failure, and all workflow paths have not been exhaustively tested in a physical Android device.
