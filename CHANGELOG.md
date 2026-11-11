# Changelog

## 0.1.1 (2026-11-11): simpler names and tidier folders
- New default naming: `Students/Billy Bob/Billy Bob - 2026 Term4 Week02 P1.webm`. Week numbers are padded so they sort correctly everywhere.
- A second recording in the same week gets ` (2)`, ` (3)`.
- Folders are named first name first, and real names are kept (apostrophes, accents). Only characters Windows/OneDrive forbid are removed.
- Details files now go in a `Recording details` folder inside each child's folder, so the child's folder shows just the audio.
- Each student gets a hidden ID, saved in `config.json` and each details file, to help with name changes later.
- Warns about two students with the same name, and won't record until one has an initial added.
- README.txt in the folder is updated with the new layout and advice on shared or personal storage. Older app-written READMEs are replaced automatically.
- Settings from 0.1.0 are upgraded automatically (Date-first naming switches to the new default, and per-student passages carry over).

## 0.1.0 (2026-11-11): batch recorder
- Class list (one per line, "First Surname" or "Surname, First"), class name, term and term start date (week numbers worked out automatically).
- Batch recording queue: one big Record/Stop button, auto-advance to the next student, Back / Skip / Absent, and keyboard shortcuts (Space, ←, →, A).
- Passage library (ID, level, text, word count). Choose "everyone reads the same passage" or "each student can have their own"; each student's passage is remembered.
- Five file-naming styles plus a custom pattern, with a live example.
- Saves WebM audio plus a details file (.json) to `Students/<Surname First>/`. Repeats get `_2`, `_3`.
- "✓ this term" badges built from the files already in the folder.
- Play back or delete the last recording straight away.
- Microphone choice (remembered on this computer) and a live level meter.
- Setup saved to `config.json` in the folder, so other computers share it. A `README.txt` organisation guide is written to the folder.
- Safety panel folds away once connected; the folder name is shown in the header.

## 0.0.2 (2026-11-11): safety foundation
- "What this tool does and doesn't do" panel, with a how-to-verify guide.
- Content Security Policy blocking all network requests, plus a "Test it" button that demonstrates the block.
- A warning when the chosen folder looks like a whole OneDrive.
- Folder remembered between visits, with a Disconnect option.
- Diagnostics: browser checks, write/read tests, folder watcher, log.
- Version number shown in the app.

## 0.0.1 (2026-11-11): OneDrive folder sync test
- A standalone test page confirming a browser can save straight into a OneDrive-synced folder.
