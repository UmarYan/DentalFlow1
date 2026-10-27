DentalFlow V7.11.1 — Patient Workflow Follow-up/Billing Order

Base: DentalFlow_V7.11.0_Patient_Workflow_Section_Order.zip.

Change log:
- Moved the existing Follow-up section to immediately after Treatment plan and before Billing & payment.
- All section contents and other UI areas remain unchanged.
- No data schema or LocalStorage changes.
- Updated the app version and service-worker cache identifier to V7.11.1.

Validation performed:
- JavaScript syntax check of all inline JavaScript blocks (Node.js).
- HTML script/style/details tag balance checks.
- Confirmed requested Patient Workflow section order.
- ZIP integrity test.
- Browser/UI runtime testing was not performed.

Post-deployment checklist:
1. Open Patient Workflow and confirm Follow-up appears directly after Treatment plan and before Billing & payment.
2. Expand Follow-up and Billing & payment and verify their fields and interactions.
3. Confirm Patient record / document and Reminder / task remain after Billing & payment.
4. Confirm the history button, draft note, Discard draft, and Save & Finish remain unchanged.
5. Test with an existing patient; confirm existing records remain intact.

Rollback:
Redeploy DentalFlow_V7.11.0_Patient_Workflow_Section_Order.zip. Do not clear LocalStorage.

Version 7.11.2 change log
- Link clinical visits to their selected treatment-plan item even when no appointment record is used; preserve existing status and data behavior.

Version 7.11.3 change log
- Carry treatment-plan item identity into bill items and prevent duplicate plan-to-bill additions while retaining legacy name/fee fallback.

Version 7.11.4 change log
- Final cumulative workflow update: visit-plan item linkage, identity-based plan-to-billing deduplication, and follow-up-linked reminder/task creation.
