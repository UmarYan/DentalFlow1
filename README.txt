DentalFlow V7.8.0 — Visits & Billing Compact Cards

Base: DentalFlow V7.9.59_Card_Readability.zip (exact requested base).

Changes:
- Visits cards: patient name on line 1, visit time at the upper-right, examination content on line 2, and treatment-done content on line 3. Date is removed from each card; date-wise group headings remain. The Examination and Treatment Done labels are removed.
- Billing cards: patient name and payment status share line 1, treatment/service item names appear on line 2, and Total · Paid · Due appear on line 3. Date is removed from each card; date-wise group headings remain.
- Existing View, Edit, Payment (when due), and Receipt actions are retained.
- Treatment Plans layout and all underlying records/LocalStorage structures are unchanged.

Validation performed:
- JavaScript syntax check for inline scripts (Node.js).
- HTML script/style tag integrity check.
- ZIP integrity check.
- Browser testing was not performed.

Post-deployment checklist:
1. Verify Visits cards show time at top-right and examination/treatment content on separate lines.
2. Verify Billing cards show status at top-right and Total · Paid · Due on line 3.
3. Check date-wise grouping, visit search, billing search, and action icons.
4. Confirm existing records remain intact.

Rollback: redeploy the original V7.9.59 ZIP. Do not clear LocalStorage.
