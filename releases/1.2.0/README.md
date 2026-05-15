# LinkPilot Release Package (v1.2.0)

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
`d29ec0dc7cda419cc92537a66ca981a1a28589028f0bcdd414428c5ade3a3dee`

## Update URL Note
This build is intended to be hosted in `LinkPilot-RELEASE` under:
`releases/1.2.0/LinkPilot.exe`

The generated manifest uses:
`https://media.githubusercontent.com/media/Officialsparxx/LinkPilot-RELEASE/main/releases/1.2.0/LinkPilot.exe`
