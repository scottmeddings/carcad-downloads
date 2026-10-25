# CarCad 0.69.0

CI waived by Scott on 18 Oct 2026 (GitHub billing), re-run when billing is restored. Verified locally instead: Linux CTest 268/268, macOS (Mac mini) 269/269, Windows ARM64 and x64 268/268.

Plain release build: filenames and the UI show 0.69.0, no test label. The CarCad Cloud sign-in uses the live service at https://carcad.com.au.

## Install on Linux (x64)

- **AppImage** (most distributions): `chmod +x CarCad-0.69.0-linux-x64.AppImage` then run `./CarCad-0.69.0-linux-x64.AppImage`.
- **Debian / Ubuntu (.deb)**: `sudo apt install ./carcad_0.69.0_amd64.deb`
- **Snap**: `sudo snap install --dangerous carcad_0.69.0_amd64.snap` (`--dangerous` is needed until CarCad is in the Snap Store).

## Install on macOS (Apple silicon, arm64)

- Open `CarCad-0.69.0-macOS.dmg` and drag CarCad to Applications.

## Install on Windows (ARM64 or x64)

- Choose ARM64 for Windows PCs with an ARM-based processor, x64 for 64-bit Intel or AMD processors.
- **Setup.exe**: run `CarCad-0.69.0-Windows-ARM64-Setup.exe` or `CarCad-0.69.0-Windows-x64-Setup.exe`.
- **MSI**: run `CarCad-0.69.0-Windows-ARM64.msi` or `CarCad-0.69.0-Windows-x64.msi`.
- The installers are unsigned, so Windows SmartScreen may warn. Choose **More info**, then **Run anyway**.
- The x64 build was tested under x64 emulation on Windows 11 ARM64, not on native x64 hardware.

Verify downloads against `SHA256SUMS.txt`.

## 0.69.0

Batch 40 cut (25 Oct 2026) at pre-cut `9840162`. Linux CTest 268/268, macOS (Mac mini) 269/269, Windows ARM64 and x64 268/268. Priority set 8/143. Ledger: 36 working / 275 partial / 86 stub / 44 planned.

- Cloud control (cloud.09, `partial`). One Sign in / avatar control as the last item in the app header at the top right. Sign in runs the existing PKCE system-browser flow. Signed-in shows `avatar_url` from GET `/api/v1/me`, or initials from the name if the image is missing or fails (single-name and empty-name). The avatar menu lists the name, Account and Sign out. Account opens `capabilities.account_url` from GET `/api/v1/desktop/capabilities` exactly as given, in the system browser only. Sign out returns to Sign in. Live HTTPS uses libcurl with TLS verification against https://carcad.com.au. CTest `cloud_ui` / `carcad_cloud` / `carcad_cloud_http`.

- Facing/CAM dark hover contrast. Dark `--hover` is `#1f2733` so hover is visible on the panel and muted/body text stay at least 4.5:1. `#banner-stop-control:hover` uses its own background/text pair in both themes. CTest `theme`.

- Grid extent (sketch.21, `working_subset`). Default viewport and sketch grid is 500 × 500 mm. The viewport Display popover **Grid size** (50–10000 mm, help icon) is remembered across launches and applied to new and open documents. CTest `grid_extent`.

- Snap packaging: `network-bind` for the loopback service and OAuth callback; store `website` / `contact` / `issues`; snap desktop drops MIME types and `%F`. `package-snap.sh` requires real `snapcraft pack` (core24 + gnome) and does not hand-assemble. CTest `snap_packaging`.

- CarCad Cloud live origin is `https://carcad.com.au` (`kCarCadCloudOrigin`). Desktop authorize URL, API base, browser allowlist, marketplace embed, snap website, tests and the ledger use that single constant. CTest `carcad_cloud` / `cloud_ui` / `snap_packaging`.

- Cloud client does not hold its mutex across HTTP; capabilities cache stamps only on success with a short failure backoff; a new sign-in clears `account_url` and the cache; persist marks saved only after a successful write. CTest `carcad_cloud`.

- Desktop Cloud HTTP is live: libcurl over HTTPS with TLS verification against `kCarCadCloudOrigin`, PKCE sign-in (CSPRNG verifier/state, system browser, loopback, token exchange, refresh, revoke), live `/api/v1/me` and `/api/v1/desktop/capabilities`, and OS token storage (Keychain / Credential Manager / libsecret). CTest `carcad_cloud_http` / `carcad_cloud`.

- Cloud retired-host scan walks only `native/`, `web/`, `packaging/` and `docs/`, so `dist-macos` / `dist-windows*` staging no longer breaks `carcad_cloud`. `carcad_cloud_http` runs on all three platforms; macOS/Windows use a test-only TLS trust hook for the mock certificate. CTest `carcad_cloud` / `carcad_cloud_http`.

- Cloud audit fixes: test-request hook lives in `forgecad::`; one refresh in flight; file fallback only when the OS store fails; libsecret required on Linux; snap `password-manager-service`; `account_url` must be on the Cloud origin; macOS HTTP does not follow redirects; persist releases the mutex before Keychain; Windows credential blob size is capped; CI/`CARCAD_FILE_SECRETS` ignored in release builds. CTest `carcad_cloud` / `carcad_cloud_http` / `snap_packaging`.

- Mock HTTPS cert builder uses `X509_NAME_new` plus `X509_set_subject_name` / `X509_set_issuer_name` so it compiles on OpenSSL 3 and OpenSSL 4 (Homebrew 4.0.3). CTest `carcad_cloud_http`.

- Cloud audit of af7d96a: `refresh_silent` uses an RAII guard and a 60s wait (connect 10s + request 30s + margin; tests inject a short bound) so a 200 without `access_token` or a persist throw cannot leave later 401s blocked on `refresh_cv_`; persist serialises OS saves with a monotonic sequence so an older snapshot cannot overwrite a newer one and sign-out always wins; a failed OS token save deletes the stale OS entry before the file fallback; Linux packaging lists `libsecret-1-dev`, `build.sh` checks for it, the snap stages `libsecret-1-0` (gnome-46-2404 also ships it), the AppImage bundles libsecret, and the `.deb` Depends on `libsecret-1-0`. CTest `carcad_cloud` / `carcad_cloud_http` / `snap_packaging`. macOS CI remains waived (billing); Mac mini local build is the Mac verification.

- Grid save network errors restore the previous non-default input. Theme active rows use `--selected` and `--accent`, not `--hover`; system-dark `--selected` matches dark. CTest `grid_extent` / `theme`.

- Snap license `Proprietary` (snapd's known token; lowercase `proprietary` fails `snap pack`), contact `support@carcad.com.au`, website `https://carcad.com.au`. Pack grade/version comes from the build CMakeCache or binary; destructive-mode sudo does not preserve `HOME`; missing `unsquashfs` fails. CTest `snap_packaging`.

**Platforms:** Linux x64, macOS (Apple silicon, arm64), and Windows ARM64 and x64.
