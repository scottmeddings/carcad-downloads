# CarCad 0.70.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored. Verified locally instead: Linux CTest 281/281 (test build) and macOS packaging/smoke on the Mac mini.

Plain release build: filenames and the UI show 0.70.0, no test label.

## What's new

- MCP server (mcp.01-11): CarCad can be driven by AI tools through the bundled CarCadMCP helper.
- New **Allow AI to control CarCad** switch; MCP stays off until you turn it on.
- Chat over MCP.
- Relay client (provisional).
- Sign-in fixes.
- Browser fixes.
- Install retries now back off.

## Platforms in this release

- macOS (Apple silicon, arm64): `CarCad-0.70.0-macOS.dmg`
- Linux x64: `CarCad-0.70.0-linux-x64.AppImage`, `carcad_0.70.0_amd64.deb`
- **Windows ARM64 and x64: not in this release.** The Windows build failed to compile; Windows users should stay on 0.69.0 until a fixed build ships.
- **Linux snap: not in this release.** Use the AppImage or .deb.

## Install on Linux (x64)

- **AppImage**: `chmod +x CarCad-0.70.0-linux-x64.AppImage` then run `./CarCad-0.70.0-linux-x64.AppImage`.
- **Debian / Ubuntu (.deb)**: `sudo apt install ./carcad_0.70.0_amd64.deb`

## Install on macOS (Apple silicon, arm64)

- Open `CarCad-0.70.0-macOS.dmg` and drag CarCad to Applications.

Verify downloads against `SHA256SUMS.txt`.
