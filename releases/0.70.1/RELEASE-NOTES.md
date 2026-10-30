# CarCad 0.70.1

CI waived by Scott on 18 Oct 2026, re-run when billing is restored. Verified locally instead: Windows ARM64 and x64 CTest 280/280, Linux and macOS packaging and smoke tests on the release build.

Plain release build: filenames and the UI show 0.70.1, no test label. This release brings every platform, including Windows, to 0.70.1 and includes everything in 0.70.0 (MCP server via the bundled CarCadMCP helper, the **Allow AI to control CarCad** switch, chat over MCP, sign-in and browser fixes).

## What's fixed

- Windows build fixed: a Windows header clash that stopped 0.70.0 compiling on Windows.
- Relay client aligned to CarCad Cloud draft.11.
- Windows build script now honours the test-build flag, so release builds are plain release builds.
- Test fixture fix for the relay client tests.

## Platforms in this release

- macOS (Apple silicon, arm64): `CarCad-0.70.1-macOS.dmg`
- Windows ARM64: `CarCad-0.70.1-Windows-ARM64-Setup.exe`, `CarCad-0.70.1-Windows-ARM64.msi`
- Windows x64: `CarCad-0.70.1-Windows-x64-Setup.exe`, `CarCad-0.70.1-Windows-x64.msi`
- Linux x64: `CarCad-0.70.1-linux-x64.AppImage`, `carcad_0.70.1_amd64.deb`
- **Linux snap: coming in a follow-up upload to this same release.** Until then, use the AppImage or .deb.

## Install on Linux (x64)

- **AppImage**: `chmod +x CarCad-0.70.1-linux-x64.AppImage` then run `./CarCad-0.70.1-linux-x64.AppImage`.
- **Debian / Ubuntu (.deb)**: `sudo apt install ./carcad_0.70.1_amd64.deb`

## Install on macOS (Apple silicon, arm64)

- Open `CarCad-0.70.1-macOS.dmg` and drag CarCad to Applications.

## Install on Windows (ARM64 or x64)

- Choose ARM64 for Windows PCs with an ARM-based processor, x64 for 64-bit Intel or AMD processors.
- **Setup.exe**: run `CarCad-0.70.1-Windows-ARM64-Setup.exe` or `CarCad-0.70.1-Windows-x64-Setup.exe`.
- **MSI**: run `CarCad-0.70.1-Windows-ARM64.msi` or `CarCad-0.70.1-Windows-x64.msi`.
- The installers are unsigned, so Windows SmartScreen may warn. Choose **More info**, then **Run anyway**.
- The x64 build was tested under x64 emulation on Windows 11 ARM64, not on native x64 hardware.

Verify downloads against `SHA256SUMS.txt`.
