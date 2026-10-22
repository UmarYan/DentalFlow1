DentalFlow V7.9.0 — Refined Finance UI/UX

Base: DentalFlow_V7.8.70_Compact_Finance_Dashboard.zip (the approved stable base).

Purpose
- Refine Clinic Finance into a cleaner, more modern and sophisticated workspace.
- Reduce visual density and form scrolling on mobile without removing finance functionality.

Changes
- Applied a finance-scoped visual system with calmer surfaces, refined typography, consistent spacing, subtle borders and restrained semantic colours.
- Improved the sticky four-tab navigation and active-state clarity.
- Refined the overview hierarchy, compacted summary metrics and account balances, and tightened quick actions.
- Added progressive disclosure for optional transaction note and receipt/invoice attachment fields; their original IDs and handlers remain intact.
- Improved form controls, transaction rows, budget/fund rows, and advanced-accounting presentation across narrow and wider screens.
- Updated app title, About label, and service-worker cache version to V7.9.0.

Preserved
- Existing patient, clinical, appointment, treatment-plan, billing/payment, receipt and clinic workflows.
- Existing finance transaction logic, patient receivables, opening balances, supplier payables, budgets, fund allocations, CSV exports, automatic double-entry journal generation and reconciliation.
- Existing DOM IDs used by finance scripts, LocalStorage schema/data keys and transaction handlers. No data reset or migration was performed.

Validation
- ZIP integrity and required-file presence checked.
- HTML parsed; manifest JSON parsed; inline JavaScript syntax checked with Node.js.
- Verified finance form IDs and tab/panel names remain present and optional transaction fields remain accessible in the DOM.
- Automated structural checks passed. Full interactive browser end-to-end testing was not available in this environment.

Deployment / rollback
- Export a fresh DentalFlow JSON backup before deployment.
- Do not clear LocalStorage during deployment.
- If issues occur, roll back to DentalFlow_V7.8.70_Compact_Finance_Dashboard.zip without clearing LocalStorage.
