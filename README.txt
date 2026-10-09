DentalFlow V7.5.9 — Update 6: Follow-up ↔ Clinical Story Linking

UPDATE 6 — FOLLOW-UP ↔ CLINICAL STORY LINKING
- Reminders can optionally link to a same-patient Clinical Visit, Treatment Plan, and Bill.
- Reminder cards show the linked clinical context; linked plans and bills can be opened directly.
- Patient Timeline now includes the reminder's related context.
- Existing reminders without links continue to work; patient data key is unchanged.


WHAT'S NEW IN UPDATE 6
- Each reminder can optionally link to a Clinical Visit, Treatment Plan, and/or Bill for the same patient.
- Link selectors only show records belonging to the selected patient.
- Reminder cards show linked clinical context.
- Linked Treatment Plans and Bills can be opened directly from reminder cards.
- Patient Timeline includes the reminder's linked visit/plan/bill context.
- Existing reminders without links continue to work.

FEATURES RETAINED FROM EARLIER UPDATES
- Context-aware patient actions and quick patient context.
- Tooth / Area Context.
- Diagnosis ↔ Treatment linking.
- Treatment Plan ↔ Clinical Visit linking.
- Billing ↔ Treatment Plan / Clinical Visit linking.
- Smart Input and context-aware FAB.
- Patient management, clinical visits, treatment planning, billing, appointments, patient records, reminders, reports, and backup/data-safety tools.

DEPLOYMENT
1. Make an External Backup from DentalFlow before replacing files.
2. Extract this ZIP.
3. Replace the current GitHub Pages deployment files with all 7 files from this ZIP.
4. Open the app and test reminder create/edit, context links, patient timeline, and reload persistence.

IMPORTANT
- The existing localStorage key `dentalflow_v2` is retained; replacing site files does not intentionally clear local patient data.
- Keep an external JSON backup before deployment, because browser storage and in-app safety snapshots are not a substitute for an external backup.
- JavaScript syntax and ZIP integrity were checked. Full live browser testing on the user's phone has not been performed.
