DentalFlow V7.9.2 — Navigation & Data Security

Base: DentalFlow V7.9.0 Clinical Workflow Tabs.

Changes in V7.9.1:
- Replaced the separate More entries for Clinic Finance, Materials Inventory, and Laboratory Tracking with one Clinic Management entry.
- Added one Clinic Management workspace with three horizontal-scroll tabs: Finance, Inventory, and Lab Tracking. Tabs remain horizontally scrollable on narrow mobile screens.
- Preserved the existing Finance, Inventory, and Laboratory Tracking content, record IDs, action handlers, rendering functions, and LocalStorage structures by reusing the original module elements.
- Legacy navigation calls to clinicFinance, inventory, and labTracking now open Clinic Management and select the corresponding tab.
- Updated the hamburger menu and service-worker cache version.

Deployment:
1. Export a DentalFlow backup before deployment.
2. Extract the ZIP and publish the contents of the DentalFlow folder to the existing GitHub Pages deployment.
3. Reload the app. If an older cached version remains, close/reopen the PWA or refresh after the service worker updates.

Rollback:
- Redeploy the prior DentalFlow V7.9.0 ZIP.
- Export a backup first and do not clear LocalStorage.

Automated checks to perform before release: JavaScript syntax, service-worker syntax, HTML parsing and duplicate IDs, manifest JSON, navigation/tab static checks, and ZIP integrity. Browser end-to-end testing is not claimed.


V7.9.2 change log
- Renamed bottom navigation Finance to Billing.
- Kept Clinic Management Finance, Inventory and Lab Tracking as peer horizontal tabs.
- Reordered the main menu and added Data & Security grouping for Backup Data, Restore Data and Data Safety.
- Removed Data Safety shortcut from Settings.
- More now contains only Clinical Workflow, Clinic Management, Treatment Plans, Reports, Backup Data and Restore Data.
- Removed Global Search and Settings from More.
