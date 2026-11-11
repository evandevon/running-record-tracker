# Running Record Tracker

A browser tool for teachers to record students reading aloud several times a year and keep the recordings organised, so you can hear whether their reading has improved.

**Status:** v0.1.1, the batch recorder. You can set up a class list and passages, then record students one after another; each recording is saved and named automatically. Reviewing and marking recordings comes next.

## Quick start
1. Open the page in **Chrome or Edge** on a laptop.
2. Click **Choose folder…** and pick (or make) a dedicated folder inside your OneDrive, e.g. `Reading Samples`.
3. In **Setup**, paste your class list and add a passage (optional).
4. Press **Record** (or the Space bar) for the first student, then press it again to stop. The recording is saved and the next student comes up.

Recordings are saved as `Students/Billy Bob/Billy Bob - 2026 Term4 Week02 P1.webm`, with a details file for each in `Students/Billy Bob/Recording details/`. WebM plays in Chrome, Edge and VLC. MP3 export is planned.

## How it works
- It runs entirely in your browser (Chrome or Edge on a laptop or desktop).
- You choose **one dedicated folder**, ideally inside your OneDrive, for example `Reading Samples`. The tool can only read and write inside that folder.
- Files are saved straight into that folder, and your OneDrive app backs them up as usual.
- There's no server, no account and no sign-in.

## Privacy and safety
See [PRIVACY.md](PRIVACY.md) for the one-page summary for principals and IT, including how to check every claim yourself.

In short:
- The page has a Content Security Policy that **blocks all network requests**, so it can't upload recordings or student details anywhere. A "Test it" button on the page shows this.
- It uses no third-party code, analytics or tracking. It's a single, readable `index.html`.
- Access is limited to the chosen folder, and you can revoke it from the browser's address bar or site settings.

## Using it
- **Online:** open the GitHub Pages link (once enabled).
- **Offline or locally:** download `index.html` and double-click it. It works the same way.

## Versions
See [CHANGELOG.md](CHANGELOG.md). The version shown in the app matches the GitHub release tag.

_Not an official NSW Department of Education product._
