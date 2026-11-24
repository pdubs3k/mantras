MANTRAS
=======
Calendar log, per-person streaks and a mantra list, synced live between phones.

ALREADY UPLOADED THE OLD VERSION? UPDATE IT
  1. Open your our-wins repository on github.com.
  2. Click "Add file" > "Upload files". Drag in ALL the files from this
     folder (the files, not the zip), including font.woff2. Same names replace
     the old ones. Then "Commit changes". If font-italic.woff2 is there from
     an earlier update, it's no longer used and can be deleted or left.
  3. In Firebase: Realtime Database > Rules tab. Replace everything with the
     new firebase-rules.json and tap Publish (streaks need the new rules;
     skip this if you already did it for the streaks update).
  4. Wait a minute, then fully close and reopen the app on each phone,
     twice if needed. Your saved logs and sync carry over.
  The old home screen icon may keep its old name and picture. To get the new
  ones, delete the icon and add it to the home screen again. On iPhone, only
  do that while sync is on and shows "Synced", because removing the icon
  erases that phone's copy.

FIRST-TIME SETUP

1. Make the free sync database (Firebase, free plan)
   a. Go to console.firebase.google.com and sign in with a Google account.
   b. Create a project (any name). You can turn Analytics off.
   c. Left menu: Realtime Database (under Build) > Create Database.
      Any location, "Start in locked mode", Enable.
   d. Rules tab: replace everything with firebase-rules.json, Publish.
   e. Data tab: copy the address at the top
      (https://....firebaseio.com or https://....firebasedatabase.app).

2. Put it online (free, GitHub Pages)
   a. github.com > "+" > New repository > Public > Create.
   b. "uploading an existing file" > drag in ALL files > Commit changes.
   c. Settings > Pages > Branch "main", "/ (root)" > Save.
   d. Your address appears after a minute: https://YOUR-NAME.github.io/REPO/

3. Install on each phone
   iPhone:  Safari > Share > Add to Home Screen.
   Android: Chrome > menu > Add to Home screen / Install app.

4. Connect
   You:    open it, add your name, gear > Start a new shared journal >
           paste the address from 1e > Start > Send invite.
   Friend: open it, add their name, gear > paste the whole invite under
           Invite > Join.

5. Daily reminder (each phone): gear > pick a time > iPhone calendar
   (tap Add All) or Google Calendar (check it repeats daily, Save).

USING IT
  - Each time it opens, tap your name. Tap the name button at the top to switch.
  - Calendar: tap a day. Each person has one note per day, and that day's
    streak results are listed under each name. You can write your own note and
    log your own streaks there; everyone else's are shown read-only.
    Your days are white, others' are dark gray.
  - Streaks: "Add new streak", pick "Done / not done" or "Number" with a unit
    (minutes, reps, pages...). Log today from the streak row. Tap the streak's
    name for its full day-by-day log, where you can fill in or fix past days.
    Everyone sees everyone's streaks and logs. You can only change your own.
  - Days with a note from anyone show "..." under the date.
  - Mantras: tap Add at the bottom, write, tap Save. Line breaks you type are
    kept. Each one is signed with your name. Tap one of yours to edit or
    delete it; others' are read-only. The font is Cormorant Garamond (free,
    see FONT-LICENSE.txt) and works offline.

GOOD TO KNOW
  - Privacy: no login. The invite holds a 32-character random code, and the
    database rules only let in someone with that exact code. Anyone with the
    invite can read and add. Only send it to your friend.
  - Names aren't passwords. Anyone using the app can pick any name.
  - Works offline; changes sync when back online.
  - Backup: gear > Backup and more > Save a backup.
  - Calendar start month: gear > Backup and more (set to Dec 2026 to May 2027).
  - After changing any file yourself, bump VERSION in sw.js.
