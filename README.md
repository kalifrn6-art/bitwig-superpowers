# Bitwig Superpowers

Native MIDI Tools and Audio Tools for Bitwig Studio.

This repository is the public download page. The implementation and development
history are private. Installers do not include Bitwig Studio, Bitwig vendor JARs,
license keys, or a Bitwig license. You must use your own valid Bitwig installation
and license.

**Superpowers is free and made by one person.** If it helps your music, please
[support the project](https://buy.stripe.com/9B64gA1b04jzaJbgyi1Jm00). It keeps new tools coming.

Website and feature tour: [kalifrn.com/superpowers](https://kalifrn.com/superpowers/)

## Downloads

macOS and Windows are native graphical installers with their own Python and
reviewed FFmpeg/ffprobe builds; no separate Python or FFmpeg is needed. Linux is a
small command-line installer. Readable project implementation source is not
distributed. Compiled code can still be reverse-engineered.

Download installers only from the [Releases](https://github.com/kalifrn6-art/bitwig-superpowers/releases)
page. Do not use GitHub's automatically generated "Source code" archives; they
contain only this public download-page README.

### Superpowers Beta 6.0.0 (Bitwig 6.1.7)

| Platform | Bitwig | Package |
|---|---|---|
| macOS 13+ Apple Silicon | **6.1.7** | [Beta 6.0.0 DMG](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-6.0.0/Bitwig-Superpowers-macOS-AppleSilicon-Beta-6.0.0.dmg) |
| Windows 10/11 x64 | **6.1.7** | [Beta 6.0.0 EXE](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-6.0.0/Superpowers-Windows-x64-Beta-6.0.0.exe) |
| Linux x64 (.deb or manually unpacked folder) | **6.1.7** | [Beta 6.0.0 GZ](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-6.0.0/Superpowers-Linux-x64-Beta-6.0.0.tar.gz) |

#### Superpowers for Patchbay (beta 6.0.0-dev.2)

For unmodified Bitwig Studio **6.1.7** with Patchbay **0.36.0-dev.16** (21 Superpowers mods + 3 required frameworks; Clean Waveforms excluded). Extract the outer ZIP, leave the 24 ZIPs inside `mods/` compressed, and add all 24 via **Mods → Add Mod…** in Patchbay. Do not mix platform ZIP sets.

| Platform | Bitwig / Patchbay | Bundle |
|---|---|---|
| macOS | **6.1.7** · `0.36.0-dev.16` | [Patchbay macOS ZIP](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-6.0.0/Superpowers-Patchbay-6.0.0-dev.2-macos.zip) |
| Windows (experimental) | **6.1.7** · `0.36.0-dev.16` | [Patchbay Windows ZIP](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-6.0.0/Superpowers-Patchbay-6.0.0-dev.2-windows.zip) |
| Linux (experimental) | **6.1.7** · `0.36.0-dev.16` | [Patchbay Linux ZIP](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-6.0.0/Superpowers-Patchbay-6.0.0-dev.2-linux.zip) |

### Patchbay Launcher catalog

All 24 inner ZIPs per platform are also published as individual release assets: 21 Superpowers mods and the 3 required frameworks (72 ZIPs total). Add a **Mods** source for repository `kalifrn6-art/bitwig-superpowers` and use the filter for your operating system:

| Platform | Source filter |
|---|---|
| macOS | `*.macos.zip` |
| Windows (experimental) | `*.windows.zip` |
| Linux (experimental) | `*.linux.zip` |

Assets use `<mod-id>-<version>.<platform>.zip`, for example `superpowers-freeze-6.0.0-dev.2.macos.zip`. The stable preferences framework uses `preferences-composition-framework-1.0.0-platform.macos.zip` (or `.windows.zip` / `.linux.zip`) so the Launcher accepts the filename. ZIP contents and manifest versions are unchanged from the bundles. Include all three frameworks: **Actions and Menus**, **Inspector**, and **Preferences**; these existing packages do not declare all framework dependencies in the Launcher's `requires` field, so select the frameworks explicitly. Use only one platform filter. The original bundles remain available for manual import.

[Release notes](RELEASE-6.0.0.md) · [SHA-256 checksums](SHA256SUMS-6.0.0.txt) · [Feature tour](https://kalifrn.com/superpowers/)

**New:** MIDI Comp, Glissando, Browser Rank/sort, Clean Waveforms and Settings → Mods.
**Updated:** Freeze MIDI notes/snowflake/tails and queue handling, Capture MIDI overdub, and MIDI Tools visual helpers. All previous tools remain included; Cmd+3 remains removed.

**Validation:** macOS Freeze/Capture and Patchbay source selection confirmed by the user; all standalone and Patchbay packages passed offline checks. Windows standalone started under CrossOver. **Windows and Linux interactive validation (standalone and Patchbay) remains pending**; optional Audio Tools setup on Linux is also pending.

Beta 6 supports **exactly Bitwig 6.1.7**. For Bitwig 6.1.5 keep [Beta 5.0.2](https://github.com/kalifrn6-art/bitwig-superpowers/releases/tag/superpowers-beta-5.0.2); for 6.1.3/6.1.4 keep [Beta 5](https://github.com/kalifrn6-art/bitwig-superpowers/releases/tag/superpowers-beta-5); for 6.1.1/6.1.2 keep Beta 4.3.

### Previous releases

**Fixed in 5.0.2**

- **Projects that would not open** ("Unknown enum value with id 7 for enum quantize_grid_subdivision",
  [#19](https://github.com/kalifrn6-art/bitwig-superpowers/issues/19)): projects saved with a 5T / 7T
  grid failed to load. The cause was the Cmd+3 straight / triplet toggle, which is now **removed**;
  the grid works exactly like stock Bitwig again. Your projects were never damaged.
- **Shortcuts you can change:** Collapse / Expand Device and Collapse / Expand Track are now listed in
  Settings > Shortcuts. Remap or remove their keys there; the defaults (`-`, `+` / `=`, Left, Right)
  no longer override your choice.

**New in Beta 5** (also in 5.0.2)

- **Capture MIDI:** keeps the last 30 seconds you played; each capture uses up the buffer, so the next one never repeats notes.
- **Freeze:** one progress window for the whole queue, no repeated missing-plug-in prompts, clips keep their shape with hatched tails, Unfreeze waits until plug-ins reload, 24-bit renders.
- **Export with Group, Return and Master effects:** a new option in Export Audio.
- **Ramp:** Start / End velocity under the Velocity lane of the piano roll.
- **Piano roll:** selection follows moved notes, Cmd+E splits at the grid and keeps the pieces selected, Duplicate copies the full length. (Beta 5 also had Cmd+3 straight / triplet, removed in 5.0.2.)
- **Detect Event Key:** right-click an audio clip; its key is added to the clip name.
- **Device Keys:** `-` collapses the selected device, `+` / `=` expands it.
- **Groups:** lighter group summaries, a compact height toggle, Left / Right fold and unfold tracks, visible Shift ranges.
- **Linux** support (Bitwig 6.1.5).

**Something not working? Use Send Report.** Every installer has it (Linux:
`python3 superpowers_linux.py report`). It saves a zip with your logs on the
Desktop, with your user name and folders removed, and opens a prefilled GitHub
issue. Drag the zip in and submit. Nothing is sent automatically.

The installers check your exact Bitwig version and stop on an unknown or modified
Bitwig JAR instead of guessing. The Mac app is ad-hoc signed, not Developer ID
signed or notarized; the Windows EXE is not code-signed.

## Before installing

Save your projects and fully quit Bitwig Studio, its audio engine, and plug-in
hosts. Keep the installer for access to its restore tools. The installer verifies
the target and creates a verified backup
before replacing anything.

The optional Audio Tools setup downloads pinned Python packages and optional
models over outbound HTTPS. If the Microsoft Visual C++ x64 runtime is missing,
the Windows installer downloads Microsoft's signed installer and shows its normal
license UI. No inbound firewall rule is required.

## Safety and support

If these tools help your music, consider supporting the project. Your support
helps me maintain and improve Superpowers. Support is always optional.
[Support Superpowers through Stripe](https://buy.stripe.com/9B64gA1b04jzaJbgyi1Jm00)

Use beta software on backed-up projects. Nothing is uploaded automatically. To
report a problem, open a GitHub issue with your operating system, exact Bitwig
version, installer version, steps to reproduce, and sanitized logs. Never upload
your Bitwig JAR, license data, private projects, credentials, or personal paths.

Bitwig Studio is a product of Bitwig GmbH. This project is independent and is not
affiliated with or endorsed by Bitwig GmbH.
