DentalFlow V7.6.2 — Update 8: Context Workflow Actions & Cross-linking

WHAT'S NEW
- Patient Timeline entries are now interactive. Tap a Clinical Visit, Treatment Plan, Patient Record, Appointment, Bill, or Reminder to open its context detail sheet directly.
- Context detail sheets now show an "Open linked records" section when linked clinical visits, plans, bills, or reminders exist.
- Patient Profile billing cards include a Details action.
- Appointment cards include a Details action.
- Existing context-detail views, patient context, tooth context, Smart Input, FAB actions, treatment links, billing links, and follow-up links are retained.

DEPLOY
1. Keep an external JSON backup before replacing app files.
2. Extract this ZIP.
3. Replace the existing 7 GitHub Pages files with the 7 files from this ZIP.
4. Reload the app and test the Patient Timeline: tap each kind of timeline entry.
5. Open a Visit, Plan, Bill, or Reminder with linked records and test the "Open linked records" buttons.

DATA
- Existing localStorage key remains dentalflow_v2.
- No intentional data reset or schema migration is performed by this update.

VALIDATION
- Inline JavaScript syntax checked with Node.js.
- ZIP integrity checked.
- Live interaction testing on the user's phone has not been performed; verify in the deployed app before relying on the new navigation.


Update 9 — Context-aware Quick Actions & Workflow Integration:
- Clinical Visit details can start a linked Treatment Plan, Bill, or Follow-up.
- Treatment Plan details can start a linked Bill or Follow-up.
- Bill details can start a payment reminder with the bill preselected.
- Appointment details can start a Clinical Visit or Follow-up with the patient preselected.
- Context is prefilled only when the selected source record belongs to the same patient.
