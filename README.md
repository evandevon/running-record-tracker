# Running Record Tracker

A browser tool for teachers to record students reading aloud several times a year and keep the recordings organised, so you can hear whether their reading has improved.

**Status:** v0.0.2, the foundation. It connects safely to a folder (for example inside OneDrive) and includes diagnostics. Recording comes in v0.1.

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
