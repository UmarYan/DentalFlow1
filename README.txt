DentalFlow V7.7.11 — Focused FAB, Search & Payment Update

Based on the V7.7.10 Patient Billing & Payment Update build.

Focused changes only:
- Home FAB now includes Appointment, Clinical Visit, New Plan, Follow-up and New Bill; existing New Patient shortcut remains.
- Removed automatic suggestion popups from Quick patient search, Patients section search and the New Patient name field. Patient search results appear in the existing results area below as the user types.
- In New Bill / Edit Bill, Payment received is placed directly after bill items and before Bill note, without a separate card.
- Edit Bill now accepts an optional additional payment; existing payments are retained as separate transactions and the new payment is validated against the remaining due.
- Billing card action order is Details, Edit, Receipt, then a compact payment icon when due remains.
- Updated service-worker cache version to V7.7.11.

Existing local data schema is retained. This ZIP contains app files only, not patient records. Before replacing a live clinic app, export a Safety Snapshot / JSON backup. Do not clear browser data during deployment.

Validation performed: inline JavaScript syntax check and ZIP integrity check. Interactive browser/device workflow was not run in this environment.
