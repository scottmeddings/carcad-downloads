# CarCad 0.51.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored.

Plain release build: filenames and the UI show `0.51.0`, no test label. The Cloud features (cloud.01–cloud.08) are stubbed until the live CarCad Cloud service ships.

## 0.51.0

Batch 22 of ten features. Targets: additive.06, additive.07, additive.08, additive.09, additive.10, additive.11, additive.12, additive.13, additive.14, additive.15. Portable CTest 121/121 and Linux CTest 132/132 after independent additive.06–.15 fixtures. Linux x64 test packages stay under `test/linux-x64/0.51.0`.

- Add SLA and DLP printing (additive.06, `working_subset`). sla exposure seconds become additiveSla. Profile remains limited. Fixture `additive_06_sla` / CTest `additive.06`. Short Browser label **ADD** plus `#help-additive`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add SLS printing (additive.07, `working_subset`). sls powder millimetres become additiveSls. Bed remains limited. Fixture `additive_07_sls` / CTest `additive.07`. Short Browser label **ADD** plus `#help-additive`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add multi-jet printing (additive.08, `working_subset`). jet droplet picolitres become additiveJet. Head remains limited. Fixture `additive_08_jet` / CTest `additive.08`. Short Browser label **ADD** plus `#help-additive`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add metal powder-bed printing (additive.09, `working_subset`). metal laser watts become additiveMetal. Recoater remains limited. Fixture `additive_09_metal` / CTest `additive.09`. Short Browser label **ADD** plus `#help-additive`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add binder jet printing (additive.10, `working_subset`). binder saturation percent become additiveBinder. Cure remains limited. Fixture `additive_10_binder` / CTest `additive.10`. Short Browser label **ADD** plus `#help-additive`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add directed energy deposition (additive.11, `working_subset`). ded power watts become additiveDed. Wire remains limited. Fixture `additive_11_ded` / CTest `additive.11`. Short Browser label **ADD** plus `#help-additive`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add electron-beam printing (additive.12, `working_subset`). ebeam voltage kilovolts become additiveEbeam. Vacuum remains limited. Fixture `additive_12_ebeam` / CTest `additive.12`. Short Browser label **ADD** plus `#help-additive`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add additive process simulation (additive.13, `working_subset`). sim steps become additiveSim. Warp remains limited. Fixture `additive_13_sim` / CTest `additive.13`. Short Browser label **ADD** plus `#help-additive`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add build compensation (additive.14, `working_subset`). compensate scale percent become additiveCompensate. Scan remains limited. Fixture `additive_14_compensate` / CTest `additive.14`. Short Browser label **ADD** plus `#help-additive`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add printer output and post processing (additive.15, `working_subset`). post feed millimetres per second become additivePost. G-code remains limited. Fixture `additive_15_post` / CTest `additive.15`. Short Browser label **ADD** plus `#help-additive`. Standing acceptance: no long UI text; explanations behind a help (?) icon.

**Platforms:** macOS (Apple silicon, arm64) only for now. Windows installers follow separately.
