# Changelog

## 0.3.0 (2026-11-12): MP3 and full recording history
- **MP3 by default.** Recordings are converted to MP3 (mono, 64 kbps, about 0.5 MB a minute) in the browser by the built-in LAME encoder, so nothing is uploaded. WebM is still available in Setup → Audio format.
- **Details inside the MP3.** Each MP3 carries the student, title, date, term/week and passage ID, and the passage text is stored as the file's "lyrics". If the conversion ever fails, the recording is saved as WebM instead and the teacher is told.
- **Convert WebM to MP3.** A one-click button in the Library converts older WebM recordings. Each MP3 is saved and checked before the WebM is removed, and the details file is updated.
- **New Library layout ("Recording history").** Pick a student on the left to see every recording they've ever had as a timeline grouped by year. Press ▶ to play any one, or tick several and press **Play selected** to hear them back to back, oldest first. A note says whether the ticked recordings use the same passage. Passages are colour-coded.
- Previous/next student buttons, search, and "This class only".
- Delete any recording from its history (it goes to the OneDrive recycle bin).
- **Term overview** (formerly Term grid): click a name to open that student's history, or ▶ to jump there and play.
- Space plays/pauses in the Library, and starts/stops recording elsewhere, so a stray Space press while listening doesn't start a recording.
- The README written into the folder now describes MP3s.

## 0.2.0 (2026-11-12): library
- New **Library** section that reads every recording in the folder.
- **By student:** each child's recordings in date order, with date, term/week, passage, length and file name, and a ▶ button for each.
- **Then vs now:** pick any two of a child's recordings (first and latest by default) and play them back to back. Shows how far apart they are, and warns when the passages differ.
- **Term grid:** students down the side, Terms 1–4 across, for any year. Click a cell to hear that term's latest recording. Shows how many are recorded per term and who is still to record this term.
- A player that stays visible while scrolling; search; "This class only" toggle (untick to see every student folder, including past students).
- Audio files without a details file (e.g. copied in from elsewhere) still appear, flagged.
- "✓ this term" badges on the Record screen now come from the same scan.

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
