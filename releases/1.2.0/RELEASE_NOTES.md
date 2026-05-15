# LinkPilot v1.2.0 Release Notes

Release date: 2026-05-15

## Summary
- Feature release focused on launch-readiness, source reliability, and account-session stability.
- Added/expanded RestockR support (source + account workflow) with safer auto-open handling.
- Added Discord account polling toggle control for account-mode listener behavior.
- Hardened account autofill so saved credentials can submit sign-in and report post-submit login state.
- Added browser window recovery so headed login/preview windows are brought back on-screen when misplaced.

## Validation
- Full local regression suite passed: `py qa_lab\run_suite.py` (169 tests).
- Release build completed with Nuitka onefile.

## Artifact Integrity
- SHA-256 (`LinkPilot.exe`):
  - `d29ec0dc7cda419cc92537a66ca981a1a28589028f0bcdd414428c5ade3a3dee`

## Notes
- Built with Nuitka onefile on Python 3.14 (Nuitka currently marks 3.14 support as experimental).
- Onefile compression warning remains unless `zstandard` is installed.
