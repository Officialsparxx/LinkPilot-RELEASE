# LinkPilot Release Package (v1.1.0)

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
`9ff7d678f1cb4b703e8805064a1d1b705c43dd995c5fdf8fb04529227eeaee38`

## Update URL Note
This build is intended to be hosted in `LinkPilot-RELEASE` under:
`releases/1.1.0/LinkPilot.exe`

The generated manifest uses:
`https://media.githubusercontent.com/media/Officialsparxx/LinkPilot-RELEASE/main/releases/1.1.0/LinkPilot.exe`
