# LinkPilot v1.3.0 Release Notes

Release date: 2026-05-18

## Summary
- Feature release focused on launch access and public release packaging.
- Added backend-backed device trial mode through `Try Without Login`.
- Trial sessions can use watch/notification flows when the backend grants `watch`.
- Live checkout submit remains gated behind paid `pro` entitlement and the normal live-submit arm.
- Release packaging continues to bundle Playwright Chromium, Chromium Headless Shell, and ffmpeg.

## Validation
- Auth session seeded with `py scripts\ai_runner_access.py seed-session`.
- Compile check passed: `py -m compileall -q scripts link_inspector qa_lab`.
- Full local QA passed: `py qa_lab\run_suite.py` (246 tests).
- Live GUI smoke passed: `py qa_lab\live_gui_driver.py --monitor-polls 1 --auto-close-seconds 70`.
- Strict Nuitka onefile build passed: `py scripts\build.py --output-dir dist\release_1.3.0 --nuitka-only`.
- Build output confirmed bundled Playwright directories:
  - `chromium-1208`
  - `chromium_headless_shell-1208`
  - `ffmpeg-1011`

## Artifact Integrity
- SHA-256 (`LinkPilot.exe`):
  - `9a1355757a2c909f903bb5b96c50efe281782ceed1217bec9263786abb5484a2`

## Notes
- Built with Nuitka onefile on Python 3.14. Nuitka 4.0.8 reports Python 3.14 support as experimental.
- Onefile compression warning remains unless `zstandard` / `Nuitka[onefile]` is installed.
- Live GUI smoke still shows known Mavely redirect warnings during cleanup; they did not block launch, scrape, or monitor attempt startup.
