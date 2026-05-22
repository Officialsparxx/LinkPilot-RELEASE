# LinkPilot 1.4.3 Release

## Artifact

- `LinkPilot.exe`

## Install / Update

Download `LinkPilot.exe` and run it directly. No Python, Playwright, browser, plugin, or helper-script setup is required for normal users.

## Hotfix Scope

This build fixes the packaged-app persistent login browser failure seen when opening saved account profiles from the Accounts tab.

## Included Runtime Assets

- Playwright Chromium
- Playwright Chromium Headless Shell
- Default source/proxy/CAPTCHA plugins
- LinkPilot logo assets
- Packaged helper scripts for login priming and sidecar CLI operations

Sensitive local state is not included: credentials, browser profiles, launch sessions, logs, caches, and local env files remain excluded.
