# WesStudy Public Starter v1.0

## Changes
- Fresh browser origin/state starts with zero subjects, zero sessions, zero degree modules, zero study plans, and no timetable.
- Removed the embedded HKA lecture/work schedule and automatic semester attendance from both the standalone `app.js` and the actual inline script in `index.html`.
- First-use welcome dialog guides the user to set up the semester.
- Uses `wesstudy_public_v1` browser storage to avoid reading the creator’s pre-existing `wesstudy_v1` data.
- Creator's Firebase project configuration was removed. Cloud sync is OFF until a new Firebase project is configured by the publisher.
- Existing import/export remains available; importing a backup intentionally imports that backup's contents.

## Deployment / security
1. Host on HTTPS (for example GitHub Pages). The app uses browser local storage by default.
2. For public Google sign-in/cloud sync, configure an independent Firebase project, enable Google Auth, verify Firestore rules, restrict authorized domains and test isolated test accounts. The supplied `firestore.rules` enforces per-UID access; **rules must actually be deployed**.
3. Test with browser private window/new profile, using DevTools console for errors.
4. Check any existing old site/browser's local data and Firebase cloud data separately: this distribution does NOT delete or modify them.
5. Review data protection, privacy policy and store requirements before public release.

## Limits / future work
- This is a first-user clean starter, not a complete commercial multi-user launch.
- Semester/degree configuration remains oriented toward the existing German student planner model.
- There is no payment, subscription, hosted backend, or privacy-policy setup yet.
