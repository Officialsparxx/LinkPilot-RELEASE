# LinkPilot Release Package (v1.3.0)

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
`9a1355757a2c909f903bb5b96c50efe281782ceed1217bec9263786abb5484a2`

## Runtime Notes

This build is intended for normal users with no manual Python dependency setup. The packaged executable includes Playwright Chromium, Chromium Headless Shell, and the Playwright ffmpeg runtime used by Chromium automation.

## Update URL Note

This build is intended to be hosted in `LinkPilot-RELEASE` under:
`releases/1.3.0/LinkPilot.exe`

The generated manifest uses:
`https://media.githubusercontent.com/media/Officialsparxx/LinkPilot-RELEASE/main/releases/1.3.0/LinkPilot.exe`
