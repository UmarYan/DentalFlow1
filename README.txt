DentalFlow V7.11.18 — Android Back Navigation Fix

Base: DentalFlow_V7.11.17_Print_Script_Fix.zip.

Change log:
- Installed SPA navigation-history handling after all application scripts so later script declarations cannot overwrite it.
- App view changes now add view state to browser history; Android/browser Back restores the previous DentalFlow view.
- Fallback routing: Patient Details → Patients, Visit Summary → Visits, other views → Home when history lacks a DentalFlow view state.
- Updated service-worker cache identifier to V7.11.18.
- No patient data structures or LocalStorage keys changed.

Validation performed:
- JavaScript syntax check of all inline JavaScript blocks and service worker.
- HTML script/style tag balance checks.
- ZIP integrity test.
- Browser/mobile runtime testing was not performed.

Post-deployment checklist:
1. Patients → Patient Details → Android Back should return to Patients.
2. Visits → Visit Summary → Android Back should return to Visits.
3. Test Android system Back button and edge-swipe gesture.
4. Confirm Home, Billing, and other navigation still work.
5. Confirm Home does not display JavaScript source text.

Rollback: redeploy DentalFlow_V7.11.17_Print_Script_Fix.zip.
