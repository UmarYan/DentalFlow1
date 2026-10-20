DentalFlow V7.8.46 — Context FAB Direct Entry

Base: V7.8.42 Finance Layout Unified, carrying forward the V7.8.43 smart-workflow implementation.

Base: DentalFlow V7.8.45 — Script Boundary Fix.

Changes in this build:
- FAB tap now opens the relevant entry form directly; it no longer expands a list of “New …” options.
- FAB action follows the active context: patient workflow, patient, clinical visit, appointment or queue walk-in, bill, follow-up or reminder, patient record, or current patient workflow.
- Removed standalone add buttons from the header and the Clinical Visits, Appointments, Queue, Follow-ups and Billing section headers.
- Bumped the service-worker cache key so deployments do not reuse the previous cached app.
- Preserved existing patient/clinical data structures, LocalStorage keys, unrelated screens and workflows.

Validation performed: ZIP integrity, Node syntax checks for all 10 extracted inline script blocks, HTML parser integrity check, and static checks for requested button removals and direct FAB dispatch. Browser end-to-end testing was not performed. Back up existing clinic data before deployment.
