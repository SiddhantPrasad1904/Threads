# Thread data and privacy

This describes the implemented Windows application, not a hosted service privacy policy.

**Local capture.** Only an explicitly active Remember session can observe permitted foreground application titles/processes and screenshots. Pause and Stop invalidate in-flight results. No keyboard hooks or keylogging. Thread's own windows and configured excluded processes are not captured. Browser-domain exclusions are not implemented; use Pause for private sites. There is no computer-input inactivity detector.

**Local files.** `%LOCALAPPDATA%\Thread` contains raw SQLite evidence, notes, work-state versions, handoffs, screenshot cache, settings and diagnostic metadata. Work history/screenshots are unencrypted and protected by ordinary Windows filesystem permissions. Screenshot quota and age cleanup remove optional pixels while preserving event metadata. Explicit deletion removes a session/thread's owned data. Backups and exported Markdown remain wherever you save them.

**AI processing.** When a configured provider is used at Stop/Retry, selected image evidence, titles, notes, timestamps/identifiers, current structured work state and extraction instructions/schema are sent to its API. It does not receive the entire profile/database. OpenRouter routes requests to a downstream provider. Your chosen service's data handling, retention and billing apply. No AI call is needed to view saved Resume/history or export Markdown. An optional developer watch worker also invokes the configured provider during active sessions.

**Credentials.** Saved API keys use Windows current-user DPAPI, scoped to the API endpoint/environment-variable name. They are not stored in JSON configuration, logs, SQLite or exports. An environment credential takes precedence. Code running as your Windows user can access that user's secrets; DPAPI is not a defense against a compromised account. Keys may not be portable to another user/computer. Remove saved keys in AI connection and separately remove any environment credential.

**Diagnostics.** Local rotating application logs contain operational metadata. Optional capture-decision logs use context hashes rather than raw titles/notes/pixels. AI-call audit records provider/model, timing, usage, schema and typed failure metadata, not prompts or secrets. There is no telemetry uploader, analytics service, auto-update phone-home, or account system.

**Deletion.** Quit Thread before deleting its profile. Uninstall preserves the profile to avoid accidental loss. For complete removal, delete the exact profile directory and any separate exports/backups. The app does not automatically redact secrets deliberately included in notes, screenshots or handoff edits; Pause before sensitive activity and review exports before sharing.
