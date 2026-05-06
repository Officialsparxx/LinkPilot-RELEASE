# LinkPilot Release Package (v1.0.0)

This folder is the release bundle prepared from the current repository state.

## Contents
- `LinkPilot.exe` - Windows one-file desktop app build (Nuitka)
- `LinkPilot.exe.sha256` - SHA-256 checksum file
- `release_hashes.json` - JSON hash metadata for artifact verification
- `update-manifest.json` - backend update manifest payload for this binary
- `RELEASE_NOTES.md` - release summary and validation notes

## Verify Integrity (PowerShell)
From this folder:

```powershell
Get-FileHash .\LinkPilot.exe -Algorithm SHA256
```

Expected:

```text
09b15ff38e63678f708fbd95f2996fce0f8583b20421308da212e13e8ae9bef6
```

## Publish Steps
1. Create a GitHub release tag `v1.0.0` in:
   - `https://github.com/Officialsparxx/LinkPilot`
2. Upload `LinkPilot.exe` and include `RELEASE_NOTES.md` content.
3. Insert/update backend `app_versions` row using values from `update-manifest.json`.
4. Smoke test app update flow from an older installed build.

## Backend Deploy Reminder
Before production rollout, ensure Cloudflare D1 migrations through `0005_checkout_successes.sql` are applied to the remote database.
