# CarCad 0.43.0

CI waived by Scott on 18 Oct 2026, re-run when billing is restored.

Plain release build: filenames and the UI show `0.43.0`, no test label. 0.43.0 includes 0.42.0, which did not get its own release. The Cloud features (cloud.01–cloud.08) are stubbed until the live CarCad Cloud service ships.

## 0.43.0

Batch 14 of ten features. Targets: mfg_setup.03, mfg_setup.04, mfg_setup.05, mfg_setup.06, mfg_setup.07, mfg_setup.08, mfg_setup.09, mfg_setup.10, mfg_setup.11, mfg_setup.12. Portable CTest 55/55 and Linux CTest 66/66 after mfg_setup.12 (includes `carcad_cloud`). Linux x64 test packages stay under `test/linux-x64/0.43.0`. Windows installers follow separately.

- Add stock and fixtures (mfg_setup.03, `working_subset`). stock box millimetres become manufacturingStock. Fixtures remain limited. Short Browser label **Setup** plus `#help-mfg-setup`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add tool and holder libraries (mfg_setup.04, `working_subset`). Named tools become manufacturingTool. Holders remain limited. Short Browser label **Setup** plus `#help-mfg-setup`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add machine libraries and kinematics (mfg_setup.05, `working_subset`). Named machines become manufacturingMachine. Kinematics remain limited. Short Browser label **Setup** plus `#help-mfg-setup`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add post processor libraries (mfg_setup.06, `working_subset`). Named posts become manufacturingPost. Vendor posts remain limited. Short Browser label **Setup** plus `#help-mfg-setup`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add toolpath templates (mfg_setup.07, `working_subset`). Named templates become manufacturingTemplate. Adaptive paths remain limited. Short Browser label **Setup** plus `#help-mfg-setup`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add operation parameters and feeds (mfg_setup.08, `working_subset`). feeds millimetres/min become manufacturingFeed. Coolant remains limited. Short Browser label **Setup** plus `#help-mfg-setup`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add toolpath ordering (mfg_setup.09, `working_subset`). order ids become manufacturingOrderCount. Rest machining remains limited. Short Browser label **Setup** plus `#help-mfg-setup`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add stock and machine simulation (mfg_setup.10, `working_subset`). sim step millimetres become manufacturingSimStep. Machine simulation remains limited. Short Browser label **Setup** plus `#help-mfg-setup`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add collision checks (mfg_setup.11, `working_subset`). collision clearance millimetres become manufacturingClearance. Holder checks remain limited. Short Browser label **Setup** plus `#help-mfg-setup`. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add setup sheets (mfg_setup.12, `working_subset`). sheet title becomes manufacturingSheet. Photos remain limited. Short Browser label **Setup** plus `#help-mfg-setup`. Standing acceptance: no long UI text; explanations behind a help (?) icon.

## 0.42.0 (included)

Batch 13 of eight cloud features. Targets: cloud.01, cloud.02, cloud.03, cloud.04, cloud.05, cloud.06, cloud.07, cloud.08.

- Add required sign-in gate (cloud.01, `working_subset`). Gate after splash when features.sign_in_required is true. Create account / Sign in, privacy line, PKCE S256, loopback callback. Live HTTPS remains limited. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add remembered sign-in and silent refresh (cloud.02, `working_subset`). One store item holds tokens and install_id. Silent refresh then heartbeat. Offline after first sign-in. invalid_grant signs out without the gate. Live HTTPS remains limited. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add account button (cloud.03, `working_subset`). Account button shows initials, Offline and Sign in. Sign out revokes and keeps install_id. Live HTTPS remains limited. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add install registration and heartbeat (cloud.04, `working_subset`). install_id UUID, POST /me/installs 201 then 200, launch heartbeat, app_installs false skips calls. Live HTTPS remains limited. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add Marketplace web view (cloud.05, `working_subset`). Marketplace modal iframe /appmarketplace?embed=1&theme=. postMessage must be source carcad-marketplace v:1 from the expected origin. Live listings remain limited. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add Marketplace sign-in hand-off (cloud.06, `working_subset`). POST /embed/exchange-codes returns a one-time code for form-POST /embed/session. Tokens stay out of URLs. Live embed sessions remain limited. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add Cloud drawings in Open Project (cloud.07, `working_subset`). Open Project > Cloud drawings lists GET /me/models. Signed-out and Offline copy. Thumbnails remain limited. Standing acceptance: no long UI text; explanations behind a help (?) icon.
- Add download and open cloud model (cloud.08, `working_subset`). Download URL expires in 300s. sha256 mismatch is rejected. Interrupted transfer UI remains limited. Standing acceptance: no long UI text; explanations behind a help (?) icon.

**Platforms:** macOS (Apple silicon, arm64) only for now. Windows installers follow separately.
