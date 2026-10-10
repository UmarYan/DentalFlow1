DentalFlow V7.6.4 — Update 11: Patient Profile Billing Fix

WHAT CHANGED
- Fixed the Patient Profile “+ Bill” button. Its generated onclick handler had a malformed patient-ID expression, so tapping it could fail instead of opening the bill form.
- Kept the existing billing flow, linked Treatment Plan/Clinical Visit selectors, patient data key, and all earlier features.
- Updated the service-worker cache namespace so the browser can pick up this release rather than reusing the previous app cache.

DEPLOY
1. Export an external JSON backup first.
2. Extract this ZIP.
3. Replace the current 7 GitHub Pages files with the 7 files in this ZIP.
4. Open a Patient Profile and tap “+ Bill”. Confirm the Bill form opens with that patient selected. Add a test bill only if appropriate; do not create a real financial record just for testing.
5. Also test + Clinical Visit, + Plan, existing Bill Details, and reload the app.

VALIDATION
- Inline JavaScript syntax checked with Node.js.
- ZIP integrity and exact 7-file package checked.
- Static check confirmed the corrected profile bill handler is present and the malformed handler is absent.
- Live testing on the user's phone has not been performed.
