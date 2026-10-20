DentalFlow V7.8.47 — Header Alignment & Context FAB

Stable source base: DentalFlow V7.8.45 — Script Boundary Fix.

Requested changes implemented:
- Keeps the header title/clinic label aligned to the left after removing the text-based + Patient header button.
- Adds a Universal Search icon and Add Patient icon on the right side of the header.
- Universal Search opens the existing Advanced Search view and focuses its search field.
- Add Patient opens the existing New Patient form.
- Carries forward the requested context FAB behavior: tapping FAB opens the primary new-entry/workflow form directly rather than showing a list of “New …” options.
- Removes the upper section-level add buttons for clinical visit, appointment, walk-in, follow-up and bill; contextual action buttons inside patient/record detail views are preserved.
- Updates the service-worker cache key so deployed clients can fetch this build.

No intentional changes to patient data structures, LocalStorage keys, clinical records, appointment/payment records, or unrelated features.

Checks performed:
- JavaScript syntax checks on extracted inline script blocks.
- Service-worker JavaScript syntax check.
- HTML parser integrity check.
- Duplicate HTML ID check.
- ZIP integrity check.

Browser end-to-end testing was not performed. Before deployment, export a data backup and manually test header search, Add Patient, and direct FAB behavior on each relevant section.

Rollback: redeploy the original DentalFlow_V7.8.45_Script_Boundary_Fix.zip files. Do not clear LocalStorage when rolling back.


DentalFlow V7.8.48 — Today's Workflow Grid & Bold Home Titles
Base: DentalFlow V7.8.47_Header_Alignment_Context_FAB.zip
Changes: Today's Workflow presented as four icon-free cards in a 2x2 grid; each card shows title, count and readable summary and opens its corresponding list. Home-screen card titles and Dashboard metric labels are bold. No data schema or LocalStorage keys changed.
