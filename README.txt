DentalFlow V7.6.3 — Update 10: Full Workflow Review & UX Polish

WHAT CHANGED
- Fixed the Backup & Data Safety back button by adding the missing showView() navigation alias.
- Patient deletion now also removes that patient’s reminders, avoiding orphan reminders in the clinic. The confirmation clearly names the related record types.
- Expanded Run data check: reports duplicate IDs, records without a matching patient, and broken/cross-patient links. This is read-only; it does not automatically alter records.
- Improved keyboard focus visibility and small-screen touch-target spacing.
- Existing patient data key remains dentalflow_v2; no intentional data reset.

DEPLOY
1. Export an external JSON backup first.
2. Extract this ZIP.
3. Replace the current 7 GitHub Pages files with the 7 files in this ZIP.
4. Test Backup & Data Safety → back button; test Run data check; test patient deletion only with a test patient if possible.
5. Test the main path Patient → Visit → Tooth/Area → Diagnosis/Treatment → Plan → Bill/Payment → Follow-up, then reload and verify.

VALIDATION
- Inline JavaScript syntax checked with Node.js.
- ZIP integrity and 7-file package checked.
- Static audit checked inline handler names and direct DOM references.
- Live testing on the user's phone has not been performed.
