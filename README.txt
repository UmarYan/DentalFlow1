DentalFlow V7.8.69 — Materials Purchase Account Sync

Base: DentalFlow V7.8.68 Lab Expense Account Balance Sync.

Changes in V7.8.69:
- Materials Inventory Stock In now requires a valid existing Cash, Bank, UPI or other Finance account when Total purchase cost is greater than ₹0.
- The selected account is stored on the linked Materials expense, so the existing Finance account-balance calculation deducts the purchase amount from that account.
- A zero-cost stock-in can still be recorded without a payment account.
- The account check happens before stock or finance records are changed.
- Adding opening stock does not create a new Finance expense, because the opening stock may represent a purchase already accounted for.
- Existing stock, purchase, expense, lab, patient, clinical, appointment, billing and LocalStorage records are preserved; no data reset or new dependency added.

Deployment:
1. Export a DentalFlow backup before deployment.
2. Extract the ZIP and publish the contents of the DentalFlow folder to the existing GitHub Pages deployment.
3. Reload the app. If an older cached version remains, close/reopen the PWA or refresh after the service worker updates.

Rollback:
- Redeploy the prior DentalFlow V7.8.68 ZIP.
- Export a backup first and do not clear LocalStorage.

Automated checks performed for this build:
- JavaScript syntax checks for all inline scripts.
- Service-worker syntax check.
- HTML parsing and duplicate-ID scan.
- Manifest JSON parsing.
- ZIP integrity and required-file checks.
- Static and targeted logic checks for required account selection on paid stock-in, valid account assignment, and compatibility with Finance expense account-balance calculation.

Limitations:
- Browser end-to-end testing was not performed.
- The app records the selected account as the payment source; it does not independently verify that money was actually paid.
- Historical stock-in records without a linked expense are not retroactively converted to expenses, to avoid duplicate accounting.
