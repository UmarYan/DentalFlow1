DentalFlow V7.11.20 — Clinical Visit Shared Form & Edit Prefill Fix

Base: DentalFlow_V7.11.19_Patient_Visit_Entry_Section_Alignment.zip.

Change log:
- Patient Visit Entry sections now appear in the requested order: Patient; Appointment / arrival; Clinical visit; Treatment plan; Follow-up; Billing & payment; Reminder / task; Patient record / document.
- Reminder / task and Patient record / document now use the same card structure, left edge, summary padding, and optional hint alignment as the other sections.
- Updated the service-worker cache identifier to V7.11.19.
- No patient data structures, LocalStorage keys, clinical data, billing data, or unrelated workflows were intentionally changed.

Validation performed:
- ZIP integrity test.
- JavaScript syntax check of all inline JavaScript blocks and service worker.
- HTML tag balance checks for script/style and workflow section structure.
- Static checks for requested section order and consistent section classes.
- Browser/mobile runtime testing was not performed.

Post-deployment checklist:
1. Open Patient Visit Entry and verify the eight sections appear in the listed order.
2. Confirm all section cards begin at the same left edge and have matching arrow/title alignment.
3. Expand Reminder / task and Patient record / document; verify all fields still work.
4. Save a visit and confirm patient data and existing billing/clinical records remain available.
5. Confirm Android Back navigation still returns to the previous app view.

Rollback: redeploy DentalFlow_V7.11.18_Android_Back_Navigation_Fix.zip.


V7.11.20 change log:
- Clinical Visit Add continues to use the shared Patient Visit Entry form and starts with blank clinical fields.
- Clinical Visit Edit explicitly rebinds the selected saved visit by record ID after the shared form opens, pre-filling chief complaint, history, examination, diagnosis, treatment, prescription, advice, and next-visit fields.
- Existing save path continues to update the selected visit ID; no new visit is created by Edit.
- Updated service-worker cache identifier.

Validation performed for V7.11.20:
- ZIP integrity test.
- JavaScript syntax check of all inline script blocks and service worker.
- Static checks for the new edit-prefill binding and existing-record save path.
- Browser/mobile runtime testing was not performed.

Rollback: redeploy DentalFlow_V7.11.19_Patient_Visit_Entry_Section_Alignment.zip.
