DentalFlow V7.8.69 — Simple Finance & Automated Accounting

Base: DentalFlow V7.8.68_Script_Boundary_Fix.zip

Purpose
- Keep the everyday Clinic Finance workflow simple while retaining automated double-entry bookkeeping behind the scenes.
- Users continue to enter a transaction once; journal rows are generated from existing source records.

Changes
- Added a compact notice in Clinic Finance explaining that accounting entries are generated automatically and no manual Debit/Credit entry is required.
- Moved the detailed accounting journal, journal CSV export, Cash & Bank Reconciliation, and accounting notes into a collapsed-by-default “Advanced accounting & reconciliation” panel.
- Renamed the visible journal heading to “Accounting journal · Double-entry” inside the advanced panel.
- Preserved all existing journal-generation logic and source data mappings; no separate/manual duplicate payment ledger was introduced.
- Updated the page title, About DentalFlow label, and service-worker cache version.

Preserved
- Patient, clinical, appointment, treatment plan, billing/payment and receipt workflows.
- Clinic Finance transactions, patient receivables, supplier payables, opening balances, budgets, fund allocations, CSV exports, and reconciliation records.
- Existing LocalStorage schema and data keys. No data reset or migration was performed.

Important accounting limitations
- Journal entries are dynamically generated from current source records; this is not an immutable general ledger.
- Monthly income-less-expenses is an operational summary, not a tax-ready profit calculation.
- Opening balances are not represented as dated journal entries because the existing setup does not capture an opening-balance date or full offsetting equity account.
- Supplier payable and patient bill histories should be reviewed for historical consistency before formal reporting.
- This is an operational bookkeeping aid, not certified accounting or tax-compliance software. Seek an accountant’s review for statutory accounts and tax filing.

Validation
- ZIP integrity and required-file presence checked.
- HTML structure parsed; manifest JSON parsed; service-worker JavaScript syntax checked.
- Inline JavaScript syntax checked with Node.js.
- Accounting UI checks: journal and reconciliation remain present inside the collapsed advanced panel; all existing IDs and handlers retained.
- Browser end-to-end testing was not performed in this environment.

Deployment / rollback
- Export a fresh DentalFlow JSON backup before deployment.
- Do not clear LocalStorage during deployment.
- Roll back to DentalFlow_V7.8.68_Script_Boundary_Fix.zip if needed; do not clear LocalStorage.
