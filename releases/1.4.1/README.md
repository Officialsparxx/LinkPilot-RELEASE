# LinkPilot Release Package (v1.4.1)

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
`317d4ffe14c0e3e85692404bec3c0bfbd81aca2ef8bd9cdd6795e52384365061`

## Runtime Notes

This build is intended for normal users with no manual Python dependency setup. The packaged executable includes Playwright Chromium, Chromium Headless Shell, and the Playwright ffmpeg runtime used by Chromium automation.

## Update URL Note

This build is intended to be hosted in `LinkPilot-RELEASE` under:
`releases/1.4.1/LinkPilot.exe`

The generated manifest uses:
`https://media.githubusercontent.com/media/Officialsparxx/LinkPilot-RELEASE/main/releases/1.4.1/LinkPilot.exe`
