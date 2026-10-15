DentalFlow V7.8.12 — Billing Cursor Fix

Fixes Enter after fee to add the treatment/fee item and return focus to Treatment / Service, even if another delegated Enter handler attempts to move focus. Fee input autocomplete/suggestions disabled.

Based on the supplied V7.8.10 billing fix archive.

DentalFlow V7.8.10 — Billing Enter & Fee Suggestion Fix

Base: DentalFlow V7.8.9 Blank Screen & Raw-Code Fix.

Fixes in this build:
- Treatment/service Enter moves to individual fee.
- Fee Enter commits the item, updates total, clears both inputs, and returns focus to treatment/service.
- Fee field is excluded from DentalFlow smart suggestions and browser autofill hints.
- Billing draft saving and visible item-count/total feedback retained.

Before deploying, export a JSON backup. Test with a dummy patient first. Android end-to-end testing is not confirmed.
