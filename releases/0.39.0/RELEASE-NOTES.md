# CarCad 0.39.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored.

Batch 10 of ten features (in progress). `CARCAD_TEST_BUILD` is ON: filenames use `0.39.0-test` and the UI says `0.39.0 (test version)`. Numeric `version` stays `0.39.0`. Targets: configuration.01, configuration.02, configuration.03, configuration.04, configuration.05, configuration.06, configuration.07, configuration.08, configuration.09, configuration.10.

- Add variant tables (configuration.01, `working_subset`). Named configuration rows with one active id. Configured dimensions remain limited. Browser label **Variants** plus `#help-configurations`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add configured dimensions (configuration.02, `working_subset`). Active row width/length/height replace the first box or cylinder size. Live parameter tables remain limited. Short Browser label **Variants** plus `#help-configurations`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add configured suppression (configuration.03, `working_subset`). Active row suppressed indexes set feature.suppressed. Face-level suppression remains limited. Short Browser label **Variants** plus `#help-configurations`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add material and appearance variants (configuration.04, `working_subset`). Active row material and appearance strings are copied onto the document. Face appearances remain limited. Short Browser label **Variants** plus `#help-configurations`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add configured external components (configuration.05, `working_subset`). Active row external id must match a linked component when set. Live path updates remain limited. Short Browser label **Variants** plus `#help-configurations`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add configuration rules (configuration.06, `working_subset`). Active row rules set matching parameter expressions to a number. Conditional rules remain limited. Short Browser label **Variants** plus `#help-configurations`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add variant assemblies (configuration.07, `working_subset`). Active row assembly id must match an occurrence when set. Config-specific mates remain limited. Short Browser label **Variants** plus `#help-configurations`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add variant drawings (configuration.08, `working_subset`). Active row drawing name is stored. Generated drawing views per variant remain limited. Short Browser label **Variants** plus `#help-configurations`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add variant manufacturing setups (configuration.09, `working_subset`). Active row cam name is stored. Toolpaths remain limited. Short Browser label **Variants** plus `#help-configurations`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add variant simulation inputs (configuration.10, `working_subset`). Active row simulation name is stored. Solver studies remain limited. Short Browser label **Variants** plus `#help-configurations`. Standing acceptance: no long UI text; explanations behind a help (?) icon.

**Platforms:** macOS (Apple silicon, arm64) only for now. Windows installers are coming in a later update to this release.
