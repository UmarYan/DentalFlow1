DentalFlow V7.8.3 — Workflow Draft Recovery

Base: DentalFlow V7.8.2 Continuous Patient Workflow.

Changes in this build:
- Adds local draft autosave to the continuous Patient Workflow (debounced while typing).
- Offers to resume a saved draft when opening the workflow again.
- Adds a Discard draft action. Successfully saved workflows clear their draft.
- Drafts are stored separately in this browser's local storage and do not create patient/visit/bill records until Save & finish is used.
- Updates service-worker cache version and app version labels.

Important limits:
- Draft recovery is device/browser-specific and is not a substitute for a clinic-data JSON backup.
- This build has been checked for JavaScript syntax and ZIP integrity, but not exhaustively tested on a physical Android device. Test with a fictional patient first.
- Do not clear Chrome site data; patient records and drafts use local storage. Export a JSON backup before replacing deployed files.
