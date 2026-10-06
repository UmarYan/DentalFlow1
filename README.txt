DentalFlow V4 — Treatment Planning

Based on the stable Clinical V3 Compact foundation.
Updates:
- Patient-specific Treatment Plans from the patient profile.
- Multiple treatment items per plan with tooth/area, procedure, priority, estimated cost, item status and notes.
- Quick-add procedure templates: RCT, Restoration, Crown, Extraction, Scaling, Prosthesis.
- Plan-level status: Proposed, Accepted, In progress, On hold, Completed.
- Automatic estimated total for each plan.
- Compact plan summary shown inside the patient profile.
- Edit and delete existing treatment plans.
- Existing dentalflow_v2 localStorage key retained for data continuity.
- Existing Clinical V3 tooth chart, clinical notes and navigation retained.
- No external libraries.

Recommended test:
Patient → Profile → + Plan → Add treatment items → Save → Profile → Edit plan → change item status → Reload.
Also test existing Clinical Visit and old patient/visit data after deployment.
