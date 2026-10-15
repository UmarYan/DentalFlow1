DentalFlow V7.8.13 — Workflow Smart Suggestions

Based on the supplied V7.8.12 Clinical Multi-Entry AutoSuggest build.

Requested changes:
- “＋ Add "…" to suggestions” is bold blue in both suggestion popup styles.
- Patient Workflow new-patient name field no longer shows the auto-suggestion popup.
- Patient Workflow Address and Medical Alert are separate fields; both use smart suggestions.
- Medical Alert supports multiple entries using Enter only, without an Add button, and allows editing/removing entries and managing saved suggestions.
- Advanced Search input no longer shows auto-suggestion popups.
- Existing Treatment/Service and fee workflow was not intentionally changed.

Deployment notes:
- Export a JSON backup before deployment and keep the previous ZIP as rollback.
- Test with a fictional patient first, including draft recovery and backup/restore.

Testing status:
- JavaScript syntax checks passed for all embedded scripts.
- Archive integrity check performed after packaging.
- Real Android/browser end-to-end testing has not been performed in this environment.
