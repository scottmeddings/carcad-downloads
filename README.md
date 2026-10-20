# Desktop downloads

Public distribution repository: https://github.com/scottmeddings/carcad-downloads

Keep application source in the private CarCad repository. The public repository contains only installers, checksums and release notes. It currently has no published installers; code signing is still pending.

## Publishing each update

1. Build and test the desktop application. Sign and verify the Windows installers before publication. State macOS processor/OS requirements and signing/notarisation status in release notes.
2. Create a **draft GitHub Release** with a unique version tag, for example `v1.2.3`.
3. Upload the complete set of supported installers using these exact asset names:

| Platform | Asset name | Permanent Cloud link |
| --- | --- | --- |
| Windows ARM64 | `CarCad-windows-arm64.exe` | `/download/windows-arm64` |
| Windows x64 | `CarCad-windows-x64.exe` | `/download/windows-x64` |
| macOS | `CarCad-macos.dmg` | `/download/macos` |
| Linux x64 | `CarCad-linux-x64.AppImage` | `/download/linux-x64` |

These names are the distribution contract, regardless of the build system's output names. Renaming a signed installer does not change its contents. Upload installers as release assets, never Git LFS pointers or source archives. Do not publish Linux until it is approved for release. A platform omitted from a release becomes unavailable; each release must include every platform you intend to offer. Reuse an unchanged, verified installer if appropriate and disclose its embedded version in release notes.

4. Include release notes and SHA-256 checksums. Publish the draft as a stable release and mark it Latest only after all uploads finish. Prereleases are ignored. Never replace assets on a published version; issue a new tag instead. Retain old releases so existing links and rollbacks continue working.
5. Cloud synchronises within 15 minutes **when its Laravel scheduler is running**. Run `php artisan downloads:sync` for an immediate refresh. Confirm `/download` shows the version and each button retrieves the correct architecture. The site validates metadata, not installer signatures or installation success.

## Deployment and recovery

Run migrations on deployment. Enable the Laravel Cloud scheduler; shared database/cache must be available for the scheduler's single-server lock. No GitHub token is needed: only public release metadata is read. The visitor request never calls GitHub's API. A database snapshot survives deployments and cache clears; transient errors, rate limiting, empty or invalid releases leave the last good snapshot intact and fail the command visibly in scheduler logs. GitHub must still be available to deliver the installer itself.

Optional environment settings:

```
CARCAD_DOWNLOAD_REPOSITORY=scottmeddings/carcad-downloads
# Pin a published stable tag for rollback; unset to follow Latest again:
CARCAD_DOWNLOAD_RELEASE_TAG=v1.2.3
```

After changing configuration, rebuild the configuration cache and run `php artisan downloads:sync`. Version-specific redirects are temporary and use `Cache-Control: no-store`, so permanent Cloud URLs follow the current snapshot. Existing per-platform URL/version environment settings remain fallback only before the first successful sync.

Initial production acceptance remains pending: publish signed installers, enable/check the scheduler, and verify real downloads on all supported operating systems. Website changes do not automatically publish new desktop binaries from the private repository's `release/` folders.
