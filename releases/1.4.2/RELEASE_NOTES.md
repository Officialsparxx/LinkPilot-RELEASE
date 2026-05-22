# LinkPilot v1.4.2 Release Notes

Release date: 2026-05-21

## Summary
- Patch/hardening release focused on making the public exe match the development app more closely.
- Public builds now bundle default source, proxy, and CAPTCHA plugin folders; LinkPilot logo/photo assets; `prime_profile_login.py`; and `sidecar_cli.py`.
- Fixed Nuitka onefile subprocess detection so packaged source/plugin/helper calls re-enter `LinkPilot.exe` in script mode instead of trying to start a second LinkPilot app instance.
- Added packaged-exe smoke coverage for bundled source plugin execution, proxy plugin execution, sidecar CLI execution, and sidecar communication while the app is already running.
- Carries forward the latest Target, Walmart, and Sam's Club monitor/drop hardening from the 1.4 line.

## Validation
- Auth session seeded with `py scripts\ai_runner_access.py seed-session`.
- Compile check passed: `py -m compileall -q scripts link_inspector qa_lab`.
- Release packaging unit tests passed: `py -m unittest qa_lab.tests.test_release_packaging -v`.
- Full local QA passed: `py qa_lab\run_suite.py` (361 tests).
- Live GUI smoke passed unarmed: `py qa_lab\live_gui_driver.py --monitor-polls 1 --auto-close-seconds 70`.
- Strict Nuitka onefile build passed: `py scripts\build.py --output-dir dist\release_1.4.2 --nuitka-only`.
- Packaged executable smoke passed: `py scripts\smoke_release_exe.py dist\release_1.4.2\LinkPilot.exe`.
- Packaged running-app sidecar smoke passed: `py scripts\smoke_release_exe.py dist\release_1.4.2\LinkPilot.exe --with-running-app --startup-timeout 90`.
- Build output confirmed bundled Playwright directories:
  - `chromium-1208`
  - `chromium_headless_shell-1208`
  - `ffmpeg-1011`

## Artifact Integrity
- SHA-256 (`LinkPilot.exe`):
  - `03bc80430525cb64051eefa6fa941f891c74db8535e165acbbfb1bd946507b4f`

## Notes
- This is the first published `1.4.2`; no `1.4.2` release folder existed in the release mirror before this pass.
- Live order submission remains gated behind paid pro entitlement, buy-ready item state, and the explicit live-submit arm.
- Built with Nuitka onefile on Python 3.14. Nuitka 4.0.8 reports Python 3.14 support as experimental.
- Onefile compression warning remains unless `zstandard` / `Nuitka[onefile]` is installed.
