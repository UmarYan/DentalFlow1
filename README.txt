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


V7.9.29 — One-Line Treatment Entry
- Procedure, estimate, priority and status share one compact row on mobile.
- Planned-treatment rows use less height and a shorter bill action.
- No LocalStorage keys or existing record structures changed.


V7.9.30 — Compact UI Across Sections
- Applied consistent compact spacing to Patient, Visits, Billing, settings, summaries, forms, cards and expandable workflow sections.
- Reduced excess padding, gaps, field heights and card whitespace while preserving readable text and usable touch targets.
- Kept existing features, event handlers, LocalStorage keys and record structures unchanged; no data migration.

Checks performed for V7.9.30:
- ZIP integrity verified after packaging.
- HTML parser check performed.
- Inline JavaScript syntax checked with Node.js.
- Service Worker syntax checked with Node.js.
- Manifest JSON validated.
- Confirmed compact CSS override is present and version title updated.
- Real browser/Android interaction testing was not performed.

Rollback: redeploy DentalFlow_V7.9.29_OneLine_Treatment_Entry.zip.
