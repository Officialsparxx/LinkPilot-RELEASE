# LinkPilot v1.1.0 Release Notes

Release date: 2026-05-14

## Summary
- Feature release with hardened launch/auth runtime and expanded readiness safeguards.
- Added navigation orchestration paths and source decision improvements for Target/Walmart/TCG workflows.
- Improved Discord account/API integration and monitor profile alignment for live runs.
- Backend/admin surface expanded and documented for account controls and safer operations.

## Validation
- Local regression suite passed: `py qa_lab\run_suite.py` (154 tests).
- Windows onefile build completed with Nuitka.

## Artifact Integrity
- SHA-256 (`LinkPilot.exe`):
  - `$sha`

## Notes
- Built with Nuitka onefile on Python 3.14 (Nuitka currently marks 3.14 support as experimental).
- Onefile compression warning remains unless `zstandard` is installed.
