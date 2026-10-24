DentalFlow V7.9.3 — Unified Treatment Workflow

Base: DentalFlow V7.9.2 Treatment Plan Workflow.

Changes in V7.9.3:
- Replaced the separate Tooth/Area selector in Treatment Plan item entry with one Treatment / Service Name field. Tooth or area can be included in that name. Legacy plan items keep their previous tooth information, displayed together with the service name.
- Added service-name suggestions from existing bills, plans, and clinical visits to reduce repeated typing.
- Clinical Visit now has independent optional Create Treatment Plan and Create Bill actions. Patient, examination, diagnosis, chief complaint, treatment done, and visit link are carried into the next form when relevant. Multiple lines in Treatment Done are prefilled as separate bill items, with fees to review.
- Treatment Plan has an optional Create Bill action. Completed and In progress items are prefilled; Planned items are not automatically billed. The Bill form also lets the user explicitly select other items from the linked plan. Fees remain editable before saving.
- Patient Workflow keeps its optional Treatment Plan action and now has an explicit optional Create Bill choice. Adding a billing item selects it automatically; unchecking the option saves the workflow without creating a bill. If both plan and bill are requested before bill items exist, the plan is saved first and billing opens afterwards.
- Bills created from Clinical Visit / Treatment Plan retain visit and/or plan references.
- No data reset or blanket migration; existing patient, clinical, appointment, billing, finance, inventory, laboratory, and LocalStorage records are preserved.

Checks performed:
- Inline JavaScript syntax checks (all inline scripts).
- Service worker syntax check.
- HTML parsing, duplicate ID scan, manifest JSON validation, and ZIP integrity check.
- Targeted static checks for unified treatment-name rendering, optional plan/bill hand-off, and recent-service suggestions.
- Browser launch was attempted in headless Chromium but blocked by the environment; no browser E2E test is claimed.

Deployment:
1. Export a DentalFlow backup before deployment.
2. Extract the ZIP and publish the contents of the DentalFlow folder to the existing GitHub Pages deployment.
3. Test Patient Workflow, Clinical Visit, Treatment Plan add/edit, service suggestions, and each optional next-step combination.
4. Confirm planned items are not automatically billed and review all fees before saving a bill.

Rollback:
- Redeploy DentalFlow V7.9.2_Treatment_Plan_Workflow.zip.
- Export a backup first and do not clear LocalStorage. New records use the existing collections; older versions may not display the newer visit/plan link fields.
