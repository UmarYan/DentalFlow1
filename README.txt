DentalFlow V7.9.6 — App-wide Tooth/Area Cleanup

Changes:
- Removed remaining tooth/area selection UI and stale visit-save/rendering code throughout the app.
- Removed obsolete tooth-grid swipe exclusion and blank tooth fields from newly created visit/bill records.
- Preserved legacy tooth-related properties during data normalization to avoid deleting existing clinical data.
- Preserved Patient Workflow and its FAB, other clinic modules, and LocalStorage key compatibility.

Deployment: deploy the contents of this folder to the existing GitHub Pages location.
Rollback: redeploy DentalFlow_V7.9.2_Navigation_Data_Security.zip if needed.
