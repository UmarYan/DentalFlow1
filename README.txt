DentalFlow V7.5.2 — Smart Patient & Custom Options
Based directly on the stable DentalFlow V7.5.1 Smart Input foundation.

Updates:
- Patient selection fields are type-first Smart Patient Inputs instead of native dropdowns.
- Existing patients appear as matching suggestions while typing.
- A new patient can be created directly from the patient input with name only; remaining details can be edited later.
- Long-press an existing Smart Input suggestion to remove it from the suggestion list without deleting clinic data.
- Long-press a patient suggestion to hide it from Smart Patient suggestions; the patient record is not deleted.
- Examination, Diagnosis and Treatment Problem/Action pickers now support custom options.
- Add a new Problem/Action option from the picker menu.
- Long-press custom Problem/Action options to delete them; built-in options are protected.
- Existing dentalflow_v2 data key and all previous clinic data are retained.
- Service worker cache updated to V7.5.2.

Recommended test:
1. Open a new Clinical Visit and type a patient name.
2. Select an existing patient; then try a new name and use Add new patient.
3. Open Examination / Diagnosis / Treatment Problem/Action menu.
4. Add a custom option and verify it appears later.
5. Long-press a Smart Input suggestion, a patient suggestion, and a custom Problem/Action option to verify delete behavior.
6. Reload the app and confirm existing data remains intact.
