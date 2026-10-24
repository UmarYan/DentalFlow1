DentalFlow V7.9.3 — Compact Treatment Plan & Auto Sync

Base: DentalFlow V7.9.2_Treatment_Plan_Before_Treatment_Done.zip

Changes in V7.9.3:
- Simplified Treatment Plan item entry: Planned Treatment, Estimated Cost, and Status are aligned horizontally on desktop; compact responsive layout on mobile.
- Tooth/Area remains available as a compact field. Priority and notes moved under optional “More details”.
- Added “Completed today” as a clear status choice.
- When a plan item is saved as Completed, its treatment is added to the patient’s Treatment Done record (linked to a clinical visit) and an open billing record is created once per plan item.
- The generated bill carries the estimated cost as a suggested fee and clearly notes that the actual fee must be verified before finalizing. No payment is recorded automatically.
- Sync is idempotent for linked plan items to avoid duplicate bills on repeated saves.
- Existing immediate-treatment workflow remains available.
- Existing LocalStorage keys and data structure remain in place; no reset or migration is performed.

Deployment:
1. Export a DentalFlow JSON backup before deployment.
2. Extract the ZIP and publish the contents of the DentalFlow folder to the existing GitHub Pages deployment.
3. Test a Planned item, then mark it Completed today. Confirm Treatment Done and Billing show the item, check the generated bill fee, and verify no payment was recorded automatically.
4. Test an immediate treatment without a plan and verify existing records remain intact.

Rollback:
- Redeploy DentalFlow_V7.9.2_Treatment_Plan_Before_Treatment_Done.zip (the immediate previous build) or the designated stable base DentalFlow_V7.9.1_Clinic_Management_Tabs.zip.
- Export a backup first. Do not clear LocalStorage.

Quality checks: see delivery notes. Browser end-to-end testing is not claimed unless explicitly performed.
