DentalFlow V7.9.4 — Finance Navigation & Action Refinement

Source base: DentalFlow_V7.8.70_Compact_Finance_Dashboard.zip (approved stable base)

Purpose
- Reduce excessive vertical scrolling in Clinic Finance without removing existing finance tools.
- Organize finance into five compact sections: Overview, Transactions, Dues, Planning, and Miscellaneous.

Changes
- Added compact, sticky five-tab navigation within Clinic Finance.
- Overview retains the monthly financial summary and account balances, with quick links to transactions, accounts/dues, and reports.
- Transactions groups the existing new-transaction form and transaction list.
- Dues contains only patient receivables and supplier payables. Miscellaneous starts with opening balances.
- Planning groups Budgets, Allocations, and expense-category reporting. Miscellaneous contains Advanced Accounting & Reconciliation after opening balances.
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
- Verified all original finance form/list IDs remain in the HTML and all five tabs map to their intended panels.
- Full browser end-to-end testing was not performed in this environment.

Deployment / rollback
- Export a fresh DentalFlow JSON backup before deployment.
- Do not clear LocalStorage during deployment.
- If issues occur, roll back to DentalFlow_V7.8.70_Compact_Finance_Dashboard.zip without clearing LocalStorage.


V7.9.4 — Finance Navigation & Action Refinement
- Finance tabs reorganized into Overview, Transactions, Dues, Planning and Miscellaneous.
- Dues contains patient receivables and supplier payables only.
- Planning contains Budgets, Allocations and expense-category planning report.
- Miscellaneous starts with Opening Balances, followed by advanced accounting and reconciliation.
- Transactions header provides icon actions for new transaction, search and filter.
- Budget and allocation forms are collapsed by default and open from their title-row action icons.
- Existing finance data keys and calculation logic preserved from V7.8.70 base.
