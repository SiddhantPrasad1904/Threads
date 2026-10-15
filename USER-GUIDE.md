# Thread

Remember your work. Return with context.

## Install and launch
Run the Windows x64 Setup executable. Installation is per user; administrator rights are not required. Launch **Thread** from Start. For the portable ZIP, extract the complete Thread folder and run `Thread.exe`; keep `_internal` and `ThreadWorker.exe` alongside it. No Python installation is needed. This release candidate targets Windows 10 2004+ / Windows 11 x64.

Unsigned builds may trigger Windows publisher/reputation warnings. Verify the download source and published SHA-256; do not disable Windows security protections. Use the signed build when the publisher provides one.

## First use
The welcome screen offers **Set up AI connection**, **Open threads / start with local capture**, and capture settings. Help remains available from the tray and floating menus.

1. Open **AI connection**. Choose OpenRouter or enter a compatible HTTPS endpoint, model and key. The model must support images and strict JSON-schema responses. Provider availability and cost are determined by your provider; a free router does not guarantee availability.
2. Allow evidence processing and **Save connection**. Keys are encrypted for your Windows account, scoped to the endpoint. Existing key environment variables take precedence. No key is written to settings or SQLite.
3. **Test saved connection** sends a synthetic image and greeting only. It makes a real provider call and may use your credits. A successful test proves one multimodal structured request worked; it does not guarantee future capacity or extraction quality. Close the dialog to cancel.
4. Open **Recent threads → New**, name your work, then **Start remembering**. Work normally. **Pause** before private activity. Add a natural note when useful.
5. **Stop remembering** immediately ends capture and prepares an AI handoff. Review, Edit and Save it. Processing failures preserve your evidence; fix the connection and Retry.
6. Later, open **Resume thread**. Viewing saved context never starts capture. **Resume remembering** explicitly starts a new session on the same thread.
7. **View history** reopens saved handoffs. **Export Markdown** creates a readable local document with saved corrections, without screenshot binaries or internal prompts.

## Privacy and storage
Read `PRIVACY.md`. Data defaults to `%LOCALAPPDATA%\Thread`; Settings displays the actual location. Screenshot disk cache defaults to **256 MiB**, configurable from 16–4096 MiB. Old unprotected pixels are evicted first; lightweight evidence remains. Current WorkState references are protected. If protected frames fill the budget, capture stops visibly; increase the quota or archive old threads, then Retry observation. Existing protected data can exceed a newly lowered limit; it cannot grow through new accepted captures.

## Quit, update and remove
Closing a window leaves Thread running. Choose **Quit Thread** from the floating or tray menu. Save prompted handoff edits. Both floating control and tray icon disappear.

For an update, Stop, save, Quit and back up your profile while Thread is closed. Run the new installer into the same application directory. Data migrations apply on launch. Do not downgrade a database opened by a newer build without restoring your backup.

Uninstall through Windows Installed apps. Work history and encrypted credentials are preserved. To remove everything, Quit/uninstall, then delete the exact profile directory shown in Settings (normally `%LOCALAPPDATA%\Thread`). Exported Markdown and explicit diagnostic exports are outside the profile and must be removed separately. To remove only an API key, use **AI connection → Remove saved key**; separately clear any key environment variable you configured.

## Troubleshooting
- **No AI configured / missing credentials:** local capture works; open AI connection, save and test, then Retry handoff. Developer `THREAD_AI_*` environment overrides must be removed before editing configuration in the GUI.
- **Timeout / provider limit / invalid structured response:** retry later or choose another model with image + strict schema support. Thread never relaxes validation or replaces source evidence with an invalid result.
- **Capture stopped:** hover the widget or open Raw events to read the error. Resolve storage/exclusions, then Retry observation.
- **No screenshot:** protected/elevated/DRM/minimized windows and nearly blank frames may be unavailable. No full-desktop fallback is used.
- **Already running:** use the tray icon; only one desktop instance per profile is allowed.
- **Interrupted session after a crash:** recover paused or end the session; recovery never silently starts capture.

The app does not detect input inactivity inside an active Remember session. Pause when away. Visual filtering and disk quota still apply. Export and saved Resume are offline; AI extraction normally happens at Stop in this release. No automatic updates or private-evidence cloud synchronization are included. Optional organization sharing requires a separately deployed server.


## Organization sharing (optional)
Set the HTTPS organization origin in Settings. Mark a thread Work, choose Share work task, enter only content you intend to publish, and approve Copy reviewed draft. Open the organization board in your browser, sign in, import the draft, select workspace/project and review every field before Publish. Copy the shared task link back to the desktop to link it locally. Labeling a thread Work never publishes its private evidence.

Shared task statuses refresh in the browser. Important updates lists blocked/completed changes from other members; read state is durable and new updates can be muted per workspace. Account/workspace deletion and ownership changes require explicit confirmation. There is no automatic private-task completion upload, background email delivery or OS push.
