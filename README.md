# Thread for Windows

Thread helps you return to unfinished work. Start a Remember session, work normally, then Stop to create a grounded handoff. Review or correct it, and return later through Resume. Export your saved work context as Markdown.

**0.1.0 RC2 is a release candidate, not a final accepted release.** Windows x64, Windows 10 build 19041 or newer. AI is optional and requires your own compatible provider key and a model supporting images and strict JSON schemas. Provider charges and data policies apply.

## Download and install

Download the installer or portable ZIP from [Releases](https://github.com/SiddhantPrasad1904/Threads/releases) when assets are available. Extract the entire ZIP before launching `Thread.exe`. No Python installation is needed. The candidate is unsigned; verify its SHA-256 against `SHA256SUMS.txt`. Do not run downloads from untrusted mirrors.

Open **AI connection**, enable AI, select a provider/model, enter your key locally and approve evidence processing. Save, then **Test saved connection**. The test uses a synthetic image. Keys are stored with Windows current-user DPAPI; they are never requested through GitHub or chat.

Read [User guide](USER-GUIDE.md), [Privacy](PRIVACY.md), and [Release notes](RELEASE-NOTES.md). Local data defaults to `%LOCALAPPDATA%\Thread`. Closing a window does not quit the application: use **Quit Thread** from its tray/floating menu.

## Privacy

Observation runs only within active Remember sessions. Pause and Stop close the capture gate. There is no keylogging. Selected screenshot and text evidence is sent to your chosen AI endpoint for extraction; local history and exports remain on your computer. Screenshot cache defaults to 256 MiB, with provenance protection. Read the privacy document for limits and retention details.

## Feedback and licensing

Report ordinary reproducible bugs through [Issues](https://github.com/SiddhantPrasad1904/Threads/issues), after removing private work content. Never attach keys, full profiles or private screenshots. Security reporting instructions must be configured before public launch; do not disclose credentials or exploitable details in public issues.

This repository contains downloads and documentation only. The repository MIT license applies to its documentation, not to the separately distributed Thread application binary or proprietary implementation. Application distribution terms require publisher review before public release. Third-party components retain their own license terms and notices.
