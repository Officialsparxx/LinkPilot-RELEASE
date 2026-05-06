# LinkPilot v1.0.0 Release Notes

Release date: 2026-05-06

## Highlights
- Launch/auth/trial/admin backend routes and launch-session model updates are integrated in the current build.
- Full local QA regression suite is passing before packaging (`72/72`).
- Backend worker TypeScript typecheck is passing.
- Windows one-file executable is built with Nuitka.

## Build and Validation Summary
- Build command:
  - `py scripts/build.py --nuitka-only --output-dir releases/1.0.0`
- QA command:
  - `py qa_lab/run_suite.py` (`72/72` passed)
- Backend typecheck command:
  - `cd backend/worker && npm run typecheck`

## Security and Update Artifacts
- SHA-256:
  - `09b15ff38e63678f708fbd95f2996fce0f8583b20421308da212e13e8ae9bef6`
- Included artifacts:
  - `release_hashes.json`
  - `LinkPilot.exe.sha256`
  - `update-manifest.json`

## Notes
- Nuitka reported Python 3.14 as experimental in this toolchain version.
- Nuitka warned that onefile compression is not enabled unless `zstandard` is installed.
