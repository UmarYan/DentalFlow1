DentalFlow V7.7.8 — Minimal Patient Profile Refresh

Base: V7.7.7 Connected Patient Flow, with the user's selected V7.7.5 stable baseline lineage.

This update redesigns the Patient Profile screen only:
- compact identity header with patient ID, age/gender and medical alert
- compact contact details
- one prominent Clinical Visit action
- compact counts for visits, plans, bills and appointments
- collapsible Tooth Status, Treatment Plans, Billing & Payments, Patient Timeline and Clinical Visit History
- secondary Edit, Patient Record and Delete actions tucked into a More menu
- visit details expand only when needed

Existing record structures, localStorage keys and other screens are preserved. This is a UI refactor, not a claim of full end-to-end clinical testing. Test with a dummy patient and export a backup before deployment.
