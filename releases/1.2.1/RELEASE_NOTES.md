# LinkPilot v1.2.1 Release Notes

Release date: 2026-05-17

## Summary
- Patch release focused on public build readiness and packaged browser automation.
- Release builds now bootstrap and bundle both Playwright Chromium runtimes required by LinkPilot:
  - `chromium`
  - `chromium-headless-shell`
- Nuitka packaging now resolves installed Playwright browser IDs before passing them to the Playwright plugin.
- Packaged runtime startup has a guarded one-time fallback install path if browser binaries are missing.
- User-facing Playwright setup guidance now names both required Chromium components.

## Validation
- Auth session seeded with `py scripts\ai_runner_access.py seed-session`.
- Compile check passed: `py -m compileall -q scripts link_inspector qa_lab`.
- Full local QA passed: `py qa_lab\run_suite.py` (244 tests).
- Strict Nuitka onefile build passed: `py scripts\build.py --output-dir dist\release_1.2.1 --nuitka-only`.
- Build output confirmed bundled Playwright directories:
  - `chromium-1208`
  - `chromium_headless_shell-1208`
  - `ffmpeg-1011`

## Artifact Integrity
- SHA-256 (`LinkPilot.exe`):
  - `076747840a9f020ab8c3c7bfe5825ebd811e2a6b89fe3facacb70709a681846c`

## Notes
- Built with Nuitka onefile on Python 3.14. Nuitka 4.0.8 reports Python 3.14 support as experimental.
- Onefile compression warning remains unless `zstandard` / `Nuitka[onefile]` is installed.
