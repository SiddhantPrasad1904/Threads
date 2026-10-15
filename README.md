# Thread for Windows

Thread helps you return to unfinished work. Start Remembering, work normally, then Stop to create a grounded handoff. Review or correct it, and return later through Resume. Export saved context as Markdown.

**0.2.0 RC1 is an unsigned preview, not a completed enterprise release.** Windows x64, Windows 10 build 19041 or newer. AI is optional and uses your own compatible provider key; image input and strict structured JSON support are required. Provider charges/data policies apply.

## Downloads

Use [GitHub Releases](https://github.com/SiddhantPrasad1904/Threads/releases) when the reviewed candidate is published. A draft is visible only to repository maintainers. Choose `Thread-0.2.0-rc1-Setup-x64.exe` or extract the entire portable ZIP and run `Thread.exe`. No separate Python installation is needed. Check the SHA-256 values in `SHA256SUMS.txt`. An unsigned preview does not have verified publisher signing identity.

Matching third-party library source archives are provided as `Thread-0.2.0-rc1-ThirdParty-Sources.zip`. This is dependency source, not proprietary Thread source. See THIRD-PARTY-SOURCE-ACCESS.md.

## Features and boundaries

Scoped foreground capture, Pause/Resume/Stop, WGC screenshots with filtering, 256 MiB default bounded screenshot cache, notes, BYOK AI setup, grounded state, editable handoffs, Resume and Markdown export. Closing a window leaves the tray running; use **Quit Thread** to exit completely.

The latest interface and optional organization draft/link controls are included. Organization sharing requires a separately deployed private server and configured identity provider; no hosted team service is provided by this download. No automatic private-evidence synchronization or automatic shared task completion inference.

No claim is made that the full readiness checklist is complete. Real organizational hosting/SSO/PostgreSQL, clean-machine coverage, user acceptance, full accessibility, load/security review and operational restore testing remain pending. No email/desktop push, SCIM, browser-domain exclusions, inactivity auto-pause or automatic updater. Read RELEASE-NOTES.md before use.

## Privacy and support

Capture occurs only in active Remember sessions; Pause before private activity. Selected evidence is sent to your configured AI provider with consent. Local work evidence is not encrypted by Thread. Saved API keys use Windows DPAPI or environment variables. Never post keys, passwords, profiles or private screenshots in public issues. Read PRIVACY.md.

General support: [GitHub Issues](https://github.com/SiddhantPrasad1904/Threads/issues). Security reports: follow [SECURITY.md](SECURITY.md) and use private reporting. No guaranteed response time.

This repository hosts downloads and documentation only. MIT applies to repository documentation, not application binaries or proprietary implementation. Application use follows [APPLICATION-LICENSE.md](APPLICATION-LICENSE.md). Third-party licenses retain their own rights.
