DentalFlow V7.8.27 — Compact Patient Rows & Context Actions — Print Script Fix

Base: DentalFlow V7.8.19 — Chairside Workflow Revamp.

Implemented in this update:
- Removed the legacy extra Home follow-up strip that duplicated follow-ups already shown in the Follow-up workspace; the single main Follow-up list remains the clearly labeled source.
- Compact follow-up/reminder cards reduce vertical padding, typography and action spacing while preserving usable touch targets.
- Today groups/cards use green accents; Overdue groups/cards use red accents.
- Home now embeds the paired Appointments / Queue workspace and Follow-up / Reminders workspace.
- Home paired workspaces support both tab taps and independent horizontal swipe; tab active state stays in sync.
- Primary bottom navigation is Home, Patients, Visits, Finance, More.
- Primary workspace navigation supports horizontal swipe between Home, Patients, Visits, Finance and More, while vertical scrolling remains available.
- More provides organized access to Appointments & Queue, Follow-ups & Reminders, Treatment Plans, Reports, Global Search, Settings, Backup and Restore.
- Finance is the renamed bottom-navigation entry for the existing Billing & Payments view; underlying billing/payment view and data remain unchanged.
- Home shows the same rendered appointment, queue, follow-up and reminder records from the existing modules rather than creating duplicate records.
- Queue rendering is explicitly refreshed as part of the main render cycle so the Home Queue panel stays synchronized.
- Existing patient, clinical visit, treatment/service, billing, payment, smart suggestion, backup/restore and record structures were retained.

Interaction safeguards:
- Horizontal navigation ignores inputs, textareas, selects, buttons, modal sheets, and paired tab controls.
- Home paired-workspace swipe is independent from primary navigation swipe.
- Appointment, queue, follow-up and reminder statuses remain separate; completion does not cascade to unrelated records.
- This is an in-app reminder experience; SMS, WhatsApp and push notification delivery are not added in this update.

Validation performed: JavaScript syntax checks passed; duplicate HTML IDs check passed; ZIP integrity check performed after packaging. Full Android/browser end-to-end interaction testing has not been performed here, so test on a backup/test dataset before production deployment.


V7.8.24 update notes
- Compact-by-default patient cards across appointments, queue, follow-ups and reminders; tap the card body to expand optional details. Action buttons remain visible and independently tappable.
- Appointment cards use red for overdue dates, green for today, and blue for upcoming dates. Queue cards for today use green status styling.
- Clinical Visits are grouped by date, with newest dates first and items sorted by time within each date. Home Today's visits also shows a date group.
- Existing records and core data structures are retained.
- Validation: ZIP integrity and inline JavaScript syntax checked. Full Android end-to-end testing has not been performed.


V7.8.24 — Shared Collapsible Date Groups & Clinical Visit Chronology
- Clinical Visits are grouped Today, Future-dated visits (when present), Recent Visits (previous 7 days), and Older Visits. Clinical visits are never labeled Overdue merely because their date is in the past.
- Date/status groups across appointments, queue, follow-ups, reminders, and history lists use collapsible headers with counts. Today/Overdue active groups default open; upcoming/completed/older groups default closed where applicable.
- Multiple groups may remain open; toggled state is preserved while the page remains open.
- Compact-by-default expandable visit cards remain in place; existing records and data structure are not intentionally changed.
- Validation is limited to ZIP integrity and static JavaScript/HTML checks; no full Android end-to-end test performed.


V7.8.24 Compact Row UI: reduces patient-card padding and typography, keeps action buttons hidden until the row is expanded, exposes a three-dot action toggle, and supports optional long-press to reveal the same actions. Existing action handlers and record structures are retained. Full Android end-to-end testing has not been performed.


V7.8.27 — Actual Compact Patient Row + Context Bottom Sheet
- Converted rendered appointment, queue, follow-up, reminder and clinical visit cards to compact two-line rows: primary name/time and small secondary metadata/status.
- Removed always-visible large action buttons from each row; actions are retained in the source markup and presented in a contextual bottom sheet through the three-dot button or optional long press.
- Tapping the row/name opens the context sheet with the record's current status, metadata and applicable existing action handlers.
- The three-dot menu and long press open the action-focused version of the same sheet; no action executes merely from long press.
- Context actions clone existing action buttons/handlers rather than creating or linking new records. Existing record IDs and data model are unchanged.
- Kept overdue/today/upcoming visual accents and collapsible date groups. Patient list rows also use reduced spacing and type scale.
- Validation: ZIP integrity, inline JavaScript syntax and duplicate HTML IDs checked. Full Android end-to-end interaction testing has not been performed.

V7.8.27 hotfix: fixed script placement that caused JavaScript from the main app to appear as visible text on screen. The print receipt document string is restored; the compact-row context script remains only at the end of the app document.


V7.8.27 changes: removed three-dot menus and contextual popup sheets from compact rows. Tapping a row expands its action icons inline in a single horizontal line. Patient list/search rows reveal profile, new visit, new appointment, and edit actions inline. Patient timeline and clinical visit lists display dates instead of times for visit entries.
