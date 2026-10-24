DentalFlow V7.9.22 — Patient & Visit List Cleanup

Changes:
- Patient List cards show address and phone after the patient name; Patient ID is no longer shown in the visible card metadata.
- Clinical Visits cards show the actual complaint, examination finding, and treatment content without the labels “Complaint:”, “Examination:”, or “Treatment done:”.
- Patient IDs remain stored and searchable internally; existing linked records and LocalStorage structures are unchanged.
- Preserved prior Clinic Management tab layout and other existing functionality.

Base: DentalFlow V7.9.21 — Clinical Workflow Tab Spacing Fix.

Checks performed: ZIP integrity, HTML parsing, inline JavaScript syntax, service worker syntax, manifest JSON parsing, and targeted UI assertions. Real browser/mobile testing and existing LocalStorage regression testing were not performed.

Rollback: redeploy the previous DentalFlow V7.9.21 ZIP if needed. Do not clear LocalStorage.
