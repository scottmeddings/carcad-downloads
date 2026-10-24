# CarCad 0.48.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored.

Plain release build: filenames and the UI show `0.48.0`, no test label. The Cloud features (cloud.01–cloud.08) are stubbed until the live CarCad Cloud service ships.

## 0.48.0

Batch 19 of ten features. Targets: multiaxis.07, multiaxis.08, multiaxis.09, multiaxis.10, multiaxis.11, multiaxis.12, turn.01, turn.02, turn.03, turn.04. Portable CTest 89/89 and Linux CTest 100/100 after independent turn.01–.04 and multiaxis.07–.12 fixtures. Linux x64 test packages stay under `test/linux-x64/0.48.0`.

- Add multi-axis roughing (multiaxis.07, `working_subset`). roughing stepover millimetres become multiaxisRoughing. Rest remains limited. Fixture `multiaxis_07_roughing` / CTest `multiaxis.07`. Short Browser label **5X CAM** plus `#help-multiaxis`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add multi-axis contours (multiaxis.08, `working_subset`). contour allowance millimetres become multiaxisContour. Lead remains limited. Fixture `multiaxis_08_contour` / CTest `multiaxis.08`. Short Browser label **5X CAM** plus `#help-multiaxis`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add rotary roughing and finishing (multiaxis.09, `working_subset`). rotary diameter millimetres become multiaxisRotary. Unroll remains limited. Fixture `multiaxis_09_rotary` / CTest `multiaxis.09`. Short Browser label **5X CAM** plus `#help-multiaxis`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add tool axis constraints (multiaxis.10, `working_subset`). tool axis tilt degrees become multiaxisAxis. Lock remains limited. Fixture `multiaxis_10_axis` / CTest `multiaxis.10`. Short Browser label **5X CAM** plus `#help-multiaxis`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add automatic collision avoidance (multiaxis.11, `working_subset`). collision clearance millimetres become multiaxisCollision. Stock remains limited. Fixture `multiaxis_11_collision` / CTest `multiaxis.11`. Short Browser label **5X CAM** plus `#help-multiaxis`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add clearance geometry (multiaxis.12, `working_subset`). clearance offset millimetres become multiaxisClearance. Wrap remains limited. Fixture `multiaxis_12_clearance` / CTest `multiaxis.12`. Short Browser label **5X CAM** plus `#help-multiaxis`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add turning setups (turn.01, `working_subset`). setup spindle RPM become turnSetup. Chuck remains limited. Fixture `turn_01_setup` / CTest `turn.01`. Short Browser label **TURN** plus `#help-turn`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add OD and ID profiling (turn.02, `working_subset`). profile allowance millimetres become turnProfile. Stock remains limited. Fixture `turn_02_profile` / CTest `turn.02`. Short Browser label **TURN** plus `#help-turn`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add facing (turn.03, `working_subset`). face allowance millimetres become turnFace. Start remains limited. Fixture `turn_03_face` / CTest `turn.03`. Short Browser label **TURN** plus `#help-turn`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add grooves (turn.04, `working_subset`). groove width millimetres become turnGroove. Relief remains limited. Fixture `turn_04_groove` / CTest `turn.04`. Short Browser label **TURN** plus `#help-turn`. Standing acceptance: no long UI text; explanations behind a help (?) icon.

**Platforms:** macOS (Apple silicon, arm64) only for now. Windows installers follow separately.
