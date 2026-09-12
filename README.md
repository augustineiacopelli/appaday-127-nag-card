# Nag Card

**AppADay #127**

Type the one important thing you cannot forget today. That is the whole setup. From there Nag Card leaves it on screen and gets progressively harder to ignore the longer it stays open.

## How it escalates

- 0 to 2 minutes: calm blue, normal size, no motion
- 2 to 5 minutes: warms slightly, text grows a little
- 5 to 10 minutes: orange, gentle pulse animation begins
- 10 to 20 minutes: deeper orange, faster pulse, phones get a short vibration
- 20 to 40 minutes: red, stronger pulse, bigger vibration pattern
- 40+ minutes: full alarm red, the card shakes, vibration pattern repeats

Switching away from the tab makes the browser title blink your reminder text so it is visible in the tab bar. Coming back to the tab triggers a quick white flash to grab your attention. All of this resumes correctly on refresh since the start time is stored locally.

Mark the task done and the app resets to calm, logs a quiet completion count, and lets you set the next one. There is also a low-key "not doing this one" link for abandoning a reminder without counting it as a win.

## Tech

Single self-contained `index.html`. No frameworks, no build step, no backend. State lives entirely in `localStorage` on the device, wrapped in try/catch so the app still works if storage is unavailable (it just will not survive a refresh). Vibration uses the standard Vibration API where supported and is skipped silently elsewhere.

## Live

Part of the [AppADay](https://augustineiacopelli.github.io/appaday/) collection, a new complete app shipped every day.
