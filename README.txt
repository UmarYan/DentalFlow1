DentalFlow V7.9.58 — Treatment Plan Four-Line Cards

Base: DentalFlow V7.9.57_Four_Line_Cards_Download.zip (exact user-specified base).

Changes:
- Treatment Plan list cards now show four content lines: Patient Name; Date; Treatment Name/Items · Status; Estimated total.
- Removed Plan Title and Examination from the Treatment Plan list card only. Stored plan data and detail/edit workflows are unchanged.
- Preserved existing relevant action icons (Details/View, Edit, Schedule when applicable), search, and date-based collapsible grouping.
- Updated service-worker cache identifier to V7.9.58.

Validation performed:
- JavaScript syntax check with Node.js (inline scripts).
- HTML script-tag integrity/count check.
- ZIP integrity check.
- Browser testing was not performed.

Known limitations:
- Treatment item names are displayed in a single line and may truncate on narrow screens, consistent with the existing compact card styling.
- Confirm appearance and saved-data access after deployment.

Post-deployment checklist:
1. Open Treatment Plans and confirm the four lines and existing icons.
2. Search by patient and treatment item.
3. Open Details, Edit, and Schedule actions where available.
4. Verify existing patient and treatment-plan data remain present.

Rollback:
Redeploy the previously working V7.9.57 ZIP. Do not clear browser storage or LocalStorage.
