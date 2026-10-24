# CarCad 0.50.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored.

Plain release build: filenames and the UI show `0.50.0`, no test label. The Cloud features (cloud.01–cloud.08) are stubbed until the live CarCad Cloud service ships.

## 0.50.0

Batch 21 of ten features. Targets: probing.04, probing.05, probing.06, probing.07, probing.08, probing.09, additive.02, additive.03, additive.04, additive.05. Portable CTest 111/111 and Linux CTest 122/122 after independent probing.04–.09 and additive.02–.05 fixtures. Linux x64 test packages stay under `test/linux-x64/0.50.0`.

- Add part alignment (probing.04, `working_subset`). alignment offset millimetres become probingAlign. Fixture remains limited. Fixture `probing_04_alignment` / CTest `probing.04`. Short Browser label **PROBE** plus `#help-probing`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add freeform surface inspection (probing.05, `working_subset`). surface deviation millimetres become probingSurface. Scan remains limited. Fixture `probing_05_surface` / CTest `probing.05`. Short Browser label **PROBE** plus `#help-probing`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add manual measurement plans (probing.06, `working_subset`). plan points become probingPlan. Manual remains limited. Fixture `probing_06_plan` / CTest `probing.06`. Short Browser label **PROBE** plus `#help-probing`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add tolerance reports (probing.07, `working_subset`). report tolerance millimetres become probingReport. Cert remains limited. Fixture `probing_07_report` / CTest `probing.07`. Short Browser label **PROBE** plus `#help-probing`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add machine result import (probing.08, `working_subset`). import samples become probingImport. Machine remains limited. Fixture `probing_08_import` / CTest `probing.08`. Short Browser label **PROBE** plus `#help-probing`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add live inspection connections (probing.09, `working_subset`). live rate hertz become probingLive. Stream remains limited. Fixture `probing_09_live` / CTest `probing.09`. Short Browser label **PROBE** plus `#help-probing`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add orientation and arrangement (additive.02, `working_subset`). orient angle degrees become additiveOrient. Nest remains limited. Fixture `additive_02_orient` / CTest `additive.02`. Short Browser label **ADD** plus `#help-additive`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add support structures (additive.03, `working_subset`). support density percent become additiveSupport. Tree remains limited. Fixture `additive_03_support` / CTest `additive.03`. Short Browser label **ADD** plus `#help-additive`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add slicing and build strategies (additive.04, `working_subset`). slice layer millimetres become additiveSlice. Infill remains limited. Fixture `additive_04_slice` / CTest `additive.04`. Short Browser label **ADD** plus `#help-additive`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add FFF printing (additive.05, `working_subset`). fff width millimetres become additiveFff. Printer remains limited. Fixture `additive_05_fff` / CTest `additive.05`. Short Browser label **ADD** plus `#help-additive`. Standing acceptance: no long UI text; explanations behind a help (?) icon.

**Platforms:** macOS (Apple silicon, arm64) only for now. Windows installers follow separately.
