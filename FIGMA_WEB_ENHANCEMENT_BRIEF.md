# Monthly Salary Recap — Final Enhancement Brief

## SOURCE OF TRUTH
Use `index.html` as the working application. Preserve its functionality and data logic.
Do NOT replace the working app with a static mockup or screenshot.

## BRAND / VISUAL DIRECTION
- Premium, clean, professional salary-management app.
- Main theme: Jet Black → Graphite/Silver gradients with white typography.
- Keep the interface decent and compact; avoid excessive decoration.
- Strong bold section headings, consistent spacing, aligned fields and cards.
- Rounded cards with subtle borders/shadows.
- IN button: green gradient. OUT button: red gradient.
- Main cards: black/graphite/silver gradient.
- Menu button: three vertical dots.
- Use the supplied Monthly Salary Recap icon files exactly; do not redesign the icon.

## HEADER / NAVIGATION
- App title: Monthly Salary Recap
- Subtitle: Salary • Attendance • Overtime • Pocket Expenses
- Three-dot menu opens a working side drawer.
- Drawer contains:
  Dashboard
  Attendance
  Expenses
  Monthly Recap
  Khata / Udhar
  Settings
- Dashboard/Attendance/Expenses/etc. should NOT appear as a separate row of large navigation buttons on the main dashboard.

## SALARY PERIOD
The app supports a custom From Date and To Date.
Examples:
- 06/09 → 06/10
- 10/09 → 10/10
- 05/09 → 05/10
All dashboard calculations and recap/export data must respect the selected period.

## ATTENDANCE
- TIME IN and TIME OUT work automatically using the current time.
- If the user forgets a day, Attendance has manual entry:
  Date, Time In, Time Out, Optional Manual OT.
- Manual entry can update an existing date.
- Work duration is calculated from In/Out.
- Normal duty hours are configurable.
- Working-day OT = hours above normal duty.
- Weekly off-day: all worked hours are OT.
- Manual OT is added separately to automatic OT.
- Display Auto OT, Manual OT and Total OT separately where appropriate.

## OT RATE — CRITICAL
OT rate is PER HOUR, not per minute.
Example:
- OT Rate = Rs. 100/hour
- 4 hours OT = Rs. 400
- 24 hours OT = Rs. 2,400
Never multiply the hourly rate directly by minutes.

## EXPENSES
Pocket expenses are separate from salary calculation records but are included in payable/receivable totals according to the current app logic.
Allow date, expense name, amount and note.

## KHATA / UDHAR
This is completely separate from salary, overtime and pocket-expense calculations.
Fields:
- Name
- Phone / Number
- Amount
- Date
- Note
Functions:
- Save
- Edit
- Delete
- Total Udhar
Do not merge Khata/Udhar with salary calculations.

## EMPLOYEE / SALARY
Settings contain:
- Employee Name
- Monthly Salary
- Normal Duty Hours
- OT Rate per Hour
- Weekly Off Day
The current employee name and salary should be clearly shown.
Do not silently remove this feature.

## MONTHLY RECAP / CSV EXPORT
Export must be a real CSV with separate spreadsheet columns, NOT one long string in a single cell.

Daily columns:
Date | Time In | Time Out | Total Work | Auto OT | Manual OT | Total OT | Type

Each date must occupy its own row.
The selected salary period controls which dates are exported.
The export should also contain a summary section for:
- Basic Salary
- OT Hours
- OT Amount
- Pocket Expenses
- Total Payable

Use CRLF line breaks and UTF-8 BOM for spreadsheet compatibility.

## DATA / FUNCTIONALITY
- Preserve localStorage persistence.
- Do not turn the application into a screenshot/mockup.
- Do not remove working buttons.
- Three-dot drawer, IN, OUT, manual attendance, expenses, settings, Khata/Udhar, backup, clear-data and CSV export must remain functional.
- Existing saved data should remain compatible where possible.

## APP ICON
The package contains:
app-icon-48.png
app-icon-72.png
app-icon-96.png
app-icon-144.png
app-icon-192.png
app-icon-512.png

Use `app-icon-512.png` as the master visual. The icon is the Monthly Salary Recap calendar + rupee + clock + chart artwork supplied for this app.

## IMPORTANT FOR ANY FUTURE DESIGN PASS
Improve only the visual layer unless a functional bug is explicitly being fixed.
Do not replace the working HTML/JavaScript with a static design.


## EASY PRINT BRANDING UPDATE
Show the exact supplied easy-print-solution-logo.png in the app header. Do not change the Monthly Salary Recap app icon; do not use the Easy Print logo as the install icon. Brand colors may influence UI accents, but keep business data and logic untouched.
