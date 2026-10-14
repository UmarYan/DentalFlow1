DentalFlow V7.8.8 — Smart Multi-Entry

This update focuses on multiple independent entries inside the Patient Workflow clinical fields.

Changes:
- Chief complaint, Examination, Treatment done, History, Diagnosis, Prescription, and Advice now use an item-entry interface.
- Type an item and press Enter to add it. There is no per-item Add button.
- Tap a previous suggestion to add it as an item.
- Each item can be edited or removed independently.
- Each field uses its own suggestion group (complaint, examination, treatment, history, diagnosis, drug, advice).
- Existing stored field values remain newline-separated strings for backward compatibility with prior visit records and the existing workflow save function.
- Draft save/recovery continues to work through the original field backing values.
- Pasting multiple lines into the entry box adds each non-empty line as a separate item.
- Service worker cache name updated.

Important testing notes:
- This is a code update, not a claim of full real-device acceptance testing.
- Test on Android using a fictional patient: add several items with Enter, edit/remove one, select a suggestion, close/reopen/resume draft, save, reload, and verify old records remain intact.
- Export a JSON backup before deployment. Do not clear Chrome site data.
