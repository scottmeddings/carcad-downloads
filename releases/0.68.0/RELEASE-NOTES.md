# CarCad 0.68.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored.

Plain release build: filenames and the UI show 0.68.0, no test label. The Cloud features (cloud.01–cloud.08) are stubbed until the live CarCad Cloud service ships. This release also includes the changes from 0.66.0 and 0.67.0, which were not published as separate releases.

## Install on Linux (x64)

- **AppImage** (most distributions): `chmod +x CarCad-0.68.0-linux-x64.AppImage` then run `./CarCad-0.68.0-linux-x64.AppImage`.
- **Debian / Ubuntu (.deb)**: `sudo apt install ./carcad_0.68.0_amd64.deb`
- **Snap**: `sudo snap install --dangerous carcad_0.68.0_amd64.snap` (`--dangerous` is needed until CarCad is in the Snap Store).

## Install on macOS (Apple silicon, arm64)

- Open `CarCad-0.68.0-macOS.dmg` and drag CarCad to Applications.

## Windows

Windows 0.68.0 installers follow separately. Until then, the Windows ARM64 and x64 installers from [CarCad 0.65.0](https://github.com/scottmeddings/carcad-downloads/releases/tag/v0.65.0) are current.

Verify downloads against `SHA256SUMS.txt`.

## 0.68.0

Batch 39 re-cut (25 Oct 2026) at facing-safety `6df901b`. Portable CTest 253/253 and Linux CTest 264/264 (253 portable names; 264 on Linux/Windows, 265 on macOS with `macos_arch`). Priority set 8/143 (document.04/.06/.12 + sketch.01/.08/.09/.11 + cam2d.03). Ledger: 35 working / 274 partial / 86 stub / 44 planned.

- Units (document.01): Browser `#document-units` switches mm, cm, m, in, ft for feature-editor length fields and the stats line. Sketch, measure, mass, parameters and CAM stay in millimetres. CTest `document.01`.

- Undo (document.05): 200-snapshot stacks; 40 undos stay available. CTest `document.05`.

- Recovery (document.06): 32 MiB / 2000 features; 80-feature snapshot accepted. CTest `document.06`.

- Bodies (document.08): New Body catalog and select. The kernel rejects more than 20 solids. CTest `document.08`.

- Components (document.09): parent nesting and occurrences in the Browser tree. Occurrences only translate; Add Occurrence uses [20,0,0]. CTest `document.09`.

- Materials (document.10): library defaults (Aluminum 2700 kg/m³, …). Mass works on one solid only. CTest `document.10`.

- Imports (document.11): inch source converts scale to 25.4. CTest `document.11`.

- Schema / save (document.12, document.15): document units are stamped on migrate/save/open. Sketch, measure, mass, parameters and CAM stay in millimetres. CTest `document.12` / `document.15`.

- Feature delete (document.14): dependents must be deleted first — delete does not cascade. The editor Delete key removes one feature with no check. CTest `document.14`.

- Sketch family (sketch.01–.20, `working_subset`). Planar closed profiles with holes; interactive lines, rectangles, circles, arcs, ellipses, splines, polygons, slots, midpoint line, conic, construction, text (1–2000 characters), 3D paths, project/intersect, offset, trim/extend/break, fillet/chamfer, mirror and patterns (2–1000 copies). Native Gauss-Newton solver: over- and under-constrained states, live drag, fully-constrained colouring (blue free / ink determined). Automatic H/V, on-curve, midpoint, origin, rectangle and tangent-arc inferences (Ctrl suppresses). CTest `sketch`.

- Facing (cam2d.03, `working_subset`). Last pass lands on the part top; the path covers the stock face plus a tool-radius overrun, including a long-axis sweep when the tool is wider than both stock axes and a single pass when ymin==ymax; stepover is a user setting (default 0.7 D, at least 5% of D, never more than D); first motion is a G0 Z-only retract to clearance, then an XY rapid, then feed-down off the stock; `check_nc` checks whole moves (crossing/overlapping rapids, rapids that do not clear zmax by 1 mm, G1 plunge including inside-stock after side entry, G91, M5 before cutting, first-motion Z-only safe start, posted T matches the setup); clearance must be at least 1 mm above the stock and part tops. CTest `cam2d.03` runs `apply_cam2d` then `simulate_stock` and a 200×200 swept-disc sample and asserts zero leftover cells. Headless `cam2d_ui` drives the facing fields and the real regenerate error path.

Correction (24 Oct 2026): an independent audit at 3b02d5e found these 0.68.0 document claims false. Units only change the feature-editor length fields and the stats line; sketch, measure, mass, parameters and CAM stay in millimetres. Twenty-one bodies still fail — the kernel rejects more than 20 solids. Delete does not cascade: the app says “Delete dependent features first”, and the editor Delete key removes one feature with no check. Mass works on one solid only. Occurrences only translate, and Add Occurrence always uses [20,0,0]. Most document tests call native helpers the running app never calls.

**Platforms:** Linux x64 and macOS (Apple silicon, arm64). Windows 0.68.0 installers follow separately.
