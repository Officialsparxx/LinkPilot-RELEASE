# LinkPilot Release Package (v1.0.1)

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
`a150fd48f588c4e91aa2a2739bf57bbe2340d1298cc41129e2d9074c26155d80`

## Update URL Note
This build is intended to be hosted in `LinkPilot-RELEASE` under:
`releases/1.0.1/LinkPilot.exe`

The generated manifest uses:
`https://media.githubusercontent.com/media/Officialsparxx/LinkPilot-RELEASE/main/releases/1.0.1/LinkPilot.exe`
