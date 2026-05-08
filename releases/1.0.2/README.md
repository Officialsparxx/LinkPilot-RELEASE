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
`d2041d92b33d5403a7dbe90f6529c61ff0f3f3d661deb778270af0e9523df738`

## Update URL Note
This build is intended to be hosted in `LinkPilot-RELEASE` under:
`releases/1.0.2/LinkPilot.exe`

The generated manifest uses:
`https://media.githubusercontent.com/media/Officialsparxx/LinkPilot-RELEASE/main/releases/1.0.2/LinkPilot.exe`
