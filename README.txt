DentalFlow V7.8.49 — Appointment Next Time & Header Quick Search

Working base: DentalFlow V7.8.48 — Today's Workflow Grid & Bold Titles, built from the user-designated V7.8.47 Header Alignment & Context FAB ZIP. V7.8.45 remains the historical baseline for the earlier development lineage; this update preserves the prior requested grid/title changes.

Requested changes:
- Fixes the Today's Workflow Appointments summary so it chooses and displays a next appointment time from today's active appointments, handling 12-hour and 24-hour time strings. If there is no usable time, the summary explicitly falls back to “time TBD”.
- Makes the Appointments, Queue, Follow-ups and Reminders labels the same font size as their counts.
- Makes the four workflow cards more compact, using the same restrained background/padding treatment as the Dashboard metric cards; retains the 2x2 layout, separate destinations, bold home card titles, counts and readable summaries.
- Removes the Quick patient search card from the middle of the Home screen and moves its existing patient-search input/results into a compact panel opened by the header search icon. The header Add Patient icon and existing Advanced Search entry in the menu remain available.
- Updates the service-worker cache key for this build.

Data safety:
- No LocalStorage keys or data schema were intentionally changed.
- Patient, clinical, appointment, follow-up, reminder, treatment-plan, billing and payment records are not migrated or reset.
- Unrelated features are intended to remain unchanged.

Automated checks to run before delivery:
- JavaScript syntax check for extracted inline scripts and service worker.
- HTML parser integrity and duplicate-ID checks.
- ZIP integrity check and required-file check.
- Static checks for the moved search controls, workflow tile styles and appointment summary logic.

Browser end-to-end testing was not performed. After deployment, manually test the next-time summary with appointments that have times (including AM/PM), header quick search/results, opening a patient profile from results, Add Patient, all four workflow cards, and the main clinical/billing workflows.

Rollback: redeploy the previously stable ZIP designated by the user. Do not clear LocalStorage when rolling back.
