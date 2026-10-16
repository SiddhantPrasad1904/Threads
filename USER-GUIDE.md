# Thread 0.2.0 RC2 dev4 preview

This preview is a portable Windows x64 ZIP. Extract the complete folder and run `Thread.exe`; keep `_internal` and `ThreadWorker.exe` beside it. No Python install is needed. The build is unsigned. Verify the SHA-256 listed in the GitHub draft before running it.

## First use

1. Launch Thread. Create or open a thread.
2. Choose **Start Remembering** to begin foreground observation. Thread captures the current permitted foreground context and later meaningful changes.
3. Choose **Pause** before private activity. Resume explicitly to continue. Choose **Stop** to end capture and produce a handoff.
4. Review the handoff. Edit and save corrections. Resume later uses saved handoff and WorkState; viewing context does not start capture.
5. Choose **Resume remembering** only when you want a new session on the same thread.
6. Use View history and Export Markdown to inspect and save local context. Export omits screenshot pixels and internal prompts, and redacts configured/common credential formats. Review every export; arbitrary secrets may not be detected.

## AI provider

AI is optional. Local capture and notes work without a provider. Configure your own compatible multimodal provider in AI connection. A provider must accept images and strict JSON-schema output. Provider charges, routing, and data policies apply. Thread sends selected evidence only when you configure and invoke extraction. The opt-in **Update WorkState while Remembering** setting sends bounded checkpoints during active sessions; it is off by default. A synthetic connection test sends a synthetic image and may incur provider charges.

Saved keys use Windows current-user DPAPI. Environment credentials take precedence. Never paste a key into chat or public issues.

## Capture and storage

Thread observes only during an active Remember session. It does not record keystrokes. Pause and Stop invalidate in-flight capture. Browser-domain exclusions are not implemented, so Pause before private browser sites. Process exclusions are available. Input-inactivity suppression defaults to 300 seconds and can be changed in Settings; this uses Windows' last-input timestamp and does not record keys or clicks.

Data defaults to `%LOCALAPPDATA%\Thread`; Settings shows the active path. Raw history and screenshots are not encrypted by Thread. Screenshot cache defaults to 256 MiB and can be adjusted in Settings. Old unprotected screenshot files are evicted first. Metadata remains after pixel eviction. Current WorkState provenance protects referenced pixels. If protected frames fill the quota, Thread reports the storage failure instead of deleting protected evidence.

## Organization sharing

Organization sharing is optional and requires a separately deployed server. Marking a thread Work does not publish it. Share only reviewed task/status content or an optional handoff. Personal screenshots, notes, and WorkState are never synchronized to the organization server. Real production hosting and identity-provider configuration are not included in this preview.

## Quit, update, and remove

Closing a window leaves Thread in the tray. Choose **Quit Thread** from the floating or tray menu to exit. Back up the profile before testing updates. Do not downgrade a profile opened by a newer build without restoring a backup. Uninstall preserves user data. For complete removal, quit Thread and delete the exact profile folder shown in Settings; separately remove exports and backups.

## Known limitations

The dev4 ZIP is a development preview, not a signed installer. Protected, elevated, DRM, minimized, or nearly uniform windows may not yield usable screenshots. Browser-domain exclusions and automatic updates are absent. Raw local history is unencrypted. M5, M6, screenshot-cache, and end-to-end human acceptance remain pending. Real multi-machine organization, SSO, PostgreSQL, HTTPS, backups, clean-machine install, accessibility, and independent security review remain unverified.
