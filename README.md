# Metro Awakening FlatXR PC Mod

An experimental keyboard-and-mouse flatscreen mod for Metro Awakening, built around a custom OpenXR runtime and UE4SS.

## Download

[Download the preview installer ZIP](https://github.com/jock1111/metro-awakening-flatxr/releases/download/v2026.11.11.1-preview/Metro-Awakening-FlatXR-Installer-2026.11.11.1.zip)

[Release notes and individual files](https://github.com/jock1111/metro-awakening-flatxr/releases/tag/v2026.11.11.1-preview)

The ZIP includes setup, installation notes, the supported-build fingerprints and the installer checksum. Setup is unsigned.

## Compatibility and testing

- Windows 10 or 11, x64.
- Setup checks the shipping executable, `global.utoc` and `pakchunk0-Windows.utoc` against the reference build. The supported executable fingerprint starts with `c5d4ab74a0e82983`.
- The launcher checks those fingerprints again when starting the game.
- Steam installation detection, App ID metadata, client preflight and launcher environment are covered by automated fixture tests. **Steam gameplay validation is pending.**
- **The latest weapon alignment, weapon swaps and backpack interactions require in-game validation.**

Installer tests cover clean installation, existing-loader backups, repair, locked-file rollback, uninstall, configuration recovery and special-character paths.

## Installation

1. Close Metro Awakening and extract the ZIP.
2. Run setup and select the game folder containing `Impact` and `Impact.exe`.
3. For Steam, locate that folder through Properties → Installed Files → Browse.
4. Start the usual game client. For Steam, sign in to the account that owns Metro Awakening.
5. Use the **Metro Awakening PC** shortcut.

For a detected Steam installation, setup installs App ID metadata for the custom launcher. Valve documents that metadata for applications launched outside the Steam client. [Steamworks initialization documentation](https://partner.steamgames.com/doc/api/steam_api)

## Preview features

- Keyboard movement, mouse look, sprint, crouch and hop.
- Crosshair interaction and off-hand grabbing.
- Size-aware held-item positioning and first-person firearm poses.
- Right-click iron sights, a weapon selector and an ammo display.
- Backpack equipment interface using Awakening's models.
- Full-window loading artwork, opening tutorial suppression and hold-Space caption skipping.

## Main controls

| Action | Control |
| --- | --- |
| Move and look | WASD and mouse |
| Sprint / crouch / hop | Shift / Ctrl / Space |
| Interact / off-hand grab or release | E / Q |
| Fire / aim / reload | Left click / right click / R |
| Weapon selector | Hold Tab, select with mouse or wheel, release Tab |
| Backpack | I |
| Use selected backpack equipment | E or left click |
| Flashlight | F |
| Handgun / primary / grenade / heal | 1 / 2 / 3 / 4 |
| Gas mask / filter / lighter / charger | G / T / L / Y |
| Holster / throw | H / middle click |
| Skip opening caption pages | Hold Space |

Runtime controls and view settings are in `FlatXR/flatxr.ini`.

## Repair and uninstall

Rerun setup to repair an installation. Use Windows Installed Apps or `FlatXR/setup/unins000.exe` to uninstall. The uninstaller restores the saved loader and settings. Backups are in `FlatXR/setup/original`, and recovered configuration edits are in `FlatXR/Recovered files`.

## Feedback

Report issues with the game build, Windows version, the control or item being tested and steps to reproduce the problem. Steam testing reports should include the Steam build ID and the installer compatibility-check result.

Third-party licenses and notices are included with the installer.
