# LinkPilot v1.0.1 Release Notes

Release date: 2026-05-07

## Summary
- Patch release after 1.0.0 with small improvements and hardening updates.
- Launch/update release wiring retained and verified.

## Validation
- Backend worker typecheck passed.
- Local QA suite passed (`80/80`).
- Windows onefile build completed with Nuitka.

## Artifact Integrity
- SHA-256 (`LinkPilot.exe`):
  - `a150fd48f588c4e91aa2a2739bf57bbe2340d1298cc41129e2d9074c26155d80`

## Notes
- Build used Nuitka on Python 3.14; Nuitka currently flags 3.14 as experimental.
- Onefile compression warning remains unless `zstandard` is installed.
