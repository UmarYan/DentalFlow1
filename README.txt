DentalFlow V7.9.25 - Compact Treatment Plans

Changes:
- Tightened Treatment Plan cards and item rows to reduce blank space and unnecessary wrapping on mobile.
- Replaced verbose plan actions with compact, accessible icon buttons.
- Kept existing Treatment Plan, appointment, billing, patient and LocalStorage record structures unchanged.
- Preserved the supplied V7.9.24 Simplified Patient Workflow as the source base.

Checks to perform before deployment:
- ZIP integrity, HTML parsing, inline JavaScript syntax, service worker syntax, manifest JSON parsing and targeted UI assertions.
- Real browser/mobile testing is not performed in this environment.

Rollback:
- Redeploy the original DentalFlow_V7.9.24_Simplified_Patient_Workflow_Download.zip to restore the previous version.
