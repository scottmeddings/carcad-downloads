# CarCad 0.45.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored.

Plain release build: filenames and the UI show `0.45.0`, no test label. The Cloud features (cloud.01–cloud.08) are stubbed until the live CarCad Cloud service ships.

## 0.45.0

Batch 16 of ten features. Targets: cam2d.10, cam2d.11, cam2d.12, cam3d.01, cam3d.02, cam3d.03, cam3d.04, cam3d.05, cam3d.06, cam3d.07. Portable CTest 57/57 and Linux CTest 68/68 after cam3d.07 (includes `cam3d`). Linux x64 test packages stay under `test/linux-x64/0.45.0`.

- Add engraving (cam2d.10, `working_subset`). engraving depth millimetres become cam2dEngrave. Fonts remain limited. Short Browser label **2D CAM** plus `#help-cam2d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add chamfer milling (cam2d.11, `working_subset`). chamfer width millimetres become cam2dChamfer. Tip control remains limited. Short Browser label **2D CAM** plus `#help-cam2d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add rest material machining (cam2d.12, `working_subset`). rest leave millimetres become cam2dRest. Stock rest remains limited. Short Browser label **2D CAM** plus `#help-cam2d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add 3D adaptive roughing (cam3d.01, `working_subset`). adaptive stepover millimetres become cam3dAdaptive. Rest remains limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add 3D offset roughing (cam3d.02, `working_subset`). offset stepover millimetres become cam3dOffset. Islands remain limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add positional roughing (cam3d.03, `working_subset`). positional tilt degrees become cam3dPositional. 5-axis remains limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add steep and shallow finishing (cam3d.04, `working_subset`). steep angle degrees become cam3dSteep. Shallow pairing remains limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add flat finishing (cam3d.05, `working_subset`). flat allowance millimetres become cam3dFlat. Detect remains limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add parallel finishing (cam3d.06, `working_subset`). parallel stepover millimetres become cam3dParallel. Angle remains limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add scallop finishing (cam3d.07, `working_subset`). scallop stepover millimetres become cam3dScallop. Cusp remains limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.

**Platforms:** macOS (Apple silicon, arm64) only for now. Windows installers follow separately.
