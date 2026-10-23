DentalFlow V7.8.65 — Simple Finance & Inventory Usability

Base: DentalFlow V7.8.64 Simple Finance & Inventory (which was created from the supplied V7.8.63 stable base).

Changes in V7.8.65:
- Added compact inventory filters: All, Low stock, Out of stock, and Expiring soon.
- Added a live count to the Expiring soon filter (expiry within the next 30 days).
- Added edit actions for manually entered expenses and other income; edits update the existing record rather than creating duplicates.
- Added a collapsed Other income list to keep the Finance screen compact while making income entries reviewable and editable.
- Added savings-goal editing so the saved amount can be updated over time.
- Added budget edit shortcut while preserving the existing category/month upsert behavior.
- Linked stock-purchase expenses remain edited through the Inventory purchase workflow to reduce mismatched stock/expense records.
- Preserved existing patient, clinical, appointment, billing, and LocalStorage data structures. No data migration or clearing is performed.

Deployment: Extract the ZIP and publish the contents of the DentalFlow folder to the existing GitHub Pages deployment.
Rollback: Redeploy DentalFlow_V7.8.63_Settings_Template_Section_Removed.zip if needed; preserve browser data and export a backup before deployment.

Validation performed: JavaScript syntax checks, HTML parsing, duplicate-ID scan, manifest JSON parsing, service-worker syntax, ZIP integrity, required-file checks, and static feature-handler checks. Browser end-to-end testing was not performed.

--- Previous release notes ---
DentalFlow V7.8.64 — Simple Clinic Finance & Materials Inventory

Changes in this version (based on the current V7.8.49 build):
- Today's Workflow cards are stacked vertically in this order: Appointments, Queue, Follow-ups, Reminders.
- Tapping a card header expands/collapses its list inline on the Home screen; it no longer navigates away.
- Preserves the existing card title, count, summary, list rendering, search/header controls, and underlying data structures.
- Updated service-worker cache name for the new release.

Deployment: Extract this ZIP and publish the DentalFlow folder contents to the existing GitHub Pages deployment.
Rollback: Redeploy the previous ZIP. Do not clear LocalStorage; this update does not intentionally change stored data.

Validation performed: JavaScript syntax, HTML parsing/IDs, service-worker syntax, ZIP integrity, and required-file checks. Browser end-to-end testing was not performed.


V7.8.59 — App-wide helper-text cleanup: removed static explanatory helper copy across section headings, forms, Settings and More cards. Labels, placeholders, dynamic record details, validation and empty states are retained.


V7.8.60 — Finance New Bill Fix
Fixed openBillForm referencing the removed billPaymentHint helper-text element. The hint is now optional, so New Bill/Edit Bill can open without a null-element exception. No data keys or bill/payment data structures changed.


V7.8.61 — Appointments tab count fix
Added a count badge to the Appointments tab in Appointments & Queue. It displays today's active appointments (excluding Completed and Cancelled), matching the existing Today metric, and updates whenever renderAppointments runs. Queue count behavior is unchanged.
Validation: JavaScript syntax, HTML parsing/IDs, manifest JSON, service-worker syntax, ZIP integrity and required-file checks. Browser end-to-end testing was not performed.


V7.8.63 — Settings template section removal
- Completely removed the “Clinical & Prescription Templates” management card from Settings.
- Kept the existing clinical/prescription template data and chairside template insertion workflow intact; no stored data is deleted or migrated.
- Updated the About version label and service-worker cache name.
Validation: JavaScript syntax, HTML parsing/structure, manifest JSON, service-worker syntax, ZIP integrity and required-file checks. Browser end-to-end testing was not performed.
Rollback: Redeploy the supplied DentalFlow_V7.8.63_Settings_Template_Section_Removed.zip. Do not clear LocalStorage.


V7.8.64 — Simple Clinic Finance & Materials Inventory
- Added lightweight Materials Inventory: item catalogue, opening stock, stock-in/out, minimum-stock warnings, expiry field, and recent stock activity.
- Added Clinic Finance: simple expense entry, accounts with opening balances, transfers, monthly collection/expense summary, basic budgets, and savings goals.
- Stock purchases can create a linked expense record when a payment account is selected; stock and expense are not entered twice.
- Existing patient, clinical, appointment, billing, and LocalStorage structures are retained; new finance/inventory data is stored in additional arrays.
- Service-worker cache version updated for deployment.
