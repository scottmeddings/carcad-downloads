# CarCad 0.44.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored.

Plain release build: filenames and the UI show `0.44.0`, no test label. The Cloud features (cloud.01–cloud.08) are stubbed until the live CarCad Cloud service ships.

## 0.44.0

Batch 15 of ten features. Targets: mfg_setup.13, cam2d.01, cam2d.02, cam2d.03, cam2d.04, cam2d.05, cam2d.06, cam2d.07, cam2d.08, cam2d.09. Portable CTest 56/56 and Linux CTest 67/67 after cam2d.09 (includes `cam2d`). Linux x64 test packages stay under `test/linux-x64/0.44.0`.

- Add NC programs and post processing (mfg_setup.13, `working_subset`). Named programs become manufacturingProgram. DNC remains limited. Short Browser label **Setup** plus `#help-mfg-setup`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add adaptive roughing (cam2d.01, `working_subset`). adaptive stepover millimetres become cam2dAdaptive. Rest machining remains limited. Short Browser label **2D CAM** plus `#help-cam2d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add offset roughing (cam2d.02, `working_subset`). offset stepover millimetres become cam2dOffset. Islands remain limited. Short Browser label **2D CAM** plus `#help-cam2d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add facing (cam2d.03, `working_subset`). facing depth millimetres become cam2dFacing. Stock facing remains limited. Short Browser label **2D CAM** plus `#help-cam2d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add contours (cam2d.04, `working_subset`). contours allowance millimetres become cam2dContour. Lead-in remains limited. Short Browser label **2D CAM** plus `#help-cam2d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add slots (cam2d.05, `working_subset`). slots width millimetres become cam2dSlot. Finish pass remains limited. Short Browser label **2D CAM** plus `#help-cam2d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add tracing (cam2d.06, `working_subset`). tracing offset millimetres become cam2dTrace. Chamfer tracing remains limited. Short Browser label **2D CAM** plus `#help-cam2d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add thread milling (cam2d.07, `working_subset`). thread pitch millimetres become cam2dThread. Tapping remains limited. Short Browser label **2D CAM** plus `#help-cam2d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add boring (cam2d.08, `working_subset`). boring diameter millimetres become cam2dBore. Peck remains limited. Short Browser label **2D CAM** plus `#help-cam2d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add circular milling (cam2d.09, `working_subset`). circular diameter millimetres become cam2dCircular. Helix remains limited. Short Browser label **2D CAM** plus `#help-cam2d`. Standing acceptance: no long UI text; explanations behind a help (?) icon.

**Platforms:** macOS (Apple silicon, arm64) only for now. Windows installers follow separately.
