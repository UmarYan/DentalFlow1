DentalFlow V7.6.5 — Update 12: Clinical Visit Open/Add Fix

WHAT CHANGED
- Fixed a function-name mismatch in the Clinical Visit form. The form called an undefined refreshVisitPlanOptions() function, so JavaScript stopped before the form could open.
- The patient selector now uses the existing renderVisitPlanOptions() function when the selected patient changes.
- This fixes both general Clinical Visit creation and patient-specific Clinical Visit creation from a Patient Profile/context action.
- Preserved the existing dentalflow_v2 LocalStorage key and the other app features.
- Updated the service-worker cache namespace to help browsers load the corrected files.

DEPLOY
1. Export an external JSON backup first.
2. Extract this ZIP.
3. Replace all 7 current GitHub Pages files with these 7 files.
4. Open Clinical Visits > + New clinical visit; confirm the form opens.
5. Open a Patient Profile > + Clinical visit; confirm the form opens with that patient selected.
6. Save a test visit only when appropriate, then reload and confirm it remains visible.

VALIDATION
- JavaScript syntax checked with Node.js.
- Browser runtime test checked the general and patient-specific open paths and the patient-change handler.
- ZIP integrity checked; exactly 7 deployment files included.
- Live test on the user's phone has not been performed.
