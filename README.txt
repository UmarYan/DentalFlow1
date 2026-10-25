DentalFlow V7.9.28 — Compact Workflow Forms

Changes:
- Compactened the Treatment Plan editor: reduced field spacing, smaller quick-pick buttons, tighter item rows, and a more compact estimated-total area.
- Quick-pick procedures wrap neatly instead of forcing a horizontally clipped row.
- Compactened Patient Workflow section headers, fields, bill items and billing summaries.
- Advanced existing-bill collection and extra billing options start collapsed in a fresh workflow; open them when needed. Existing functionality remains available.
- Kept the existing plan, visit, billing and payment logic and LocalStorage structures unchanged.
- No intentionally removed features or data migrations.

Checks performed:
- ZIP integrity tested after packaging.
- HTML parser check performed.
- Inline JavaScript syntax checked with Node.js.
- Service Worker syntax checked with Node.js.
- Manifest JSON validated.
- Targeted checks verified compact CSS, quick-pick controls, plan item renderer and workflow billing controls remain present.
- Real browser/Android interaction testing was not performed.

Rollback:
- Redeploy DentalFlow_V7.9.27_Compact_Treatment_Plan_Cards.zip.
