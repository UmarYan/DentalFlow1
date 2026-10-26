DentalFlow V7.9.59 — Card Readability Update

Base: DentalFlow V7.9.58_Treatment_Plan_Four_Line_Cards.zip (exact requested base).

Changes:
- Improved readability in Visits, Billing, and Treatment Plans list cards using a white background, a clearer border, darker primary text, and higher-contrast secondary text/action icons.
- Preserved card geometry, spacing, typography sizes, action icons, search, date-wise grouping, underlying data, and LocalStorage structures.
- Added a new service-worker cache identifier for V7.9.59.

Validation performed:
- JavaScript syntax check for inline scripts (Node.js).
- HTML script-tag integrity check.
- ZIP integrity check.
- Browser testing was not performed.

Post-deployment checklist:
1. Open Visits, Billing, and Treatment Plans and check small-text readability on mobile.
2. Check search, date-wise grouping, and existing action icons in all three sections.
3. Verify existing patient, visit, bill, and treatment-plan data remains present.

Rollback:
Redeploy the previous V7.9.58 ZIP. Do not clear browser storage or LocalStorage.
