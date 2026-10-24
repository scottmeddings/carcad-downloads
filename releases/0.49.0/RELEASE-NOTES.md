# CarCad 0.49.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored.

Plain release build: filenames and the UI show `0.49.0`, no test label. The Cloud features (cloud.01–cloud.08) are stubbed until the live CarCad Cloud service ships.

## 0.49.0

Batch 20 of ten features. Targets: turn.05, turn.06, turn.07, turn.08, turn.09, turn.10, turn.11, probing.01, probing.02, probing.03. Portable CTest 100/100 and Linux CTest 111/111 after independent turn.05–.11 and probing.01–.03 fixtures. Linux x64 test packages stay under `test/linux-x64/0.49.0`.

- Add thread turning (turn.05, `working_subset`). thread pitch millimetres become turnThread. Insert remains limited. Fixture `turn_05_thread` / CTest `turn.05`. Short Browser label **TURN** plus `#help-turn`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add parting (turn.06, `working_subset`). parting width millimetres become turnPart. Chamfer remains limited. Fixture `turn_06_part` / CTest `turn.06`. Short Browser label **TURN** plus `#help-turn`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add turning drilling (turn.07, `working_subset`). drill depth millimetres become turnDrill. Peck remains limited. Fixture `turn_07_drill` / CTest `turn.07`. Short Browser label **TURN** plus `#help-turn`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add part transfer (turn.08, `working_subset`). transfer offset millimetres become turnTransfer. Spindle remains limited. Fixture `turn_08_transfer` / CTest `turn.08`. Short Browser label **TURN** plus `#help-turn`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add live tooling (turn.09, `working_subset`). live tooling rpm become turnLive. Mill remains limited. Fixture `turn_09_live` / CTest `turn.09`. Short Browser label **TURN** plus `#help-turn`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add mill-turn synchronization (turn.10, `working_subset`). mill-turn phase degrees become turnSync. Wait remains limited. Fixture `turn_10_sync` / CTest `turn.10`. Short Browser label **TURN** plus `#help-turn`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add turned stock simulation (turn.11, `working_subset`). stock diameter millimetres become turnStock. Leftover remains limited. Fixture `turn_11_stock` / CTest `turn.11`. Short Browser label **TURN** plus `#help-turn`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add stock and part setup probing (probing.01, `working_subset`). setup clearance millimetres become probingSetup. Cycle remains limited. Fixture `probing_01_setup` / CTest `probing.01`. Short Browser label **PROBE** plus `#help-probing`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add probe geometry (probing.02, `working_subset`). geometry points become probingGeometry. Path remains limited. Fixture `probing_02_geometry` / CTest `probing.02`. Short Browser label **PROBE** plus `#help-probing`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add hole recognition (probing.03, `working_subset`). hole diameter millimetres become probingHole. Pattern remains limited. Fixture `probing_03_hole` / CTest `probing.03`. Short Browser label **PROBE** plus `#help-probing`. Standing acceptance: no long UI text; explanations behind a help (?) icon.

**Platforms:** macOS (Apple silicon, arm64) only for now. Windows installers follow separately.
