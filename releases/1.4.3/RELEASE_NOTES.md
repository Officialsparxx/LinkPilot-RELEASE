# LinkPilot 1.4.3

Patch hotfix for the public 1.4.2 build.

- Fixed the Accounts tab **Open Persistent Login** action failing with Playwright's sync-API-inside-asyncio-loop error in packaged builds.
- Persistent login browser automation now runs on a dedicated Playwright owner thread while keeping the same UI workflow for login priming, focus, autofill, and profile reuse.
- Preserves the 1.4.2 release packaging hardening: bundled Playwright Chromium, Chromium Headless Shell, default plugins, logo assets, and helper scripts.

Users preparing for Target/Walmart/Sam's drops should update from 1.4.2 to 1.4.3 before opening account persistent-login profiles.
