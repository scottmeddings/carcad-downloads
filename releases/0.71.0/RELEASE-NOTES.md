# CarCad 0.71.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored. Verified locally instead: Linux CTest 304/304 (test build) and 302 names on the release build (288 passed, 14 skipped that need test-build hooks, 0 failed), Windows ARM64 CTest 300/300 and x64 CTest 300/300 (release build, x64 under emulation), macOS CTest 287/301 on the release build (13 skipped; one MCP test timed out in the build environment, see the CarCad repo notes), Linux packaging, snap review and smoke tests on the release build.

Plain release build: filenames and the UI show 0.71.0, no test label.

## What's new

- **Browser panel** (platform.09): a document Browser panel with MCP commands.
- **Windows setup wizard** (platform.10): a CarCad-branded Setup for ARM64 and x64 with license, install location, Start Menu, shortcut and WebView2 pages, and a branded uninstall. CarCad installs per user in `%LOCALAPPDATA%\Programs\CarCad`.
- **Open from CarCad Cloud and Marketplace** (cloud.05-08): open a Cloud project in CarCad, live Marketplace listings, Open in CarCad from a listing, and a smoother sign-in hand-off.
- **Grid size** (sketch.21): Settings > Grid size, plus MCP tools to read and set it (50-10000 mm, default 500 x 500 mm).
- **Drawings**: tests for 12 drawing features with the bugs they found fixed; old invalid GD&T frames still open and are flagged in red, with an optional strict mode.
- **Secret storage** on Linux and macOS: authenticated encryption for saved sign-ins and keys, files private (0600) from creation; older files are migrated once.
- **Fixes from audits**: thumbnail host allow-list, stricter Marketplace message replay checks, a sign-in startup fix, and limits on the local MCP endpoint.

## Platforms in this release

- macOS (Apple silicon, arm64): `CarCad-0.71.0-macOS.dmg`
- Windows ARM64: `CarCad-0.71.0-Windows-ARM64-Setup.exe`, `CarCad-0.71.0-Windows-ARM64.msi`
- Windows x64: `CarCad-0.71.0-Windows-x64-Setup.exe`, `CarCad-0.71.0-Windows-x64.msi`
- Linux x64: `CarCad-0.71.0-linux-x64.AppImage`, `carcad_0.71.0_amd64.deb`, `carcad_0.71.0_amd64.snap` (built on Ubuntu 24.04 / core24, snap-review pass)

## Install on Linux (x64)

- **AppImage**: `chmod +x CarCad-0.71.0-linux-x64.AppImage` then run `./CarCad-0.71.0-linux-x64.AppImage`.
- **Debian / Ubuntu (.deb)**: `sudo apt install ./carcad_0.71.0_amd64.deb`
- **Snap**: `sudo snap install --dangerous carcad_0.71.0_amd64.snap` (`--dangerous` is needed until CarCad is in the Snap Store). Snap Store availability for 0.71.0 follows separately.

## Install on macOS (Apple silicon, arm64)

- Open `CarCad-0.71.0-macOS.dmg` and drag CarCad to Applications. The app is ad hoc signed, not notarised.

## Install on Windows (ARM64 or x64)

- Choose ARM64 for Windows PCs with an ARM-based processor, x64 for 64-bit Intel or AMD processors.
- **Setup.exe**: run `CarCad-0.71.0-Windows-ARM64-Setup.exe` or `CarCad-0.71.0-Windows-x64-Setup.exe`.
- **MSI**: run `CarCad-0.71.0-Windows-ARM64.msi` or `CarCad-0.71.0-Windows-x64.msi`.
- The installers are unsigned, so Windows SmartScreen may warn. Choose **More info**, then **Run anyway**.
- The x64 build was tested under x64 emulation on Windows 11 ARM64, not on native x64 hardware.

Verify downloads against `SHA256SUMS.txt`.
