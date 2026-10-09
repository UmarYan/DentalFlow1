DentalFlow V7.5.4 — Update 1: Patient Context Layer
Based on DentalFlow V7.5.3 Context-aware FAB.

New in this update:
- Patient cards/names in key clinic lists are interactive and open a Quick Patient Context sheet.
- Patient Context shows recent visit, active treatment plan, due balance, next follow-up, next appointment and visit count.
- Quick actions: Profile, Clinical Visit, Treatment Plan, Billing, Appointment, Follow-up, Patient Record and Edit Patient.
- Patient-linked actions automatically preselect the patient.
- Patient Profile now has a direct Patient Context entry point.
- Existing V7.5.3 Context-aware FAB and V7.5.1 Smart Input are retained.

Not included yet:
- Tooth Context
- Diagnosis ↔ Treatment linking
- Billing ↔ Treatment linking
- Global context popups for every clinical object

Stability:
- Existing dentalflow_v2 localStorage key retained.
- No external libraries.
- Service worker cache version bumped for this update.


DentalFlow V7.5.5 — Tooth / Area Context (Update 2)
- Tap tooth-status chips in Patient Profile or Clinical Visit History to open Tooth / Area Context.
- The context view summarizes recorded tooth status, related clinical visits, treatment-plan items, and billing items.
- Quick actions start a new Clinical Visit, Treatment Plan, or Bill with the patient preselected.
- While editing a Clinical Visit tooth chart, use History to open the selected tooth context.
- Existing patient records and Smart Input storage keys are retained.
