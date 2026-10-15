DentalFlow V7.8.14 — Bold Global Suggestion Actions

Changes:
- Add and delete suggestion actions are available in both the general smart-suggestion popup and the unified clinical multi-entry popup.
- Applies to all supported smart-suggest fields throughout the app, including Chief complaint, History, Examination, Diagnosis, Treatment done, Prescription, Advice, patient/appointment/plan/record/reminder fields, and Treatment/Service.
- The “＋ Add … to suggestions” action is now bold and visually prominent across both popup systems, matching the stronger blue action shown in the reference screenshot.
- Add saves a reusable suggestion; selecting a suggestion inserts it into the active field. Delete removes only the reusable suggestion, not existing patient or visit records.
- Multi-entry clinical items still use Enter to commit, with per-item edit/remove controls.
- Fee field remains excluded from auto-suggestions.
- Service-worker cache version updated.

Before deployment:
- Export a JSON backup first. Do not clear Chrome site data.
- Replace repository files with the ZIP contents.
- Test with a fictional patient before clinic use.

Validation status:
- JavaScript syntax checks and ZIP integrity are checked during packaging.
- Real Android end-to-end behavior, draft recovery, data migration, and backup/restore are not verified here.
