DentalFlow V7.8.12 — Unified Smart Suggestions

Changes:
- Restores the same type-first smart-suggestion behavior across mapped single-entry fields and the continuous Patient Workflow multi-entry fields.
- Previous entries can be tapped to use/add them.
- Typed new entries can be saved to suggestions with the blue “＋ Add … to suggestions” action.
- Each previous suggestion has an × action to remove it from the suggestion list only; it does not delete patient, visit, plan, bill, or other clinical records.
- Applies to mapped fields including Treatment/Service, Chief Complaint, Examination, Diagnosis, History, Treatment Done, Prescription, Advice, Plan Procedure, Appointment Reason, and other mapped smart-suggest fields.
- Individual Fee/amount fields remain excluded from suggestions.
- Keeps existing multi-entry Enter-to-add behavior and the existing patient workflow.
- Updates the service-worker cache name so the new interface can load after deployment.

Deployment / safety:
- Export a JSON backup before replacing deployed files. Do not clear Chrome site data.
- Replace repository files with the ZIP contents.
- Test with a fictional patient first; confirm old suggestions, add, tap-to-use, and delete-suggestion-only behavior on Android.

Validation:
- Inline JavaScript syntax checked with Node.js.
- ZIP integrity checked during packaging.
- Real Android end-to-end testing, live deployment, and data migration have not been verified in this environment.
