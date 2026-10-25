DentalFlow V7.9.27 - Compact Treatment Plan Cards

Changes:
- Fixed the Treatment Plans card layout on Patient Details. The context-row grid was forcing card children into narrow columns, causing the large blank area and awkward wrapping shown in the supplied screenshot.
- Treatment plan cards now use a full-width compact flow; treatment, status, fee and actions stay close together and use fewer lines where practical.
- Kept the existing quick-pick and custom treatment entry.
- No patient, clinical, treatment-plan, appointment, billing, payment or LocalStorage data structures were intentionally changed.

Checks performed:
- ZIP integrity checked.
- HTML parser check performed.
- Inline JavaScript syntax check performed with Node.js where available.
- Service Worker syntax and manifest JSON checked.
- Targeted assertions checked for the new scoped CSS, treatment-plan renderer and retained quick-pick.
- Real browser/Android interaction testing was not performed in this environment.

Rollback:
- Redeploy DentalFlow_V7.9.26_Treatment_Quick_Pick.zip.
