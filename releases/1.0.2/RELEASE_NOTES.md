# LinkPilot v1.0.2 Release Notes

Release date: 2026-05-07

## Summary
- Patch release after 1.0.1 with deployment and relay hardening updates.
- TCG monitor relay path stabilized for production backend routing.
- Launch backend defaults updated to use `https://api.linkpilot.pro`.

## Validation
- Backend worker typecheck passed.
- Source polling regression tests passed.
- Windows onefile build completed with Nuitka.

## Artifact Integrity
- SHA-256 (`LinkPilot.exe`):
  - `28f36b4eca874b6d5030c942abb5d2a62c9311cd2dc44e275fbc5b7d8c4e155d`

## Notes
- Built with Nuitka onefile on Python 3.14 (Nuitka currently marks 3.14 as experimental).
- Onefile compression warning remains unless `zstandard` is installed.
