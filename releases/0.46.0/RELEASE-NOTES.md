# CarCad 0.46.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored.

Plain release build: filenames and the UI show `0.46.0`, no test label. The Cloud features (cloud.01–cloud.08) are stubbed until the live CarCad Cloud service ships.

## 0.46.0

Batch 17 of ten features. Targets: cam3d.08, cam3d.09, cam3d.10, cam3d.11, cam3d.12, cam3d.13, cam3d.14, cam3d.15, cam3d.16, cam3d.17. Portable CTest 67/67 and Linux CTest 78/78 after independent cam3d.08–.17 fixtures. Linux x64 test packages stay under `test/linux-x64/0.46.0`.

- Add contour finishing (cam3d.08, `working_subset`). contour allowance millimetres become cam3dContour. Lead-in remains limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add ramp finishing (cam3d.09, `working_subset`). ramp angle degrees become cam3dRamp. Helix remains limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add pencil cleanup (cam3d.10, `working_subset`). pencil radius millimetres become cam3dPencil. Passes remain limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add horizontal finishing (cam3d.11, `working_subset`). horizontal stepdown millimetres become cam3dHorizontal. Detect remains limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add spiral finishing (cam3d.12, `working_subset`). spiral pitch millimetres become cam3dSpiral. Center remains limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add radial finishing (cam3d.13, `working_subset`). radial stepover millimetres become cam3dRadial. Origin remains limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add morph spiral finishing (cam3d.14, `working_subset`). morph spiral pitch millimetres become cam3dMorphSpiral. Blend remains limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add projected paths (cam3d.15, `working_subset`). project offset millimetres become cam3dProject. Curve remains limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add blended paths (cam3d.16, `working_subset`). blend factor becomes cam3dBlend. Guides remain limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add morph paths (cam3d.17, `working_subset`). morph factor becomes cam3dMorph. Surfaces remain limited. Short Browser label **3D CAM** plus `#help-cam3d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Register independent cam3d.08–.17 CTest fixtures (`cam3d_08_contour` … `cam3d_17_morph` in `native/cam3d_tests.cpp`). Each case uses its own document and is runnable as `CarCadCam3dTests cam3d.NN`. Portable CTest becomes 67 names; Linux full suite becomes 78.

**Platforms:** macOS (Apple silicon, arm64) only for now. Windows installers follow separately.
