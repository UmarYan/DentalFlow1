DentalFlow V7.9.6 — Automatic Payables

Changes: Dues labels Receivables and Payables; Supplier Payables entry is separated from the outstanding Payables list; expense entries can be marked Unpaid and automatically added to Payables without reducing cash/bank balances until payment is recorded.

Base package: V7.9.5 Finance Workspace Refinement.

DentalFlow V7.8.70 — Compact Finance Dashboard

Base: DentalFlow V7.8.69_Simple_Finance_Automated_Accounting.zip

Purpose
- Reduce excessive vertical scrolling in Clinic Finance without removing existing finance tools.
- Organize finance into four compact sections: Overview, Transactions, Accounts, and Reports.

Changes
- Added compact, sticky four-tab navigation within Clinic Finance.
- Overview retains the monthly financial summary and account balances, with quick links to transactions, accounts/dues, and reports.
- Transactions groups the existing new-transaction form and transaction list.
- Accounts groups patient receivables, opening balances, and supplier payables.
- Reports groups budgets, fund allocations, expense-category reporting, and the collapsed Advanced Accounting & Reconciliation section.
- Added compact mobile spacing and summary tiles while preserving the existing finance forms and transaction handlers.
- The selected finance tab is remembered for the current browser session only.
- Updated app title, About label, and service-worker cache version.

Preserved
- Patient, clinical, appointment, treatment plan, billing/payment, and receipt workflows.
- Existing Clinic Finance transaction records, receivables, payables, opening balances, budgets, funds, exports, journal generation, and reconciliation records.
- Existing LocalStorage schema and data keys; no data reset or migration was performed.
- Existing transaction creation and accounting-generation logic.

Validation
- ZIP integrity and required-file presence checked.
- HTML parsed; manifest JSON parsed; inline JavaScript syntax checked with Node.js.
- Verified all original finance form/list IDs remain in the HTML and all four tabs map to their intended panels.
- Full browser end-to-end testing was not performed in this environment.

Deployment / rollback
- Export a fresh DentalFlow JSON backup before deployment.
- Do not clear LocalStorage during deployment.
- If issues occur, roll back to DentalFlow_V7.8.69_Simple_Finance_Automated_Accounting.zip without clearing LocalStorage.


V7.9.5 Change log: Finance navigation now uses five horizontally scrollable tabs: Overview, Transactions, Dues, Planning and Miscellaneous. Transactions title row has New/Search/Filter icons; Budget and Allocation forms open from their title-row plus icons. Expense Category Report moved to Miscellaneous immediately after Opening Balances.
