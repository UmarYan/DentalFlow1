DentalFlow V7.7.7 — Connected Patient Flow

Base: DentalFlow V7.7.6 Minimal Patient Profile Refresh (derived from the V7.7.5 stable base).

This update adds an optional, collapsible Patient Flow entry sheet for a single patient. It can record any combination of appointment, clinical visit, follow-up reminder, bill, and payment while retaining the existing separate screens and data model. Sections remain collapsed until needed. Existing localStorage key and existing record arrays are preserved.

Package contents: index.html, sw.js, manifest.json, icon.svg, icon-192.png, icon-512.png, README.txt. Replace all existing repository files with these package files after making an external JSON backup.

Validation: ZIP integrity and JavaScript syntax checks are run during packaging. These checks do not replace real-device workflow testing. Test with a test patient first: save appointment, visit, follow-up, bill and payment; reload; confirm links and amounts; then test backup/restore. Do not use an unverified build as the sole clinical record.
