DentalFlow V7.9.5 — Patient Workflow Cleanup

Base: user-designated stable base DentalFlow_V7.9.2_Navigation_Data_Security.zip (V7.9.2).

Change log
- Removed the tooth chart, individual tooth/area selection and status editor, tooth-context sheet, profile tooth chips, and tooth/area fields from new clinical, treatment-plan, billing, and laboratory forms.
- Removed the corresponding tooth-specific picker, chart-rendering, context and hide-only helper code.
- Kept Patient Workflow as the unified creation entry point and retained the single Patient Workflow FAB.
- Kept existing saved records and legacy tooth-related properties in stored data for backward compatibility; no patient or clinical data was cleared or migrated.

Checks performed: HTML parser, inline JavaScript syntax checks, service-worker syntax, manifest JSON parsing, ZIP integrity, and static checks for removed tooth-chart UI/handlers. Browser-based testing was not performed.
