# LinkPilot v1.0.2 Release Notes

Release date: 2026-05-07

## Summary
- Patch release after 1.0.1 with deployment and relay hardening updates.
- TCG monitor relay path stabilized for production backend routing.
- Launch backend defaults updated to use `https://api.linkpilot.pro`.
- Reduced notification noise by keeping `DEBUG` lines out of user-facing Live Activity by default.

## Validation
- Backend worker typecheck passed.
- Source polling regression tests passed.
- Windows onefile build completed with Nuitka.

## Artifact Integrity
- SHA-256 (`LinkPilot.exe`):
  - `d2041d92b33d5403a7dbe90f6529c61ff0f3f3d661deb778270af0e9523df738`

## Notes
- Built with Nuitka onefile on Python 3.14 (Nuitka currently marks 3.14 as experimental).
- Onefile compression warning remains unless `zstandard` is installed.
