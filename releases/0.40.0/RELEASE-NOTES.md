# CarCad 0.40.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored.

Batch 11 of ten features (in progress). `CARCAD_TEST_BUILD` is ON: filenames use `0.40.0-test` and the UI says `0.40.0 (test version)`. Numeric `version` stays `0.40.0`. Targets: render.01, render.02, render.03, render.04, render.05, render.06, render.07, render.08, render.09, render.10.

- Add material appearances (render.01, `working_subset`). Named appearance RGB 0–1 fills a portable PPM. Texture mapping remains limited. Browser label **Render** plus `#help-render`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add texture mapping (render.02, `working_subset`). Texture scaleU/scaleV and offsetU/offsetV drive a checker on the portable PPM. PBR maps remain limited. Short Browser label **Render** plus `#help-render`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add lighting environments (render.03, `working_subset`). Environment studio, outdoor or indoor scales the portable PPM. HDRI files remain limited. Short Browser label **Render** plus `#help-render`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add point and spot lights (render.04, `working_subset`). Up to four point or spot lights with position and intensity scale the portable PPM. IES profiles remain limited. Short Browser label **Render** plus `#help-render`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add camera and exposure (render.05, `working_subset`). Camera fov 10–90 and exposure −5 to 5 EV scale the portable PPM. Depth of field remains limited. Short Browser label **Render** plus `#help-render`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add in-canvas ray tracing (render.06, `working_subset`). rayTrace shades a unit disk in the portable PPM. Path tracing and bounces remain limited. Short Browser label **Render** plus `#help-render`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add local final rendering (render.07, `working_subset`). render_local stores lastImage width/height and returns a PPM up to 256 px. Denoisers remain limited. Short Browser label **Render** plus `#help-render`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add cloud rendering jobs (render.08, `working_subset`). Named local jobs with status queued, done or local. Cloud upload remains limited. Short Browser label **Render** plus `#help-render`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add render gallery (render.09, `working_subset`). Up to eight named gallery entries store the last image size. Cloud galleries remain limited. Short Browser label **Render** plus `#help-render`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add image export (render.10, `working_subset`). `export_render_image` writes a PPM from lastImage or 16×16. PNG and EXR remain limited. Short Browser label **Render** plus `#help-render`. Standing acceptance: no long UI text; explanations behind a help (?) icon.

**Platforms:** macOS (Apple silicon, arm64) only for now. Windows installers are coming in a later update to this release.
