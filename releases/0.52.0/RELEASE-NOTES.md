# CarCad 0.52.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored.

Plain release build: filenames and the UI show `0.52.0`, no test label. The Cloud features (cloud.01–cloud.08) are stubbed until the live CarCad Cloud service ships.

## 0.52.0

Batch 23 of ten features. Targets: nest.01, nest.02, nest.03, nest.04, nest.05, nest.06, nest.07, nest.08, nest.09, simulation.01. Portable CTest 133/133 and Linux CTest 144/144 after independent nest.01–.09 and simulation.01 fixtures. Linux x64 test packages stay under `test/linux-x64/0.52.0`.

- Add material and packaging libraries (nest.01, `working_subset`). material thickness millimetres become nestMaterial. Grain remains limited. Fixture `nest_01_material` / CTest `nest.01`. Short Browser label **NEST** plus `#help-nest`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add nest preparation (nest.02, `working_subset`). prepare gap millimetres become nestPrepare. Stock remains limited. Fixture `nest_02_prepare` / CTest `nest.02`. Short Browser label **NEST** plus `#help-nest`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add part quantity and grain rules (nest.03, `working_subset`). quantity count become nestQuantity. Grain remains limited. Fixture `nest_03_quantity` / CTest `nest.03`. Short Browser label **NEST** plus `#help-nest`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add advanced arrangement (nest.04, `working_subset`). arrange rotate degrees become nestArrange. Nest remains limited. Fixture `nest_04_arrange` / CTest `nest.04`. Short Browser label **NEST** plus `#help-nest`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add nest studies (nest.05, `working_subset`). study sheets become nestStudy. Compare remains limited. Fixture `nest_05_study` / CTest `nest.05`. Short Browser label **NEST** plus `#help-nest`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add nest comparisons (nest.06, `working_subset`). compare yield percent become nestCompare. Cost remains limited. Fixture `nest_06_compare` / CTest `nest.06`. Short Browser label **NEST** plus `#help-nest`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add sheet utilization (nest.07, `working_subset`). utilize percent become nestUtilize. Remnant remains limited. Fixture `nest_07_utilize` / CTest `nest.07`. Short Browser label **NEST** plus `#help-nest`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add nest export (nest.08, `working_subset`). export scale become nestExport. DXF remains limited. Fixture `nest_08_export` / CTest `nest.08`. Short Browser label **NEST** plus `#help-nest`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add laser waterjet and plasma paths (nest.09, `working_subset`). path kerf millimetres become nestPath. Pierce remains limited. Fixture `nest_09_path` / CTest `nest.09`. Short Browser label **NEST** plus `#help-nest`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add simulation model simplification (simulation.01, `working_subset`). simplify faces become simSimplify. Mesh remains limited. Fixture `simulation_01_simplify` / CTest `simulation.01`. Short Browser label **SIM** plus `#help-simulation`. Standing acceptance: no long UI text; explanations behind a help (?) icon.

**Platforms:** macOS (Apple silicon, arm64) only for now. Windows installers follow separately.
