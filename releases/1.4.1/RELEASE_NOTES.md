# LinkPilot v1.4.1 Release Notes

Release date: 2026-05-20

## Summary
- Patch/hardening release focused on the first successful real Target live-checkout path.
- Strengthens Target checkout from cart and product-page states, including cart-state resume and account-login priming before the first monitor check.
- Adds quantity-aware add-to-cart/checkout routing so the app avoids unsafe Buy Now-only paths and prefers the requested product row in cart.
- Improves payment/CVV handling for saved cards, side-panel security-code prompts, and Target checkout auth-choice pages.
- Adds explicit source import controls so source alerts can be observed without automatically importing unknown links unless fast-drop/live-armed workflows intentionally override it.
- Keeps public release packaging self-contained with Playwright Chromium, Chromium Headless Shell, and ffmpeg bundled into the exe.

## Validation
- Auth session seeded with `py scripts\ai_runner_access.py seed-session`.
- Compile check passed: `py -m compileall -q scripts link_inspector qa_lab`.
- Full local QA passed: `py qa_lab\run_suite.py` (315 tests).
- Live GUI smoke passed unarmed: `py qa_lab\live_gui_driver.py --monitor-polls 1 --auto-close-seconds 70`.
- Strict Nuitka onefile build passed: `py scripts\build.py --output-dir dist\release_1.4.1 --nuitka-only`.
- Packaged executable launch smoke passed: `releases\1.4.1\LinkPilot.exe` stayed alive for 45 seconds.
- Build output confirmed bundled Playwright directories:
  - `chromium-1208`
  - `chromium_headless_shell-1208`
  - `ffmpeg-1011`

## Artifact Integrity
- SHA-256 (`LinkPilot.exe`):
  - `317d4ffe14c0e3e85692404bec3c0bfbd81aca2ef8bd9cdd6795e52384365061`

## Notes
- This is a patch release because it preserves the 1.4 workflow while shipping the real-world checkout hardening that worked today.
- Live order submission remains gated behind paid pro entitlement, buy-ready item state, and the explicit live-submit arm.
- Built with Nuitka onefile on Python 3.14. Nuitka 4.0.8 reports Python 3.14 support as experimental.
- Onefile compression warning remains unless `zstandard` / `Nuitka[onefile]` is installed.
