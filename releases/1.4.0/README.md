# LinkPilot Release Package (v1.4.0)

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
`be7de557f47262e4f09fce07cb9a66a5b6b7005372c36d39665d7612843735db`

## Runtime Notes

This build is intended for normal users with no manual Python dependency setup. The packaged executable includes Playwright Chromium, Chromium Headless Shell, and the Playwright ffmpeg runtime used by Chromium automation.

## Update URL Note

This build is intended to be hosted in `LinkPilot-RELEASE` under:
`releases/1.4.0/LinkPilot.exe`

The generated manifest uses:
`https://media.githubusercontent.com/media/Officialsparxx/LinkPilot-RELEASE/main/releases/1.4.0/LinkPilot.exe`
