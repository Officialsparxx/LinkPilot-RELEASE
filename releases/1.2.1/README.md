# LinkPilot Release Package (v1.2.1)

Contents:
- `LinkPilot.exe`
- `LinkPilot.exe.sha256`
- `release_hashes.json`
- `update-manifest.json`
- `RELEASE_NOTES.md`

## Verify

```powershell
Get-FileHash .\LinkPilot.exe -Algorithm SHA256
```

Expected:
`076747840a9f020ab8c3c7bfe5825ebd811e2a6b89fe3facacb70709a681846c`

## Runtime Notes

This build is intended for normal users with no manual Python dependency setup. The packaged executable includes Playwright Chromium, Chromium Headless Shell, and the Playwright ffmpeg runtime used by Chromium automation.

## Update URL Note

This build is intended to be hosted in `LinkPilot-RELEASE` under:
`releases/1.2.1/LinkPilot.exe`

The generated manifest uses:
`https://media.githubusercontent.com/media/Officialsparxx/LinkPilot-RELEASE/main/releases/1.2.1/LinkPilot.exe`
