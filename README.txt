DentalFlow V7.8.1 — Billing & Treatment Plans Status/Action Layout

Base: DentalFlow_V7.9.59_Card_Readability.zip (exact requested base).

Changes:
- Billing cards: patient name, date, service/treatment items, and Total · Paid · Due are displayed as four content lines. Status is placed at the upper-right, with existing action icons arranged horizontally beneath it.
- Treatment Plan cards: patient name, date, treatment items, and estimated total are displayed as four content lines. Status is placed at the upper-right, with existing action icons arranged horizontally beneath it.
- Preserved Billing payment, view, edit, and receipt actions; preserved Treatment Plan details, edit, and scheduling actions.
- Preserved search, date-wise grouping, stored records, and LocalStorage data structures.
- Updated service-worker cache identifier to V7.8.1.

Validation performed:
- JavaScript syntax check for all inline scripts (Node.js).
- HTML script/style tag integrity check.
- ZIP integrity check.
- Browser testing was not performed.

Post-deployment checklist:
1. Open Billing and verify status is in the upper-right and action icons are horizontal directly beneath it.
2. Verify the four Billing content lines and Total · Paid · Due.
3. Open Treatment Plans and verify status/action placement and the four content lines.
4. Test Payment, View, Edit, Receipt, Plan Details, Edit, and Schedule actions where available.
5. Verify search, date-wise grouping, and existing patient/billing/plan records.

Rollback:
Redeploy the previous DentalFlow V7.9.59 ZIP. Do not clear browser storage or LocalStorage.
