# CarCad 0.36.0 — 23 Oct 2026

CI waived by Scott on 18 Oct 2026, re-run when billing is restored.

Batch 7 of ten features. One minor version per batch of 10. Targets: mesh.11, mesh.13, form.01, form.02, form.03, form.04, form.05, form.06, form.07, form.08 as working subsets.

- Add mesh booleans (mesh.11, `working_subset`). Union appends a millimetre AABB tool box; cut/intersect keep or drop triangles by centroid. Triangle-triangle CSG remains limited. Short Mesh-tool label **Boolean** plus `#help-workspace-tools`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add texture extrusion (mesh.13, `working_subset`). Vertices offset along averaged face normals by amplitude × sin(2π x / wavelength + 1.2). Image-based height maps remain limited. Short Mesh-tool label **Texture**. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add subdivision primitives (form.01, `working_subset`). Empty-project **Box** control cage (subdivided AABB mesh). Other primitives and Catmull-Clark remain limited. FORM tab plus `#help-workspace-tools`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add control cage editing (form.02, `working_subset`). Translate vertices on the positive side of X/Y/Z by delta. Direct 3D manipulators remain limited. Short Form-tool label **Edit**. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add extruded freeform faces (form.03, `working_subset`). Top (max Z) cage vertices offset along Z by distance. Selected-face extrude remains limited. Short Form-tool label **Extrude**. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add freeform sweep and loft (form.04, `working_subset`). Top cage scaled toward its XY centroid by topScale. Path sweep remains limited. Short Form-tool label **Loft**. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add creases and smoothing (form.05, `working_subset`). Laplacian smoothing holds AABB-corner vertices as creases. Painted edge weights remain limited. Short Form-tool label **Crease**. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add symmetry (form.06, `working_subset`). Mirror the cage across X=0 and append the reflected triangles. Live multi-axis symmetry remains limited. Short Form-tool label **Symmetry**. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add bridge faces (form.07, `working_subset`). A square tube of triangles spans min-X to max-X through the cage centre. Selected-face bridges remain limited. Short Form-tool label **Bridge**. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add weld and merge (form.08, `working_subset`). Weld cage vertices within a millimetre tolerance. Interactive merge of selected vertices remains limited. Short Form-tool label **Weld**. Standing acceptance: no long UI text; explanations behind a help (?) icon.

**Platforms:** macOS (Apple silicon, arm64) only for now. Windows installers are coming in a later update to this release.
