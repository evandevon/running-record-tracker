# Running Record Tracker: privacy and safety summary

_For principals, IT staff and teachers. Applies to version 0.0.2 and later unless this page says otherwise._

## What the tool is
A single web page that teachers open in Chrome or Edge. It saves reading recordings and their details into a folder the teacher chooses, ideally a dedicated folder inside the school's OneDrive.

## What data it handles
- Audio recordings of students reading (from v0.1), plus details such as student name, date, term and passage, saved as small text (JSON) files next to each recording.
- All of it is stored **only** in the folder the teacher chooses. The school's existing storage (for example OneDrive) holds and backs up the data, under the school's normal controls.

## What it can and can't access
| It can | It can't |
|---|---|
| Read and write inside the one folder the teacher picks, and its subfolders | See any other folder or file on the computer or in OneDrive |
| Remember which folder was picked, in this browser only | Access the teacher's Microsoft account, email or sign-in |
| | Send data over the internet |

The browser enforces these limits, not just the tool. The teacher must approve folder access, an icon in the address bar shows when it's active, and it can be revoked at any time in the browser's site settings.

The tool also warns the teacher if the folder they pick looks like their whole OneDrive, and asks them to pick a dedicated folder instead.

## No uploads: how this is enforced
The page includes a **Content Security Policy**, a standard browser security rule, with `connect-src 'none'` and `default-src 'none'`. This tells the browser to block every network request the page tries to make, including uploads, tracking and loading outside code. The tool loads no third-party code: no analytics, no fonts and no libraries.

## How to verify
1. **Test button:** the page has a "Test it: try to send data to the internet" button. The browser blocks the attempt and the page shows that it did.
2. **Offline test:** load the page, turn off Wi-Fi, and use it. Everything works.
3. **Network inspection:** press F12, open the Network tab and use the tool. No requests are made after the page loads.
4. **Source review:** the full source is public at https://github.com/evandevon/running-record-tracker. It's one readable file (`index.html`) with no build step and no minified code. Each version shown in the app matches a tagged release.

## Honest limits
- **The hosted page could change.** If the tool is used from its web address (GitHub Pages), trust depends on that code staying the same. Every change is public in the repository history. A school can keep and use its own reviewed copy of `index.html` instead.
- **The host sees visits.** GitHub, which hosts the page, can see that a device loaded it (as any website host can). It never receives recordings, names or any folder contents.
- **The rule can't stop a page leaving.** The browser rule blocks the page from *sending requests*, but it doesn't stop a page navigating to another website. The tool's only outbound link is to its own source code on GitHub, in the page footer.
- **Approval:** student voice recordings are personal information. Schools should follow their own approval, consent and retention processes before using any tool that handles student information.

## Not an official product
This tool is not made or endorsed by the NSW Department of Education.
