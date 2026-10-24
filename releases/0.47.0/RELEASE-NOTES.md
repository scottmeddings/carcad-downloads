# CarCad 0.47.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored.

Plain release build: filenames and the UI show `0.47.0`, no test label. The Cloud features (cloud.01–cloud.08) are stubbed until the live CarCad Cloud service ships.

## 0.47.0

Batch 18 of ten features. Targets: cam3d.18, cam3d.19, cam3d.20, cam3d.21, multiaxis.01, multiaxis.02, multiaxis.03, multiaxis.04, multiaxis.05, multiaxis.06. Portable CTest 78/78 and Linux CTest 89/89 after independent cam3d.18–.21 and multiaxis.01–.06 fixtures. Linux x64 test packages stay under `test/linux-x64/0.47.0`.

- Add corner finishing (cam3d.18, `working_subset`). corner radius millimetres become cam3dCorner. Detect remains limited. Fixture `cam3d_18_corner` / CTest `cam3d.18`. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add flow finishing (cam3d.19, `working_subset`). flow stepover millimetres become cam3dFlow. UV remains limited. Fixture `cam3d_19_flow` / CTest `cam3d.19`. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add deburring (cam3d.20, `working_subset`). deburr width millimetres become cam3dDeburr. Edges remain limited. Fixture `cam3d_20_deburr` / CTest `cam3d.20`. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add geodesic finishing (cam3d.21, `working_subset`). geodesic stepover millimetres become cam3dGeodesic. Seed remains limited. Fixture `cam3d_21_geodesic` / CTest `cam3d.21`. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add indexed tool orientations (multiaxis.01, `working_subset`). indexed tilt degrees become multiaxisIndexed. Table remains limited. Fixture `multiaxis_01_indexed` / CTest `multiaxis.01`. Short Browser label **5X CAM** plus `#help-multiaxis`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add wrapped rotary paths (multiaxis.02, `working_subset`). wrapped diameter millimetres become multiaxisWrapped. Unroll remains limited. Fixture `multiaxis_02_wrapped` / CTest `multiaxis.02`. Short Browser label **5X CAM** plus `#help-multiaxis`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add simultaneous four-axis paths (multiaxis.03, `working_subset`). four-axis lead degrees become multiaxisFour. Continuous remains limited. Fixture `multiaxis_03_four` / CTest `multiaxis.03`. Short Browser label **5X CAM** plus `#help-multiaxis`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add simultaneous five-axis paths (multiaxis.04, `working_subset`). five-axis tilt degrees become multiaxisFive. Collision remains limited. Fixture `multiaxis_04_five` / CTest `multiaxis.04`. Short Browser label **5X CAM** plus `#help-multiaxis`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add swarf cutting (multiaxis.05, `working_subset`). swarf angle degrees become multiaxisSwarf. Blend remains limited. Fixture `multiaxis_05_swarf` / CTest `multiaxis.05`. Short Browser label **5X CAM** plus `#help-multiaxis`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add advanced swarf (multiaxis.06, `working_subset`). advanced swarf stepover millimetres become multiaxisAdvancedSwarf. Floor remains limited. Fixture `multiaxis_06_advanced` / CTest `multiaxis.06`. Short Browser label **5X CAM** plus `#help-multiaxis`. Standing acceptance: no long UI text; explanations behind a help (?) icon.

**Platforms:** macOS (Apple silicon, arm64) only for now. Windows installers follow separately.
