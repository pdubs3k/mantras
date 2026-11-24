OUR WINS JOURNAL
================
A 6-month wins calendar + a mantra list that syncs live between you and a friend.
Open it, see the calendar, tap a day. Mantras are one tap away. Everything else
is behind the gear button.

ONE-TIME SETUP (about 15 minutes, only one of you does steps 1 and 2)

1. Make the free sync database (Firebase, free plan, no card needed)
   a. Go to console.firebase.google.com and sign in with a Google account.
   b. Create a project. Any name, e.g. our-wins. You can turn Analytics off.
   c. In the left menu, open Realtime Database (under Build) > Create Database.
      Pick any location, choose "Start in locked mode", then Enable.
   d. Open the Rules tab. Delete what's there, paste everything from
      firebase-rules.json (in this folder), and tap Publish.
   e. Open the Data tab and copy the address at the top. It looks like
      https://our-wins-xxxxx-default-rtdb.firebaseio.com

2. Put the journal online (free, GitHub Pages)
   a. Sign in at github.com. Click "+" > New repository, name it our-wins,
      make it Public, Create.
   b. Click "uploading an existing file", drag in ALL the files from this
      folder (the files, not the zip), then "Commit changes".
   c. Settings > Pages > Branch: "main", folder "/ (root)" > Save.
   d. After a minute your address shows at the top, like
      https://YOUR-NAME.github.io/our-wins/

3. Install it on both phones
   iPhone:  open the address in Safari > Share > "Add to Home Screen".
   Android: open it in Chrome > menu > "Add to Home screen" / "Install app".
   Always open it from the home screen icon after that.

4. Connect the two phones
   You:     open the icon > gear > "Start a new shared journal" > paste the
            database address from step 1e > Start > "Invite your friend"
            and send the invite in a message.
   Friend:  open their icon > gear > paste your whole invite message into
            "Got an invite?" > Join.
   Done. The top of the calendar says "Live with <name>" when it's working.

5. Daily reminder (each of you)
   Gear > pick a time > "iPhone calendar" (tap "Add All") or
   "Google Calendar" (check it repeats Daily, Save).
   It's a repeating calendar alert, so it fires even with the app closed.

GOOD TO KNOW
  - Privacy: there's no login. The invite contains a long random code
    (32 characters), and the database rules only let someone in who has that
    exact code. Anyone you send the invite to, or who sees it, can read and
    add to the journal. Only send it to your friend, and don't post it.
    The rules also stop anyone from wiping the journal in one go.
  - Offline: it still opens and saves with no signal. Changes sync the next
    time you're online.
  - iPhone: Safari and the home screen icon keep separate copies on the phone.
    Use the icon. (With sync on, both end up with the same journal anyway.)
  - Backup: gear > "Backup and more" > "Save a backup". Restoring a backup on a
    new phone brings back your wins as yours.
  - Calendar start month: gear > "Backup and more", or DEFAULT_START near the
    top of the script in index.html. Set to December 2026 (through May 2027).
  - Changed a file later? Bump VERSION in sw.js so phones load the new copy.
  - Free plan limits are far beyond what two people writing notes will use.
