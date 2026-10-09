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


DentalFlow V7.5.6 — Diagnosis ↔ Treatment Linking (Update 3)
- In Clinical Visit, select diagnosis text and treatment text, then tap Link to connect them.
- Links are saved with the clinical visit and shown in the Patient Profile clinical visit history.
- Multiple diagnosis-treatment links can be added; each can be removed before saving.
- Existing localStorage key and patient/clinical data structure are retained; older visits without links continue to work.
- Service worker cache updated for V7.5.6.

Suggested test: open a patient profile → Clinical Visit → add a diagnosis and treatment (using structured controls or typing) → link them → save → check the Dx ↔ Tx line in clinical visit history → reload and confirm it remains.


DentalFlow V7.5.7 — Treatment Plan ↔ Clinical Visit Linking (Update 4)
- Clinical Visit form can link one or more existing Treatment Plans for the same patient.
- Treatment Plan form can link one or more existing Clinical Visits for the same patient.
- Both records store reciprocal IDs (visit.linkedPlanIds and plan.linkedVisitIds).
- Patient Profile shows linked plans in visit history and linked visits in treatment-plan cards.
- Patient Timeline includes the linked plan/visit context.
- Deleting a Treatment Plan removes its references from linked visits.
- Older records remain compatible; missing link arrays default to empty arrays.
- Existing localStorage key dentalflow_v2 is retained.
- Service-worker cache updated to dentalflow-v7.5.7-plan-visit-link.

Suggested test:
1. Open a patient profile and create a Treatment Plan with at least one item.
2. Create a Clinical Visit for that same patient; in “Link existing Treatment Plan”, choose the plan and tap Link. Save the visit.
3. Check Patient Profile: the visit should show the linked plan.
4. Edit the Treatment Plan; in “Link Clinical Visit(s)”, choose the visit and tap Link. Save.
5. Check the plan card and Patient Timeline. Reload the app and confirm links remain.
6. Confirm other patients’ visits/plans do not appear in these link selectors.
