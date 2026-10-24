DentalFlow V7.9.2 — Treatment Plan Workflow

Base: DentalFlow V7.9.1 Clinic Management Tabs.

Changes in V7.9.2:
- Added a working More → Treatment Plans view with cross-patient search, status and patient filters, details, edit and patient-profile actions.
- Added an optional “Add Treatment Plan” choice to Patient Workflow. After the workflow is saved, the linked Treatment Plan form opens with patient, visit link, examination and diagnosis context prefilled. The plan is not saved until treatment items are added and the user confirms Save.
- Treatment Plan details now allow selecting items to include in a bill. Completed and In progress items are preselected; Planned items are not automatically selected.
- Selected plan items, tooth/area and estimated fees populate a new bill; fee fields remain editable before saving. The bill stores its linkedPlanId.
- Existing Patient, Clinical Visit, Appointment, Billing, Finance, Inventory, Lab Tracking and LocalStorage structures are preserved; no data reset or migration was added.
- Updated title, backup version label, and service-worker cache.

Deployment:
1. Export a DentalFlow backup before deployment.
2. Extract the ZIP and publish the contents of the DentalFlow folder to the existing GitHub Pages deployment.
3. Reload the app and test More → Treatment Plans, Patient Workflow → Add Treatment Plan, and plan → bill.

Rollback:
- Redeploy DentalFlow V7.9.1_Clinic_Management_Tabs.zip.
- Export a backup first and do not clear LocalStorage. Bills created from plans in this version keep their plan link in the new version's data; older app versions may not display that link.

Browser end-to-end testing is not claimed.
