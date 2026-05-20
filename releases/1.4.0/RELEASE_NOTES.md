# LinkPilot v1.4.0 Release Notes

Release date: 2026-05-20

## Summary
- Feature release focused on safer public startup behavior, source-intake control, and live-retail reliability.
- Saved watches, source polling, Discord startup, and live drop automation now default to off until the user enables them.
- New review-first source intake can hold unknown Discord/source product signals for manual review, while fast-drop and live-armed workflows can still override that intentionally.
- Dashboard/header status now reports operational state: safety arm, intake mode, active scope, runtime activity, and latest meaningful event.
- Walmart affiliate/tracking URLs are canonicalized before monitor strategy dispatch, reducing unnecessary challenge-page escalation.
- Checkout/payment form handling includes stronger saved-card and AmEx CID handling.
- Public release packaging continues to bundle Playwright Chromium, Chromium Headless Shell, and ffmpeg.

## Validation
- Auth session seeded with `py scripts\ai_runner_access.py seed-session`.
- Compile check passed: `py -m compileall -q scripts link_inspector qa_lab`.
- Full local QA passed: `py qa_lab\run_suite.py` (286 tests).
- Live GUI smoke passed unarmed: `py qa_lab\live_gui_driver.py --monitor-polls 1 --auto-close-seconds 70`.
- Strict Nuitka onefile build passed: `py scripts\build.py --output-dir dist\release_1.4.0 --nuitka-only`.
- Packaged executable launch smoke passed: `releases\1.4.0\LinkPilot.exe` stayed alive for 45 seconds.
- Build output confirmed bundled Playwright directories:
  - `chromium-1208`
  - `chromium_headless_shell-1208`
  - `ffmpeg-1011`

## Artifact Integrity
- SHA-256 (`LinkPilot.exe`):
  - `be7de557f47262e4f09fce07cb9a66a5b6b7005372c36d39665d7612843735db`

## Notes
- This is a minor release rather than a major release because workflows are preserved and live submit remains behind the existing paid pro entitlement plus live-submit arm.
- Users who want startup automation should explicitly re-enable saved watch/source/Discord startup settings after reviewing the safer defaults.
- Built with Nuitka onefile on Python 3.14. Nuitka 4.0.8 reports Python 3.14 support as experimental.
- Onefile compression warning remains unless `zstandard` / `Nuitka[onefile]` is installed.
- Live GUI smoke still shows known Mavely redirect warnings during cleanup; they did not block launch, scrape, Playwright rendering, or monitor startup.
