# CarCad 0.65.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored.

The Cloud features (cloud.01–cloud.08) are stubbed until the live CarCad Cloud service ships. For macOS, this release also includes the changes from 0.53.0 through 0.64.0, which were not published as separate macOS releases.

## Install on Linux (x64)

- **AppImage** (most distributions): `chmod +x CarCad-0.65.0-linux-x64.AppImage` then run `./CarCad-0.65.0-linux-x64.AppImage`.
- **Debian / Ubuntu (.deb)**: `sudo apt install ./carcad_0.65.0_amd64.deb`
- **Snap**: `sudo snap install --dangerous carcad_0.65.0_amd64.snap` (`--dangerous` is needed until CarCad is in the Snap Store).

## Install on macOS (Apple silicon, arm64)

- Open `CarCad-0.65.0-macOS.dmg` and drag CarCad to Applications.

## Install on Windows (ARM64 or x64)

- Choose ARM64 for Windows PCs with an ARM-based processor, x64 for 64-bit Intel or AMD processors.
- **Setup.exe**: run `CarCad-0.65.0-Windows-ARM64-Setup.exe` or `CarCad-0.65.0-Windows-x64-Setup.exe`.
- **MSI**: run `CarCad-0.65.0-Windows-ARM64.msi` or `CarCad-0.65.0-Windows-x64.msi`.
- The installers are unsigned, so Windows SmartScreen may warn. Choose **More info**, then **Run anyway**.
- The x64 build was tested under x64 emulation on Windows 11 ARM64, not on native x64 hardware.

Verify downloads against `SHA256SUMS.txt`.

## 0.65.0

Batch 36 is the seventh stub-rework batch. Plain release build: filenames and the UI show 0.65.0, no test label. Targets: turn.05, turn.06, turn.07, turn.08, turn.09, turn.10, turn.11, probing.01, probing.02, probing.03. Portable CTest 229/229 and Linux CTest 240/240 after turn.05–.11 and probing.01–.03.

- Rework thread turning (turn.05, `working_subset`). OD thread steps in from stock, sampling Z by pitch as turnPath / turnNcProgram. Insert remains limited. Fixture `turn_05_thread` / CTest `turn.05`.
- Rework parting (turn.06, `working_subset`). Plunge inward from the stock near zmin as turnPath / turnNcProgram. Chamfer remains limited. Fixture `turn_06_part` / CTest `turn.06`.
- Rework turning drilling (turn.07, `working_subset`). Axial drill from zmax by depth as turnPath / turnNcProgram. Peck remains limited. Fixture `turn_07_drill` / CTest `turn.07`.
- Rework part transfer (turn.08, `working_subset`). XZ move of the stock envelope by offset as turnPath / turnNcProgram. Spindle remains limited. Fixture `turn_08_transfer` / CTest `turn.08`.
- Rework live tooling (turn.09, `working_subset`). Radial OD mill as turnPath / turnNcProgram. C-axis milling remains limited. Fixture `turn_09_live` / CTest `turn.09`.
- Rework mill-turn synchronization (turn.10, `working_subset`). Phase-indexed live mill as turnPath / turnNcProgram. Wait remains limited. Fixture `turn_10_sync` / CTest `turn.10`.
- Rework turned stock simulation (turn.11, `working_subset`). Stock envelope from the programmed diameter as turnPath / turnNcProgram. Leftover removal is not simulated. Fixture `turn_11_stock` / CTest `turn.11`.
- Rework stock and part setup probing (probing.01, `working_subset`). Clearance approach to the part top as probingPath / probingNcProgram. Cycle remains limited. Fixture `probing_01_setup` / CTest `probing.01`. Short Browser label **PROBE** plus `#help-probing`.
- Rework probe geometry (probing.02, `working_subset`). Offset-profile sample points as probingPath / probingNcProgram. Scan remains limited. Fixture `probing_02_geometry` / CTest `probing.02`.
- Rework hole recognition (probing.03, `working_subset`). Circle the document hole (L at 4,4) as probingPath / probingNcProgram. Pattern remains limited. Fixture `probing_03_hole` / CTest `probing.03`.

**Platforms:** Linux x64, macOS (Apple silicon, arm64), and Windows ARM64 and x64.
