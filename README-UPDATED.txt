SPES HUB - UPDATED FRONT-END PROTOTYPE

HOW TO RUN
1. Extract the ZIP file.
2. Open the spes-hub folder.
3. Run index.html in a modern browser, or serve the folder using VS Code Live Server.
4. Demo staff accounts:
   Admin: username admin / password admin123
   Office Head: username head / password head123
5. Admin can create B1 and B2 batches (for example, name them B1 - 2026 and B2 - 2026).
6. Beneficiaries register using the batch code. The app generates a SPES ID in the format B1-2026-0001 or B2-2026-0001.

CHANGES INCLUDED
- Attendance image submissions remain Pending until administrator review.
- Attendance is separated into Morning Time-In, Morning Time-Out, Afternoon Time-In, and Afternoon Time-Out.
- Upload now asks for confirmation with Cancel and Submit image actions.
- Admin review screen displays uploaded proof photos and allows Approve or Reject.
- Full day requires approved morning and afternoon in/out slots; one fully approved half-day is labeled Half day.
- Saturday and Sunday are rest days and excluded from the 20-day work schedule.
- Friday is Work From Home, requires no attendance upload, and remains counted in the 20 scheduled workdays.
- Registration includes Male/Female and generates a unique SPES ID.
- Admin batch classroom cards include name/SPES ID search, attendance counts, journal entries/photos, scores, and account deletion.
- Theme toggle is placed at the upper-right of the app.
- Game room navigation uses the shared click handler; Next is blocked until the current item is answered; small hints are available.
- Existing records marked "verified" are migrated to "approved" in browser storage.

IMPORTANT LIMITATIONS
This ZIP is still a front-end prototype. It uses browser localStorage and sessionStorage. Data is stored only in the browser/device where it is used; it is not shared across users or computers. The demo passwords are plain text and are not secure. Admin-only controls are enforced in the interface code but are not secure server-side authorization. Uploaded images are compressed into browser storage. For actual deployment, connect a PHP/MySQL backend with password hashing, server-side role checks, secure image upload validation, audit logs, and database-backed attendance approvals. Do not use real beneficiary personal information until those backend protections are implemented.

ATTENDANCE RULES IN THIS PROTOTYPE
- Morning Time-In: before 8:00 AM
- Morning Time-Out: 12:00 PM onwards
- Afternoon Time-In: before 1:00 PM
- Afternoon Time-Out: 5:00 PM onwards
- Every photo submission is Pending until Administrator approval.
- System submission time is recorded by the browser in this prototype; a production system must use server time.

LATEST UPDATE (November 2026)
- Quiz progression is locked until the current question is answered correctly. Incorrect answers can be retried; they do not advance to the next question.
- Removed the in-game hint feature.
- Replaced the role text beside the theme control with a more visible Light mode / Dark mode switch featuring an icon and toggle indicator.
- Added an editable Gender identity field to the beneficiary Profile page (Male/Female options, matching the existing registration fields).
