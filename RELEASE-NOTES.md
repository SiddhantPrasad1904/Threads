# Thread 0.2.0 RC2 dev4 — unpublished preview

Current artifact: portable Windows x64 ZIP. This is a development candidate. The existing GitHub release remains draft and unpublished. Older setup and ZIP assets remain in the draft for history and do not contain dev4.

## Candidate changes

- Added an explicit Settings notice that browser-domain exclusion is not available. Users must Pause before private browser sites.
- Retained WGC foreground capture, initial-context capture at Start/Resume, visual filtering, event persistence, process exclusions, input-inactivity suppression, and bounded screenshot cache.
- Retained optional provider configuration, provenance-grounded WorkState, saved handoffs, Resume, and corrected Markdown export.
- Retained organization task/status sharing with explicit review and publication, role-based workspaces, inbox updates, invitation/identity controls, and restricted SCIM support. A production organization host is not provided.

## Verification

- Desktop suite: 302 passed, 3 skipped.
- Organization service suite: 74 passed; two dependency deprecation warnings.
- Organization browser tests: 8 passed.
- Packaged dev4 offline smoke: 7 checks passed.
- Credential-pattern release scan: 153 files scanned, no findings. Pattern scans do not prove absence of every secret.
- Portable ZIP SHA-256: `9e1cc02e9f5558903083d0994cda23ce120a63678c972b7a71d1e9108827a7f1`.

No live provider, fresh real-window capture, clean-machine installation, production deployment, or end-to-end human acceptance is claimed by these automated checks.

## Open gates

M5 Resume, M6 export, screenshot-cache and full end-to-end acceptance remain awaiting human review. Current-source installer compilation is blocked by the host's NSIS startup error. Build is unsigned. Raw local history/screenshots are not encrypted by Thread. Browser-domain exclusions and automatic update are absent. Real Docker/PostgreSQL/SSO/TLS hosting, backup/restore, multi-machine organization acceptance, complete accessibility review, third-party license clearance, and independent security assessment remain open. Do not treat this preview as an enterprise-ready release.
