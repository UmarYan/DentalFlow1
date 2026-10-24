DentalFlow V7.9.2 — Treatment Plan Before Treatment Done

Stable base: DentalFlow_V7.9.1_Clinic_Management_Tabs.zip

Changes in V7.9.2:
- Added a compact optional Treatment Plan section before Treatment Done in the standard Clinical Visit and Unified Patient Workflow.
- Planned procedure, tooth/area, estimated fee, and priority are saved as a treatment-plan item linked to the patient and clinical visit.
- “Completed today” is an explicit choice; a planned item is marked Completed only when selected and actual treatment is documented.
- Immediate treatment remains supported: leave the plan fields blank and record the actual Treatment Done directly.
- Preserved existing patient, visit, plan, appointment, billing, payment, and LocalStorage structures; no migration or reset is performed.
- Updated the service-worker cache version.

Deployment:
1. Export a DentalFlow backup before deployment.
2. Extract the ZIP and publish the contents of the DentalFlow folder to the existing GitHub Pages deployment.
3. Reload the app and test both planned-treatment and immediate-treatment paths.

Rollback:
- Redeploy DentalFlow_V7.9.1_Clinic_Management_Tabs.zip.
- Export a backup first and do not clear LocalStorage.

Checks performed for this build are listed in the delivery message. Browser end-to-end testing is not claimed unless explicitly stated.
