# Thread for Windows

Thread helps you return to unfinished work. Start Remembering, work normally, then Stop to create a grounded handoff. Review or correct it, and return later through Resume.

## Current preview

The unpublished development preview is **0.2.0 RC2 dev4**, Windows x64. It is a portable ZIP; extract the complete folder and run `Thread.exe`. No separate Python installation is needed. The preview is unsigned. Check the SHA-256 file before use.

This is a development preview, not a completed public release or enterprise service. The existing GitHub release remains a draft. Older setup and ZIP assets in that draft are historical and do not contain dev4. Read RELEASE-NOTES.md and USER-GUIDE.md before use.

## What it does

- Foreground observation only during an active Remember session. Pause and Stop end observation; Thread does not record keystrokes.
- Windows Graphics Capture with local visual filtering, process exclusions, input-inactivity suppression, and a configurable bounded screenshot cache. Browser-site exclusions are not available; Pause before private sites.
- Optional bring-your-own-key multimodal provider for grounded WorkState, editable handoffs, and Resume. Evidence stays local unless you configure and invoke a provider or deliberately publish reviewed organization content.
- Local history, provenance, crash-safe event persistence, and Markdown export with saved corrections and credential-pattern redaction.
- Optional separately deployed organization workspace for explicitly reviewed shared tasks and optional handoffs. Private screenshots, notes, and WorkState are not synchronized.

## Not release-ready yet

M5 Resume, M6 export, screenshot-cache, and end-to-end human acceptance remain pending. No verified current-source installer or code signing is available. Raw local history and screenshots are not encrypted by Thread. Browser-domain exclusions and automatic updates are absent. Real SSO, Docker, PostgreSQL, HTTPS deployment, backup-restore, multi-machine acceptance, accessibility review, and independent security assessment remain open.

## Downloads and docs

The draft prerelease is at [GitHub Releases](https://github.com/SiddhantPrasad1904/Threads/releases). Do not install the older setup binary as if it contained dev4. Current preview files and checksums are listed in the draft body.

- [User guide](USER-GUIDE.md)
- [Privacy](PRIVACY.md)
- [Release notes](RELEASE-NOTES.md)
- [Security reporting](SECURITY.md)
- [Third-party notices](THIRD-PARTY-NOTICES.md)
- [Application preview terms](APPLICATION-LICENSE.md)

Support: [GitHub Issues](https://github.com/SiddhantPrasad1904/Threads/issues). Never post API keys, passwords, local databases, screenshots, or private work evidence in public issues.

This public repository contains downloads and documentation only. MIT terms apply to repository documentation, not Thread application binaries or private implementation. See APPLICATION-LICENSE.md.
