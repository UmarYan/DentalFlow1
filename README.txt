DentalFlow V7.9.26 - Treatment Quick Pick

Changes:
- Added a compact native quick-pick list for common treatment names in Patient Workflow.
- Custom procedure names remain supported by free-text entry.
- No default fees are assumed; enter the clinic's actual estimate for each treatment.
- Kept the supplied V7.9.25 patient, clinical, treatment plan, appointment, billing, payment and LocalStorage structures unchanged.

Checks performed:
- ZIP integrity checked.
- HTML parser check performed.
- Inline JavaScript syntax check performed where supported.
- Manifest JSON and service worker syntax checked.
- Targeted assertion confirmed the treatment quick-pick is present and custom text input remains enabled.
- Real browser/mobile interaction testing was not performed in this environment.

Rollback:
- Redeploy DentalFlow_V7.9.25_Compact_Treatment_Plans.zip.
