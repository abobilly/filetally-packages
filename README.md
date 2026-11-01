# FileTally packages

Publisher-maintained Windows x64 installation metadata for [FileTally](https://filetally.com/). Requires Windows 10 or later. FileTally is commercial software with a free trial. See [licensing](https://filetally.com/licensing) and the [EULA](https://filetally.com/eula).

## Scoop

With Scoop and Git available in your normal Windows account:

```powershell
scoop bucket add filetally https://github.com/abobilly/filetally-packages
scoop install filetally/filetally-np
```

For later releases, use `scoop update` followed by `scoop update filetally-np`. Remove the app with `scoop uninstall filetally-np`.

## Chocolatey

Download `filetally.1.0.1.nupkg` and `SHA256SUMS.txt` from [release v1.0.1](https://github.com/abobilly/filetally-packages/releases/tag/v1.0.1) into a fresh local folder. Compare `Get-FileHash .\filetally.1.0.1.nupkg -Algorithm SHA256` with the checksum file.

Use a user-writable Chocolatey installation from a non-elevated shell, under the Windows account that will use FileTally. From the package folder:

```powershell
choco install filetally --version 1.0.1 --source . --yes
```

For a later accepted package, download it into a new folder and run `choco upgrade filetally --source . --yes` there. Remove the app with `choco uninstall filetally --yes` under the same account. The GitHub release URL hosts downloads; the local package folder is Chocolatey's source.

## Existing installations and updates

Each manager verifies its ownership before upgrading or removing an installation. Continue using the original channel for an existing direct or other-manager installation. Licenses, trial history and saved scans survive removal.

This is FileTally's publisher bucket and package-download channel. Chocolatey Community Repository and Scoop Main/Nonportable listing are separate submission processes.

Maintainers pin the accepted version, immutable installer URL, installer SHA256 and installed-app SHA256, then verify the affected install, upgrade and removal behavior before release. App source and private release records stay in the main private repository.
