DentalFlow V7.7.10 — Patient Billing & Payment Update

Based on the V7.7.8 Clean Patient Profile Accordion build.

Focused changes:
- Patient profile edit icon appears immediately to the right of Patient Name.
- New Bill includes an optional initial payment amount and payment mode. Initial payment is saved as a payment transaction, and cannot exceed the bill total.
- Patient Profile Billing & Payments includes a compact payment icon in the Payment History area when a balance is due; it opens the existing Record Payment flow. A shortcut is also shown when a bill has a due balance but no payment history yet.
- Service-worker cache version updated to V7.7.10 to help deployed clients pick up the new files.

Existing local data schema is retained. This ZIP contains app files only, not patient records. Before replacing a live clinic app, export a Safety Snapshot / JSON backup. Do not clear browser data during deployment.

Validation performed: inline JavaScript syntax check and ZIP integrity check. Interactive browser/device workflow was not run in this environment.
