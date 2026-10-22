# CarCad 0.38.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored.

Batch 9 of ten features (in progress). `CARCAD_TEST_BUILD` is ON: filenames use `0.38.0-test` and the UI says `0.38.0 (test version)`. Numeric `version` stays `0.38.0`. Targets: plastic.02, plastic.03, plastic.04, plastic.05, plastic.06, plastic.07, plastic.08, plastic.09, plastic.10, plastic.11.

- Add bosses (plastic.02, `working_subset`). `plastic_boss` fuses a cylinder on the +Z AABB face. Draft, hole and fillet remain limited. Short Plastic-tool label **Boss** plus `#help-plastic-tools`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add snap fasteners (plastic.03, `working_subset`). `plastic_snap` fuses a rectangular tab on the max-X AABB face. Hook undercut and mating hole remain limited. Short Plastic-tool label **Snap** plus `#help-plastic-tools`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add support rests (plastic.04, `working_subset`). `plastic_rest` fuses a pad on the min-Z AABB face. Draft and rest arrays remain limited. Short Plastic-tool label **Rest** plus `#help-plastic-tools`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add lip and groove joints (plastic.05, `working_subset`). `plastic_groove` cuts a slot along the max-Y AABB face. Mating lip and groove radius remain limited. Short Plastic-tool label **Groove** plus `#help-plastic-tools`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add automated ribs and webs (plastic.06, `working_subset`). `plastic_rib` fuses a thin wall on the +Z AABB face along X. Auto web networks and draft remain limited. Short Plastic-tool label **Rib** plus `#help-plastic-tools`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add geometric pattern rules (plastic.07, `working_subset`). `plastic_pattern` fuses count≥2 cylinders along X on the +Z AABB face. Circular and face patterns remain limited. Short Plastic-tool label **Pattern** plus `#help-plastic-tools`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add volumetric lattices (plastic.08, `working_subset`). `plastic_lattice` cuts a through-Z cylinder unit cell. Gyroid/TPMS and 3D cell arrays remain limited. Short Plastic-tool label **Lattice** plus `#help-plastic-tools`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add manufacturability advice (plastic.09, `working_subset`). `plastic_advice` passes when AABB min ≥ thickness and max/min ≤ 20. Fill analysis remains limited. Short Plastic-tool label **Advice** plus `#help-plastic-tools`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add configuration validity rules (plastic.10, `working_subset`). `plastic_config` requires AABB min extent to match stored thickness within 0.05 mm. Feature-suppression configs remain limited. Short Plastic-tool label **Config** plus `#help-plastic-tools`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add similar component search (plastic.11, `working_subset`). `plastic_similar` matches AABB extents to stored width/length/height within tolerance. Library search remains limited. Short Plastic-tool label **Similar** plus `#help-plastic-tools`. Standing acceptance: no long UI text; explanations behind a help (?) icon.

**Platforms:** macOS (Apple silicon, arm64) only for now. Windows installers are coming in a later update to this release.
