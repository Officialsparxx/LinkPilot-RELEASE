# LinkPilot Release Package (v1.0.2)

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
`28f36b4eca874b6d5030c942abb5d2a62c9311cd2dc44e275fbc5b7d8c4e155d`

## Update URL Note
This build is intended to be hosted in `LinkPilot-RELEASE` under:
`releases/1.0.2/LinkPilot.exe`

The generated manifest uses:
`https://media.githubusercontent.com/media/Officialsparxx/LinkPilot-RELEASE/main/releases/1.0.2/LinkPilot.exe`
