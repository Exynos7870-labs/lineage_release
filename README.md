# Exynos7870-labs releases

Unofficial LineageOS builds for Samsung Galaxy devices with the Exynos 7870
SoC. The flashable zips are published under
[Releases](https://github.com/Exynos7870-labs/lineage_release/releases).

## Devices

| Device | Model | Current release line |
| :--- | :--- | :--- |
| `a3y17lte` | Galaxy A3 (2017) | LineageOS 22.2 |
| `j5y17lte` | Galaxy J5 (2017) | LineageOS 22.2 |

Older LineageOS 20 / 18.1 builds are still available in the release list.

## OTA updates

The builds use the LineageOS Updater. The OTA metadata is served from the
`22.2` branch:

- a3y17lte: <https://raw.githubusercontent.com/Exynos7870-labs/lineage_release/22.2/a3y17lte.json>
- j5y17lte: <https://raw.githubusercontent.com/Exynos7870-labs/lineage_release/22.2/j5y17lte.json>

Open **Settings → System → Updater** on the device. OTA updates only work
between builds signed with the same keys. Builds made with the public AOSP test
keys (including the early R1/R2 releases) require a one-time clean flash before
they can receive updates from the signed releases.

## Branch layout

| Branch | Purpose |
| :--- | :--- |
| `22.2` | Updater JSON files served to devices. Do not edit these by hand. |
| `lineage-22.2` | Target branch for LineageOS 22.2 GitHub releases. |
| `lineage-20` | Previous LineageOS 20 release line (default branch). |
| `lineage-18.1` | Previous LineageOS 18.1 release line. |

## Building from source

A complete guide is maintained in the build manifest repository:

**<https://github.com/samsungexynos7870/android_manifest_samsung_a3y17lte/blob/lineage-22.2/README.md>**

It covers the host packages and toolchain setup, `repo` initialization, key
generation, the build command and the output zip.

The published zips are signed with private Exynos7870-labs keys that are not
in any public repository. A self-built zip signed with your own keys requires a
clean flash and will not receive OTA updates from these releases.

## Reporting issues

Please use the [issue tracker](https://github.com/Exynos7870-labs/lineage_release/issues)
and include the device, build tag, kernel version and steps to reproduce.
